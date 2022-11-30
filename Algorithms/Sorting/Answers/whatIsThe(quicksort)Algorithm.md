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

