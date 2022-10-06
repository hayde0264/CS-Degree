# Binary Search

Class: **Search**

**BEST** - O(1) 

**WORST** - O(log N) 

**COMPLEXITY** - O(1) for iterative, O(log N) for recursive

*Binary Search* is a popular algorithm used to search 
for an element within a sorted array. 

## How does it work? 
Binary search implements a **divide and conquer** strategy 
to identify the key element position within an array. The algorithm 
compares the key element to the middle element within the array. 
If a match is found, it's position is returned. If the key element
is smaller than the middle element, the key **cannot be higher or 
on the right side** so these values are discarded. If the element 
is higher that the middle element, the key **cannot be lower or on the 
left side** of the middle element, so these values become discarded. This 
processes continues until the array returns the key value. 

### Steps:
- declare a key to search for within the array  
- initialize a constant that that will find the middleIndex of the array 
- if the value of the search key is equal to the middleIndex return such index 
- if the value of the search key is less than the middleIndex, disgard numbers greater than the middleIndex 
- if the value of the search key is greater than the middleIndex, disgard numbers less than the middleIndex
- continue until either the value is found or array is empty

![binary-search](https://user-images.githubusercontent.com/109105989/194418509-1742728e-071a-4afd-8861-d5250b7f4c0a.png)

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

