# Defining Classes 

When you write software for OS X or iOS, most of your time is spent working with **objects**. 

Objects in Objective-C are **just like objects in other object-oriented programming languages**: they package their data with related behavior. 

An app is built as a large ecosystem of interconnected objects **that communicate with each other to solve specific problems**, such as displaying a visual interface, responding to user input, or storing information. For OS X or iOS development, **you don't need to create objects from scratch to solve every conceivable problem**; instead, you have a large library **of existing objects** available for your use, provided by Cocoa (for OS X) and Cocoa Touch (for iOS). 

Some of these objects are immediately usable, *such as basic data types like strings and numbers**, or user interface elements like **buttons** and **table views**. Some are designed for you to **customize and combine the objects provided by underlying frameworks** with your own objects to give your app its unique set of features and functionality. 

In object-oriented programming terms, an object **is an instance of a class**. Class contain interfaces **which describe the way you intend the class and its instantiated objects to be used**. This interface includes the **list of messages that the class can receive**, so you also need to provide the class implementation, **which contains the code to be executed in response to each message**. 


# Classes are Blueprints for Objects 
A class **describes the behavior and properties** common to any parituclar type of an object. For a string object (in Objective-C, this is an instance of the class NSSTring), the class **offers various ways to examine and convert the internal characters that it respresents**. Similaryly, the class used to decribe a number object (NSNumber) **offers functionality around an internal number value, such as converting that value to a different numeric type**. 

In the same way that multiple building constructed from the same blueprint are indentical in structure, **every instance of a classs shares the same properties and behavior as all other instances of that class**. Every **NSString** instance behaves in the same way, **regardless of the internal string of characters it holds**. 

Any particular object is designed to be used in specific ways. You might know that a string object represents some string of characters, **but you don't need toknow the exact internal mechanisms used to store those characters**. You don't need to know anything about the internal behavior used by the objects itself to work directly with its characters, **but you do need to know how you are expected to interact with the object**, perpahs to ask it for specific characters or request a new object in which all the original characters are converted to uppercase. 

In Objective-C, the class **interace specifies exactly how a given type of object is intended to be used by other objects**. In other words, it defines the public interface between instances of the class and the outside world. 

# Mutability Determines Whether A Represented Value Can Be Changed 
Some classes define objects that are **immutable** This means thatt the internal contents **must be set when an object is created, and cannot subseqnently be changed by other objects**. In Objective-C, all basic **NSString** and **NSNumber** objects are **immutable**. If you need to represent a differnt number, you must use a **new NSNumber instance**. 

Some immutable classes offer a **mutable version**. If you specifically need to change the contents of a string at runtime, for example by appending characters as they are received over a network connection, **you can use an instance of the NSMutableString class**. Instances of this class behave just like **NSString** objects, except that they also offer **functionality to change the characters that the object represents**. 

Although **NSString** and **NSMutableString** are different classes, they have many similarities. Rather than writing two completely seperate classes from scratch that just happen to have some similar behavior, **it makes sense to make use of inheritance**. 


# References 
Apple Inc. (2014). *Programming with Objective-C*. <https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/DefiningClasses/DefiningClasses.html#//apple_ref/doc/uid/TP40011210-CH3-SW1>


