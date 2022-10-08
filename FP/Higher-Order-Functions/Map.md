# Map

The *map* method goes through each element 
of an array and applies a **passed in** function 
to each element, and finally will return a brand 
new array with modified values. 

### The .map() method is sometimes referenced as "apply-to-all" 

## Keep in mind
Since the .map() method updates each element 
in an array, if you have a huge collection 
of data, using a for loop may be better. 

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
fun makeNamesUppercase() {
    var lowercasedNames = arrayListOf<String>("ben", "katy", "susie", "robbie")
    val uppercaseNames = lowercasedNames.map { name -> name.uppercase() }
    print(uppercaseNames)
}           // PRINTS - [BEN, KATY, SUSIE, ROBBIE] 
```
 
# References
Levkovsky, M. (2019, August 17). *The Holy Trinity of Functional Programming: Map, Filter, Reduce* DEV. <https://dev.to/mlevkov/the-holy-trinity-map-filter-and-reduce-381e> 
Wikipedia. (2022, January 30). *Map (higher-order function*. <https://en.wikipedia.org/wiki/Map_(higher-order_function> 

