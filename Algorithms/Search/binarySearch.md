# Binary Search

Class: **Search**

**BEST** - O(1) 

**WORST** - O(log N) 

**COMPLEXITY** - O(1) for iterative, O(log N) for recursive

*Binary Search* begins by comparing an element in the middle 
of an array with the target (key) value. If the target value 
matches the element, its position with the array is returned. 
If the target value is **less than** the element, the search 
continues in the **lower half** of the array. If the target value 
is **greater tha** the element, the search continues in the **upper 
half** of the array.

## How does it work? 


### Steps:
- declare a key to search for within the array  
- initialize a constant that that will find the middleIndex of the array 
- if the value of the search key is equal to the middleIndex return such index 
- if the value of the search key is less than the middleIndex, disgard numbers greater than the middleIndex 
- if the value of the search key is greater than the middleIndex, disgard numbers less than the middleIndex
- continue until either the value is found or array is empty
- 

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
GeeksForGeeks. (2022, September 5). *Binary Search*. <https://www.geeksforgeeks.org/binary-search> 

