# Concurrency 

Swift has built-in support for writing asynchronous and parallel code in a **structured way** Asynchronous code can be **suspended and resumed later**, although only one piece of the program executes at a time. Suspending and resming code i your program lets **it continue to make progress on short-term operations like updating its UI while continuing to work on long-running operations** like fetching data over the network or parsing files. 

**Parallel code** - means that multiple pieces of code run simultaneously, for example, a computer with a four-core processor can run **four pieces of code at the same time**, with each core carrying out one of the tasks. 

A program that uses parallel and asynchroonous code carries out multiple operations at one time; **this suspends operations that are waiting for an external system**, and makes it easier to write this code in a **memory-safe way**. 

The additional scheduling flexibility from parallel or asynchronous code also **comes with a cost of increassed complexity**. Swift lets you express you intent in a way that **enables some compile-time checking**-- for example, you can use **actors to safely access mutable state**. However, addding concurrency to slow or buggy code isn't a garuntee that it will become fast or correct. In fact, adding concurrency might even make your code harder to debug. However, using Swift's language-level support for concurrency in code that needs to be concurrent means **Swift can help you catch problems at compile time**. 


# Defining and Calling Asynchronous Functions 
An **asynchronous function** or **asynchronous method** is a special kind of function or method that **can be suspending while it's partway through execution**. 

This is in constract to ordinary, synchronous functions and methods, **which either run to completion, throw an error, or never return**. An asynchronous function or method still does one of those three things, **but it can also pause in the middle when it's waiting for something**. Inside the body of an asynchronous funciton or mehtod, **you mark each of these places where execution can be suspended**. 

To indicate that a funciton or method is asynchronous, you write the **async** keywrod in its declaration after its parameters, similar to how you use **throws** to marka a throwing funciton. If the funcion or method returns a value, you write **async** before the return arrow (->). For example, here's how you might fetch the names of photos in a gallery: 

``` swift 
// asynchornous function 1
func listPhotos(inGallery name: String) async -> [String] {
    let result = / ... some asynchornous networking code
    ...
    return result
}
``` 

For a function or method that's both **asynchornmous and thorwing**, you write **async** before **thows**. 

When calling an asynchronous method, **execution suspends until that method reuturns**. You write **await** in fornt of the call to mark the possible supspention point. 

This is like writing **try** when calling a throwing funciton, to mark the possible change to the program's flow if there's an error. Inside an asynchornous method, the flow of execution is supsended **only when you call another asynchronous method**-- suspension is never implic or preeptive-- which means every possible suspention poiint is market with **await**. 

For example, the code below fetches the names of all the pictures in the gallery and then shows the first picture: 

``` swift 
let photoNames = await listPhotos(inGallery: "Summer Vacation")
let sortedNames = photoNames.sorted()
let name = sortedNames[0]
let photo = await downloadedPhoto(named: name)
show(photo)
``` 

Because the **listPhotos(inGallery:)** and **downloadedPhoto(named:)** functions both need to make network requrest, they could take **a relatively long time to complete**. Making them both asynchronous by writing **async** before the return arrow lets the **the rest of the app's code keep running while this code waits for the picture to be ready**. 

To understand the concurrent nature of the example above, here's one possible order of execution. : 

``` swift 
let photoNames = await listPhotos(inGallery: "Summer Vacation")
let sortedNames = photoNames.sorted()
let name = sortedNames[0]
let photo = await downloadedPhoto(named: name)
show(photo)
``` 

Because the **listPhotos(inGallery:)** and **downloadedPhoto(named:)** functions both need to make network requrest, they could take **a relatively long time to complete**. Making them both asynchronous by writing **async** before the return arrow lets the **the rest of the app's code keep running while this code waits for the picture to be ready**. 

To understand the concurrent nature of the example above, here's one possible order of execution. 

1. The code starts running form the first line and runs up to the first **await**. It calls the **listPhotos(inGallery:)** function and **supends execution while it waits for a function to return**. 
2. While this code's execution is suspended, **some other concurrent code in the same program runs**. For example, maybe a long-running backgorund task continues updates a list of new photo galleries. That code **also runs until the next suspention point**, marked by **await**, or until it completes. 
3. After **listPhotos(inGallery:)** returns, this code **continues execution starting at that point**. It assigns the value that was returned to **photoNames**.   


# References 
Apple. (2022). The Swift Programming Language (5.7 Edition).
