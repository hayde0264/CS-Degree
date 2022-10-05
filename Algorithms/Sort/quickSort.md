# Quick Sort 

Class: Sorting Algorithm

**Best**: O(n log n) 
**Worst**: O(n^2) 
**Space**: O(n) 

The *quick sort* algorithm is **a in-place 
sorting algorithm** (an algorithm that places elements 
of a list into order). Quicksort is also defined 
as a *divide-and-conquer* algorithm. 

## How does it work?
Quick sort selects a **pivot** element from an array 
and then partitions the other elements of such array 
into two sub-arrays, based on if the value is **greater 
than** or **less than** the pivot value. The sub-arrays 
are then sorted **recursively**. 

### Steps: 
- If the range has less than two elements, return immediately 
- Otherwise pick a value, or a **pivot**, that lies within the array 
- Partition the range: by reordering its elements, while keeping track 
  of a **point of division**. Having a point of division allows you to 
  determine if the element should come before the pivot (element is 
  less than pivot), or if the element should be placed after the pivot (element 
  is greater than pivot).  
- **Recursively** apply the quicksort to the sub-range to the point of 
  divison and to the sub-range after it, possibly excluding from both ranges
  the element equal to the pivot at the point of division. 

## Java 
``` java 
``` 
## Swift 
``` swift 
``` 
## Go 
``` go 
``` 
## Kotlin
``` kotlin 

fun <T> Array<T>.swap(i: Int, j: Int) { 
    val temporary = this[i]
    this[i] = this[j]
    this[j] = temporary
}
fun <T: Comparable<T>> partition(array: Array<T>, low: Int, high: Int): Int { 
    var left = low
    var right = high
    val mid = (left + right) / 2 
    val pivot = array[mid]
    
    while (left <= right) {
        while (array[left] < pivot) {
            left++ 
        }
        while (array[right] > pivot) {
            right--
        }
        if (left <= right) {
            array.swap(left, right) 
            left++ 
            right-- 
        }
    }
    return left
}
fun <T: Comparable<T>> quickSort(array: Array<T>, low: Int, high: Int) { 
    if (low < high) {
        val pivot = partition(array, low, high)
        quickSort(array, low, high)
        quickSort(array, pivot, high)
    }
}
``` 

# References 
Wikipedia. (2022 20, September). *Quicksort* <https://en.wikipedia.org/wiki/Quicksort> 

