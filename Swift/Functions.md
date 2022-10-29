# Functions 

# Functions without parameters
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


# Functions with single parameter single output 
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


# Functions with multiple inputs single output 

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

# Functions with a single input and multiple outputs 

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


# Functions with variadic parameters 

```swift
// variatic inputs  
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


# Functions with in-out parameters 

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

