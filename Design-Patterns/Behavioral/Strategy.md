# Strategy Pattern 

Class: **Behavioral** 

The strategy design pattern is a behavioral design pattern that enables the programmer to select an algorithm at run-time. Rather than use a single algorithm directly, objects can receive run-time instructions as to which algorithm to implement.

### Remember to program to interfaces, not implementations.

## How does it work? 
To adhere to the strategy pattern, behaviors of classes **should not** 
be inhereited. Instead, behaviors should be **encapsulated with interfaces**.
This references that open/closed principal, which states classes **should be 
open for extension but closed for modification**. The strategy pattern uses 
composition (has - a) instead of inheritance (is - a). 

### Steps 
- separate behaviors into different interfaces 
- create classes that implement the behaviors from the recently defined interfaces  
- create an abstract class that holds a reference to each interface 
- extend the abstract class with concrete examples that instantiate certain  behaviors  

![Strategy-Pattern](https://user-images.githubusercontent.com/109105989/194192512-b21efbe6-0343-45b5-bf0d-e1946e158c5a.png)

## Java 
``` java 

``` 
## Go 
``` go 

``` 
## Swift 
``` swift 

``` 
## Kotlin 
``` kotlin 

``` 

# References 
Wikipedia. (2022, August 26). *Strategy Pattern*. <https://en.wikipedia.org/wiki/Strategy_pattern> 

