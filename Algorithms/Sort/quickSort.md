# Quick Sort 

Class: **Sorting Algorithm**

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
  
  <img align="center" src="https://user-images.githubusercontent.com/109105989/194144386-e8bf46f6-7be3-4b9b-a2f7-99a3917f14a5.png">

  
## Java 
``` java 
public class QuickSort {

    private int partition(int[] array, int lo, int hi) {
        int pivot = array[hi];
        int i = (lo - 1);
        for (int j = lo; j < hi; j++) {
            if (array[j] <= pivot) {
                i++;

                int swapTemp = array[i];
                array[i] = array[hi];
                array[hi] = swapTemp;
            }
        }
        int swapTemp = array[i + 1];
        array[i + 1] = array[hi];
        array[hi] = swapTemp;
        return i + 1;
    }
    
    public void quickSort(int[] array, int lo, int hi) {
        if (lo < hi) {
            int partition = partition(array, lo, hi);
            quickSort(array, lo, partition - 1);
            quickSort(array, partition + 1, hi);
        }
    } 
    
}
``` 
## Swift 
``` swift 
func swap<T: Comparable>(_ leftValue: inout T, _ rightValue: inout T) {
    (leftValue, rightValue) = (rightValue, leftValue)
}

func partition<T: Comparable>(_ array: inout [T], _ low: Int, _ high: Int) -> Int {
    let pivot = array[low]
    var i = low - 1
    var j = high + 1

    while true {
        repeat { j -= 1 } while a[j] > pivot
        repeat { i += 1 } while a[i] < pivot

        if i < j {
            a.swap(i, j)
        } else {
            return j
        }
    }
}

func quickSort<T: Comparable>(_ array: inout [T], _ low: Int, _ high: Int) {
    if low < high {
        let p = partition(&array, low, high)
        quickSort(&array, low, p - 1)
        quickSort(&array, p + 1, high)
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

