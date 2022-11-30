# What is the quicksort algorithm? 


## In C++: 
```cpp 
  #include <algorithm>
  #include <array>
  #include <cstddef>
  #include <string>
  #include <vector>
  #include <iostream>
  
  
  using namespace std;
  
  int partition(vector<int>&, size_t, size_t);
  void quickSort(vector<int>&, size_t, size_t);
  
  
  
  void quickSort(vector<int>& vec, size_t first, size_t last) {
          if (first < last) {
                  int pivot = partition(vec, first, last);
                  quickSort(vec, first, pivot);
                  quickSort(vec, pivot + 1, last);
          }
  }
  
  int partition(vector<int>& vec, size_t first, size_t last) {
          int x = vec[first];
          int i = first;
  
          for (size_t j = first; j < last; ++j) {
  
                  if (vec[j] <= x) {
                  ++i;
                  swap(vec[i], vec[j]);
                  }
          swap(vec[i], vec[j]);
          }
          return i;
  }
``` 

## In Java: 
```java 

void quickSort(int[] array, int left, int right) {
    int index = partition(array, left, right);
    if (left < index - 1) { // sort left half
           quickSort(array, left, index - 1);
     }
     if (index < right) { // sort right half
           quickSort(array, index, right);
     }
}
  
  
int partition(int[] array, int left, int right) {
     int pivot = array[(left + right) / 2];
     while (left <= right) {
            // find left element that should be moved right
            while (array[left] < pivot) left++;
            // find right element that should be moved left
            while (array[right] > pivot) right--;
  
            // swap
            if (left <= right) {
                 swap(array, left, right);
                 left++;
                 right--;
             }
      }
   return left;
 }
  
void swap(int[] array, int left, int right) {
      int temp = array[left];
      array[left] = array[right];
      array[right] = temp;
 }
  ```
  
  

