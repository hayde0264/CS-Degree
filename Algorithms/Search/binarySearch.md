# Binary Search

Class: **Search**

**BEST** - O(1) 

**WORST** - O(log N) 

**COMPLEXITY** - O(1) for iterative, O(log N) for recursive

*Binary Search* is a popular algorithm used to search 
for an element within a sorted array. Binary search 
implements a **divide and conquer** approach by comparing 
the target element with the middle element of the array. 

## How does it work? 


### Steps:
- declare a key to search for within the array  
- initialize a constant that that will find the middleIndex of the array 
- if the value of the search key is equal to the middleIndex return such index 
- if the value of the search key is less than the middleIndex, disgard numbers greater than the middleIndex 
- if the value of the search key is greater than the middleIndex, disgard numbers less than the middleIndex
- continue until either the value is found or array is empty

## Java 
``` java 
public class BinarySearch {

    public static int binarySearch(int array[], int key) {
        int low = 0;
        int high = array.length - 1;
        while (low <= high) {
            int middleIndex = low + (high - low) / 2;
            if (array[middleIndex] == key) {
                return middleIndex;
            } else if (array[middleIndex] < key) {
                low = middleIndex + 1;
            } else {
                high = middleIndex - 1;
            }
        }
        return -1;
    }

}
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
Nirmitha, D. (n.d.). *Binary Search in Java*. Stack Abuse. <https://www.stackabuse.com/binary-search-in-java/> 

