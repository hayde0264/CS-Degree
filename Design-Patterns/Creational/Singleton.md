# Singleton Design Pattern

The **singleton pattern** is a creational design pattern that ensures that a class contains only a single instance while providing a global access point to this instance. 

## The good: 
- the singleton object is only initialized when it's requested for the first time. 

## The bad: 
- voilates the Single-Responsibilty principal
- instantiates tight coupling 
- requires special treatment in a multithreaded environment so that multiple threads won't create multiple singleton objects 
- is difficult to unit test 

## Steps to create: 
1. Add a private static field to the class for storing the singleton instance. 
2. Declare a public static creation method for getting the singleton instance. 
3. Implement "lazy initialization" inside the static method. It should create a new object on its first call and put it into the static field. The method should always return that instance on all subsequent calls. 
4. Make the constructor of the class private. The static method of the class will still be able to call the constructor but not the other objects. 
5. Go over the client code and replace all direct calls to the singleton's constructor will call to its static creation method. 

## Java 
``` java 
public class Singleton {
    // private STATIC field, which refers to the object 
    private static Singleton singleObject; 
    
    // PRIVATE constructor 
    private Singleton(){}
    
    public static Singleton getInstance() {
        // creates a single object 
        if (singleObject == null) {
            singleObject = new Singleton();
        }
        // returns the new object 
        return singleObject; 
    }
}
``` 



# References
*Java Singleton Class*. (2022). Programiz. <https://www.programiz.com/java-programming/singleton>  
*Singleton*. (2022). Refactoring Guru. <https://refactoring.guru/design-patterns/singleton> 
