# Functions 

**Functions** - are self-contained chunks of code that perform a specific task. You give a function a name that **identifies what it does**, and this name is used to "call" the function to perform its task when needed. 

Swift's unified function syntax is flexible enough to express anything from a simple C-style function with no parameter names **to a complex Objective-C style method with names and arguments labels for each parameter**. 

Parameters **can provide default values to simplify function calls and can be passed as in-out parameters**, which modify passed variables once the function has completed its execution. 

Every function in Swift has a type consisting of the function's parameter types and return type. You can use this type like any other type in Swift, **which makes it easy to pass functions as parameters to other functions and return functions from functions**. Functions can also be written within other functions to **encapsulate** useful functionality within a nested function scope. 

<img width="600" height="300" src="https://user-images.githubusercontent.com/109105989/198848918-e4768b3f-6c80-4eea-bb63-71ae7f958809.png"/> 

# Defining and Calling Functions 
When you define a function, you can optionally define one or more named, typed values that the function takes as input, known as **parameters**. 

You can also optionally define a type of value that the function will pass back as an **output** when it's done; this is known as its **return type**. 

Every function has a **function name**, which describes the task that the function performs. To use a function, you "call" that function with its name and pass it input values (**arguments**) that match the types of the function's parameters. A function's arguments must always be provided in the same order as the function's parameter list. 
<img width="800" height="300" src="https://user-images.githubusercontent.com/109105989/198849028-fafc2402-9fc7-4ebb-8617-31aae9db47d3.png"/> 

# Function Parameters and Return Values 
Function parameters and return values are extremely flexible in Swift. You can define anything from a single utility function with a single unnamed parameter to a complex function with expressive parameter names and different parameter options. 


## Functions without parameters

Functions aren't required to define input parameters. Below is a function **with no** input parameters, which will always return the **same String message**. 

```swift  
// functions without parameters
func nameSomethingYouLove() -> String {
    return "Coding!"
} 
print(nameSomethingYouLove()) 
/* OUTPUT
 Coding! 
*/
``` 

## Functions with single parameter and a single output 
```swift 
// single input single output (String)
func admitJob(job: String) -> String {
    return "I'm a \(job)."
}
print(admitJob(job: "developer"))
/* OUTPUT
 I'm a developer. 
*/
```

## Functions with multiple inputs and a single output 

Functions can have multiple input parameters, which are written with the **function's parenthesis**, separated by **commas**. 

``` swift
// multiple inputs single output (String)
func makeCoffee(type: String, alreadyMade: Bool) -> String {
    if alreadyMade {
        return prepared(type: type)
    } else {
        return unPrepared(type: type)
    }
}
func prepared(type: String) -> String {
    return "Your \(type) coffee is ready to enjoy."
}
func unPrepared(type: String) -> String {
    return "Your \(type) coffee isn't ready. Would you like to brew now?"
}
print(makeCoffee(type: "Italian roast", alreadyMade: true))
print(makeCoffee(type: "French roast", alreadyMade: false))
/* OUTPUTS
 Your Italian roast coffee is ready to enjoy.
 Your French roast coffee isn't ready. Would you like to brew now?
*/ 
```

## Functions with a single input and multiple outputs 

You can use a **tuple type** as the return type for a function to return multiple values as part of one compound return value. 

``` swift
// single input multiple outputs
func ageGap(arrayOfAges: [Int]) -> (minAge: Int, maxAge: Int) {
    var currentMin = arrayOfAges[0]
    var currentMax = arrayOfAges[0]
    for age in arrayOfAges[1..<arrayOfAges.count] {
        if age < currentMin {
            currentMin = age
        } else if age > currentMax {
            currentMax = age
        }
    }
    return (currentMin, currentMax)
}
print(ageGap(arrayOfAges: [10, 22, 4, 59, 26, 87]))
/* OUTPUT
 (minAge: 4, maxAge: 87) 
 */ 
``` 


## Functions with variadic parameters 

**Variadic parameters** - accept **zero or more** values of a specific type. 

You can use a variadic parameter to specify that the parameter can be passed **a varying number of input values** when the function is called. 

You write variadic parameters by inserting three-period characters (**...**) after the parameter's type name. 

```swift
// variadic inputs  
func findClassAverage(_ grades: Int...) -> String {
    var total = 0
    for scores in grades {
        total += scores
    }
    return "Your class average is \( total / grades.count)."
}
print(findClassAverage(87, 99, 96, 89))
/* OUTPUT
 Your class average is 92.
*/
``` 


## Functions with in-out parameters 

Function parameters are **constants by default**. This means if you try to change the value of a function parameter within the body of the function, you'll receive a compile-time error. This also means that you can't change the value of a parameter by mistake (thanks, Swift). 

If you want to modify a parameter's value, and you want those changes to persist after the function call has ended, define that parameter as an **in-out-parameter** instead. 

You write an in-out parameter by placing the **inout** keyword right before a parameter's type. 

An in-out parameter has a value that's passed **in** the function, is **modified** by the function, and is passed back **out** of the function to replace the original value. 

## Rules 
- only variables can be passed as arguments 
- place an ampersand (&) before a variable's name when you pass it as an argument

``` swift 
// in-out parameters
func swapName(_ firstName: inout String, _ lastName: inout String) {
    let temp = firstName
    firstName = lastName
    lastName = temp
}
var firstName = "Hayden"
var lastName = "Howell"
swapName(&firstName, &lastName)
print("First name is \(firstName). Last name is \(lastName).")
/* OUTPUT
 First name is Howell. Last name is Hayden.
*/
``` 

# References 
Apple. (2022). The Swift Programming Language (5.7 Edition).
