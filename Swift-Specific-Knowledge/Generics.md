# Generics 

Generic code enables you to write **flexible, reusable functions and types that can work with any type**, subject to requirements that you define. YOu can write code that **avoids duplication and expresses its intent in a clear, abstracted manner**. 

Much of the Swift standard library is built with generic code. For example, Swift's **Array** and **Dictionary** types are both generic collections. 

For instance, you can create an array that holds **Int** values, or an array that holds **String** values, or indeed an array for any other type that can be created in Swift. Similarly, you can create a **dictionary** to store values of any specified type, and there are **no** limitations on what that type can be. 

# Problems Generics Solve
Generic functions **can work with any type**. 

So instead of writing a function swapTwoInts(), make once instead called swapTwoValues() which is **polymorphic**. 

``` swift 
// nongeneric swap
func swapTwoInts(_ a: inout Int, _ b: inout Int) {
    let temp = a
    a = b
    b = temp
}

// generic swap
func swapTwoValues<T>(_ a: inout T, _ b: inout T) {
    let temp = a
    a = b
    b = temp
}
```  

Notice that the body of the swapTwoValues() fucntion is identical to the body of the swapTwoINts function. Howver, within the first line of swapTwoValues there is a generic placeholder **<T>** which says "a and b must be of the same type, but the actually type can be determined when the function is called". 

# Naming Type Paramters 
In most cases, type parameters have descriptive names, such as **Key** and **Valule** in **Dictonary<Key, Value>** and **Element** in **Array<Element>**, which tells the reader about the relationshiops between the type parameter and the generic type or function it's used in. 

# Generic Types 
In addition to generic functions, Swift enables you to define your own **generic types**. 

## These are: 
- custom classes 
- structures 
- and enumerations that can work with **any type** similar to **Array** and **Dictionary** 

## This stack will only accept Ints: 
``` swift
// nongeneric stack
struct IntStack {
    var collection = [Int]()
    
    // add to top
    mutating func push(_ element: Int) {
        collection.append(element)
    }
    // pull off topmost item
    mutating func pop() -> Int {
        collection.removeLast()
    }
}
let limitedStack = {
    var stack = IntStack()
    stack.push(1)
    stack.push(2)
    stack.push(3)
    stack.pop()
    print(stack.collection)
} // Output when limitedStack() -> [1, 2] 
``` 

## This stack can work with any type: 
``` swift 
// generic stack
public struct GenericStack<T> {
    var collection = [T]()
    
    // add to the top
    mutating func push(_ element: T) {
        collection.append(element)
    }
    // pull off topmost item
    mutating func pop() -> T {
        collection.removeLast()
    }
}



// generic stack with Ints
let intStack = {
    var stack = GenericStack<Int>()    // notice initialzing the type <Int>
    stack.push(10)
    stack.pop()
    stack.push(9)
    stack.pop()
    stack.push(8)
    print(stack.collection)
 } 

// generic stack with Strings
let strStack = {
    var stack = GenericStack<String>() // notice initialize the type <String>
    stack.push("red")
    stack.push("purple")
    stack.pop()
    stack.push("yellow")
    stack.push("green")
    print(stack.collection)
} // Output when strStack() -> ["red", "yellow", "green"]


// generic stack with Characters
let charStack = {
    var stack = GenericStack<Character>()  // notice initializing the type <Character>
    stack.push("a")
    stack.push("b")
    stack.push("c")
    print(stack.collection)
} // Output when charStack() -> ["a", "b", "c"]


// generic stack with Dictionary
let dictStack = {
    var stack = GenericStack<Dictionary<Int, String>>()    // notice initializing the type <Dictonary<Int, String>>
    stack.push([1: "Hayden"])
    stack.push([2: "Kimberly"])
    stack.push([3: "Kate"])
    stack.pop()
    stack.push([4: "Dave"])
    print(stack.collection)
} // Output when dictStack() -> [[1: "Hayden"], [2: "Kimberly"], [4: "Dave"]]
``` 
    
# References 
    
