# Type Casting

Type casting is a way **to check the type of an instance**or to **treat that instance as a different superclass or subclass** from somewhere else in its own class hierarchy. 

Type casting in Swift is implemented with the **is** and **as** operators. These two operators provide a simple and expressive way to **check the type of a value or cast a value to a different type**. 

## Defining a Class Hierarchy for Type Casting 
You can use type casting with a hierarchy of classes and subclasses **to check the type of a particular class instance and to cast that instance to another class within the same hierarchy**. 

The snippet below defines a new base called **MediaItem**. This class provides basic functionality for any kind of item that appears in a digital media library. Specifically, it **declares a name property of type String** and an **init name initializer**. 

``` Swift 
class MediaItem {
    var name: String
    
    init(name: String) {
        self.name = name
    }
}
``` 

The next snipped defines **two subclasses of MediaItem**. The first subclass, **Movie, will encapsulate additional information about a movie or film**. This class adds a **director** property on top of the base **MediaItem** class, with a corresponding initializer. 

The second subclass in the snippet, **Song**, adds an **artist** property and initializer on top of the base class. 

``` Swift 
class Movie: MediaItem {
    var director: String
    
    init(name: String, director: String) {
        self.director = director
        // notice the super.init()
        super.init(name: name)
    }
}
class Song: MediaItem {
    var artist: String
    
    init(name: String, artist: String) {
        self.artist = artist
        // notice the super.init()
        super.init(name: name)
    }
}
``` 

The final snippet creates a **constant array called library**, which contains two **Movie** instances and three **Song** instances. The type of the **library** array is inferred by initializing it with the contents of an array literal. Swift's type checker is able to **deduce that Movie and Song have a common superclass of MediaItem**, so it infers a type of [MediaItem] for the **library** array. 

``` Swift 
let library = [
    Movie(name: "Casablanca", director: "Michael Curtiz"),
    Movie(name: "Citizen Kane", director: "Orson"),
    Song(name: "Blue Suede Shoes", artist: "Elvis Presley"),
    Song(name: "The One And Only", artist: "Chesney Hawkes"),
    Song(name: "Never Gonna Give You UP", artist: "Rick Astley")
]
``` 

The items stored above in **library** are still **Movie** and **Song** instances behind the scenes. However, if you iterate over the content of this array, **the items you receive back are types as MediaItem**, and not Movie or Song. In order to work with them as their native type, **you need to check their type or downcast them to a different type**. 

## Checking 
type 
Use the **type check operator (is)** to check whether an instance is of a **certain subclass type**. The type check operator returns **true if the instance is of that subclasses type and false if it's not**. 

The example below defines two variables, **movieCount** and **songCount**, which count the number of **Movie** and **Song** instances in the **library** array. 

``` Swift
var movieCount = 0
var songCount = 0
let checkTypeOfLibraryArray = {
    for item in library {
        // notice the (is) keyword
        if item is Movie {
            // increase the movie count by 1
            movieCount += 1
        } else if item is Song {    // notice the (is) keyword
            // increase the song count by 1
            songCount += 1
        }
    }
    // output the results
    print("Media Library contains \(movieCount) movies and \(songCount) songs.")
}
checkTypeOfLibraryArray()  // Prints "Media LIbrary contains 2 movies and 3 songs."
``` 

## Downcasting 
A constant or variable of a certain class type may actually **refer to an instance of a subclass behind the scenes**. Where you believe this is the case, you can try to **downcast to the subclass type with a type cast operator (as? or as!)**. 

Because downcasting can fail, the typecast operator comes in two different forms. The conditional form, **as?** returns an **optional value** of the type you are trying to downcast too. The forced form, **as!**, attempts the downcast and **force-unwraps** the result as a single compound action. 

Use the conditional form of the type cast operator **as?** when you **aren't sure if the downcast will succeed**. This form of the operator will **always return an optional value, and the value will be nil if the downcast was not possible**. This enables you to check for a successful downcast. 

Use the forced form of the type cast operator **as!** only when **you are sure that the downcast will always succeed**. This form of the operator will trigger a runtime error if you try to downcast to an incorrect class type. 

The example below will iterate over each **MediaItem** in the **library** array and print an appropriate description for each item. To do this, it needs to access each item as a try **Movie** or **Song**, and not just as a **MediaItem**. This is necessary in order for it to be able to access the **director** or **artist** property of a **Movie** or **Song** for use in the description. 

In this example, each item in the array might be a **Move**, or it might be a **Song**. **You don't know in advance which actual class to use for each item**, that's why it's appropriate to use the condition form of the type cast operator **as?** to check the downcast each time through the loop. 

``` Swift 
// initializes a constant array of type [MediaItem]
let library = [
    Movie(name: "Casablanca", director: "Michael Curtiz"),
    Movie(name: "Citizen Kane", director: "Orson"),
    Song(name: "Blue Suede Shoes", artist: "Elvis Presley"),
    Song(name: "The One And Only", artist: "Chesney Hawkes"),
    Song(name: "Never Gonna Give You UP", artist: "Rick Astley")
]
// uses downcasting to access MediaItems subclasses (Movie, Song) 
let downCastLibraryArray = {
    // notice items role within the coming lines
    for item in library {
        // notice the conditional as?
        if let Movie = item as? Movie {
            print("Move: \(movie.name) Director: \(movie.director)")
        } else if let song = item as? Song {        // notice the conditional as?
            print("Song: \(song.name) Artist: \(song.artist)")
        }
    }
}
downCastLibraryArray()
/*  Output
 Media Library contains 2 movies and 3 songs.
 Move: Casablanca Director: Michael Curtiz
 Move: Citizen Kane Director: Orson
 Song: Blue Suede Shoes Artist: Elvis Presley
 Song: The One And Only Artist: Chesney Hawkes
 Song: Never Gonna Give You UP Artist: Rick Astley
 */
``` 

The example starts by trying to downcast the current **item** as a **Movie**. Because **item** is a **MediaItem** instance, it's possible that it **might actually be a Movie**; equally, it's also possible that it might be a **Song**or even just a base **MediaItem**. Because of this uncertainty, the **as?** form of the type cast operator **returns an optional value when attempting to downcast to a subclass type**. The result of **item as? Movie** is of type **Movie?**, or **"optional Movie"**. 

Downcasting to **Movie** fails when applied to the **Song** instances in the library array. To cope with this, the example above **uses optional binding to check whether the optional Movie actually contains a value**(that is, to find out whether the downcast succeeded). This optional binding is written **if let Movie = item as? Movie"**, which can be read as: 
> "Try to access **item** as a **Movie**. If this is successful, set a new temporary constant called **movie** to the value stores in the returned optional **Movie**" 

If the downcasting succeeds, the properties of **Movie** are then used to print a description for that **Movie** instance, including the name of its **director**. A Similar principle is used to check for **Song** instances and to print an appropriate description (including **artist** name) whenever a **Song** is found in the library. 

## Remember: 
> "Casting doesn't actually modify the instance or change its values. The underlying instance remains the same; it's simply treated and accessed as an instance of the type to which it has been cast."

# References 
Apple. (2022). *The Swift Programming Language* (5.7 Edition). 


