# Quick Sort 

Class: **Sorting Algorithm**

**BEST**: O(n log n) 

**WORST**: O(n^2) 

**SPACE**: O(n) 

The quick sort algorithm is an in-place sorting algorithm (an algorithm that places elements of a list into order). Quicksort is also defined as a divide-and-conquer algorithm.

## How does it work?
Quick sort selects a **pivot** element from an array 
and then partitions the remaining elements of such array 
into two sub-arrays, based on if the value is **greater 
than** or **less than** the pivot value. The sub-arrays 
are then sorted **recursively**. 

### Steps: 
- if the range has less than two elements, return immediately 
- otherwise, pick a value, or a **pivot**, that lies within the array 
- partition the array: by reordering its elements while keeping track 
  of a **point of division**. Having a point of division allows you to 
  determine if the element should come before the pivot (the element is 
  less than the pivot) or if the element should be placed after the pivot (element is greater than the pivot).  
- **recursively** apply the quicksort to the sub-ranges 
- repeat until the pivot element is the point of division.
  
 ![Quicksort](https://user-images.githubusercontent.com/109105989/194144386-e8bf46f6-7be3-4b9b-a2f7-99a3917f14a5.png)
  
## Java 
``` java 
public class QuickSort {

    static void swap(int[] array, int i, int j) {
        int temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }
    static int partition(int[] array, int low, int high) {
        int pivot = array[high];
        int i = (low - 1);
        for (int j = low; j <= high; j++) {
            if (array[j] < pivot) {
                i++;
                swap(array, i, j);
            }
        }
        swap(array, i + 1, high);
        return (i + 1);
    }
    static void quickSort(int[] array, int low, int high) {
        if (low < high) {
            int pi = partition(array, low, high);
            quickSort(array, low, pi - 1);
            quickSort(array, pi + 1, high);
        }
    }
    
}
``` 
## Go 
``` go 
func partition(array []int, low int, high int) ([]int, int) { 
        pivot := array[high] 
        i := low 
        for j := low; j < high; j++ { 
                if array[j] < pivot { 
                        array[i], array[j] = array[j], array[i] 
                        i++ 
                } 
        } 
        array[i], array[high] = array[high], array[i] 
        return array, i 
}
func quickSort(array []int, low int, high int) []int { 
        if low < high { 
                var p int 
                array, p = partition(array, low, high) 
                array = quickSort(array, low, p - 1) 
                array = quickSort(array, p + 1, high) 
        } 
        return array 
} 
``` 
## Swift 
``` swift 
func swap<T>(_ array: inout [T], _ i: Int, _ j: Int) {
    if i != j {
        array.swapAt(i, j)
    }
}
func partition<T: Comparable>(_ array: inout [T], _ low: Int, _ high: Int) -> Int? {
    let pivot = array[low]
    var i = low - 1
    var j = high + 1
    while true {
        repeat { j -= 1 } while array[j] < pivot
        repeat { i += 1 } while array[j] > pivot
        
        if i < j {
            array.swapAt(i, j)
        } else {
            return j
        }
    }
}
func quicksort<T: Comparable>(_ array: inout [T], _ low: Int, _ high: Int) {
    if low < high {
        let p = partition(&array, low, high)
        quicksort(&array, low, p)
        quicksort(&array, p + 1, high)
    }
}                                                                                                                                           
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
Wikipedia. (2022 20, September). *Quicksort*. <https://en.wikipedia.org/wiki/Quicksort> 

