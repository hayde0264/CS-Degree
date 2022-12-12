# Map

The map method goes through each element of an array, 
applies a passed-in function to each element, and returns
a brand-new array with modified values.

### The .map() method is sometimes referenced as "apply-to-all" 

## Keep in mind
Since the .map() method updates each element 
in an array, if you have a huge collection 
of data, using a for loop may be better. 

![map](https://user-images.githubusercontent.com/109105989/194680143-304280df-4ec4-4745-a93a-c7c615970985.png)

## Java 
``` java 
public void makeNamesUppercase() {
   List<String> lowercasedNames = Arrays.asList("ben", "katy", "sussie", "robbie");
   Stream<Object> uppercaseNames = lowercasedNames.stream().map(names -> names.toUpperCase());
   System.out.println(uppercaseNames);
}            // PRINTS - ["BEN", "KATY", "SUSSIE", "ROBBIE"] 
```

## Swift 
``` swift
func makeNamesUppercased() {
   var lowercasedNames = ["ben", "katy", "susie", "robbie"]
   let uppercasedNames = lowercasedNames.map { name in
            name.uppercased()
   }
  print(uppercasedNames)
}         // PRINTS - ["BEN", "KATY", "SUSSIE", "ROBBIE"] 
``` 
## Kotlin 
``` kotlin
fun makeNamesUppercase() {
    var lowercasedNames = arrayListOf<String>("ben", "katy", "susie", "robbie")
    val uppercaseNames = lowercasedNames.map { name -> name.uppercase() }
    print(uppercaseNames)
}       // PRINTS - [BEN, KATY, SUSIE, ROBBIE] 
```
 
# References
Levkovsky, M. (2019, August 17). *The Holy Trinity of Functional Programming: Map, Filter, Reduce* DEV. <https://dev.to/mlevkov/the-holy-trinity-map-filter-and-reduce-381e> 

Wikipedia. (2022, January 30). *Map (higher-order function*. <https://en.wikipedia.org/wiki/Map_(higher-order_function> 

