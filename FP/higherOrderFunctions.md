# Higher-order Functions

*Higher-order functions* are functions that either accept 
other functions as arguements, or return functions as 
results. 

## Advantages? 
For example, many languages have higher order functions 
for sorting collections.  

### Most programming languages come with a build in sort method

## Java 
``` java 
class HigherOrderFunctions { 
    
    public void sortingCollections() { 
        List<String> arrayList = new ArrayList<>(); 
        arrayList.add("A"); 
        arrayList.add("B"); 
        arrayList.add("C");
        Collections.sort(arrayList, (a, b) -> { 
            return a.compareTo(b);
        });
    }
    
}
```
## Go  
``` go 


``` 
## Swift 
``` swift 
func descendNumbers() -> [Int] {
    let numbers = [5, 4, 3, 2, 1]
    let sortNumbers = { numbers.sorted { x, y in
        x < y
    }}
    return sortNumbers()
}
print(descendNumbers())		// PRINTS [1, 2, 3, 4, 5]
``` 
## Kotlin 
``` kotlin


```
# References 
Coosner, L. (2022, May 11). *Higher-order Functions in Java*. 
	Incus Data. <https://incusdata.com/blog/higher-order-functions-in-java> 

