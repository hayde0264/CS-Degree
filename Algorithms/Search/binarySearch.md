# Binary Search

Class: **Search**

**BEST** - O(1) 

**WORST** - O(log N) 

**COMPLEXITY** - O(1) for iterative, O(log N) for recursive

*Binary Search* is a popular algorithm used to search 
for an element within a sorted array. 

## How does it work? 
Binary search implements a divide-and-conquer strategy to identify the key element position within an array. The algorithm compares the key element to the middle index of the array. If a match is found, its position is returned. If the key element is smaller than the middle index, the key cannot be higher or on the right side, so these values are discarded. If the element is higher than the middle index, the key cannot be lower or on the left side, so these values become discarded. This process continues until the array returns the key value.

### Steps:
- create an array to search through and a key to search for 
- identify the lowest and highest value of the array 
- as long as the lower value is less than the highest value
- initialize a constant that will find the middle index of the array 
- if the value of the search key is equal to the middle index return, such index 
- if the value of the search key is less than the middle index, discard numbers greater than the middle index 
- if the value of the search key is greater than the middle index, discard numbers less than the middle index
- continue until either the value is found or the array is empty

![binary-search](https://user-images.githubusercontent.com/109105989/194418509-1742728e-071a-4afd-8861-d5250b7f4c0a.png)

## Java 
``` java 
public class BinarySearch {

    public static int binarySearch(int array[], int key) {
        int low = 0;
        int high = array.length - 1;
        while (low <= high) {
            int middle = low + (high - low) / 2;
            if (array[middle] == key) {
                return middle;
            } else if (array[middle] < key) {
                low = middle + 1;
            } else {
                high = middle - 1;
            }
        }
        return -1;
    }

}
``` 
## Go 
``` go 
func binarySearch(array []int, key int) int { 
        low := 0 
        high := len(array) - 1 
        for low <= high { 
                middle := low + (high - low) / 2 
                if array[middle] == key { 
                        return middle 
                } else if array[middle] < key { 
                        low = middle + 1 
                } else { 
                        high = middle - 1 
                } 
        } 
        return -1 
} 
``` 
## Swift 
``` swift 
func binarySearch<T: Comparable>(_ array: [T], key: T) -> Int? {
    var low = 0
    var high = array.count
    while low < high {
        let  mid = low + (high - low) / 2
        if array[mid] == key {
            return mid
        } else if array[mid] < key {
            low = mid + 1
        } else {
            high = mid
        }
    }
    return nil
}
``` 
## Kotlin 
``` kotlin 
fun binarySearch(array: IntArray, key: Int): Int { 
    var low = 0 
    var high = array.size - 1 
    while (low <= high) {
        val middle = low + (high - low) / 2 
        when { 
            array[middle] == key -> return middle
            array[middle] < key -> low = middle + 1 
            array[middle] > key -> high = middle - 1
        }
    }
    return -1
}
``` 

# References 
GeeksForGeeks. (2022, September 5). *Binary Search*. <https://www.geeksforgeeks.org/binary-search> 

Nirmitha, D. (n.d.). *Binary Search in Java*. Stack Abuse. <https://www.stackabuse.com/binary-search-in-java/> 

