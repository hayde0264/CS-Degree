# Search a sorted array for the first element greater than k 

Design an efficient algorithm that takes a sorted array and a key and finds the index of the first 
occurrence of the element greater than that key. 

**Solution** - iterate through the array from the smallest element onwards, returning when we first see an element larger than (k). If there is
no element return -1. 

**time** - O(log n) 
**space** - O(n)

## In C++: 
```cpp
  #include <vector>
  #include <iostream>
  using namespace std;
  
  int searchFirstLargerThanK(const vector<int>& arr, int key) {
          int low = 0;
          int high = arr.size() - 1;
          int result = -1;
          while (low <= high) {
                  int middle = low + ((high - low) / 2);
                  if (arr[middle] > key) {
                          result = middle;
                          high = middle - 1;
                  } else {
                          low = middle + 1;
                  }
          }
          return  result;
  }
  ``` 
  
  ## In Java: 
  ```cpp 
          public static int searchFirstGreaterThanK(List<Integer> arr, int key)   {
                  int low = 0;
                  int high = arr.size() - 1;
                  int result = -1;
                  while (low <= high) {
                          int middle = low + ((high - low) / 2);
                          if (arr.get(middle) > key) {
                                   result = middle;
                                   high = middle - 1;
                          } else {
                                  low = middle + 1;
                          }
                  }
                  return result;
          }
``` 

# References 
Aziz, A. Lee, T. Prakash, A. (2015). *Elements of Programming Interviews in Java* (1st ed.). <https://www.amazon.com/Elements-Programming-Interviews-Questions-Tsung-Hsien/dp/B00C7F0V3W/ref=sr_1_1?crid=SU7GU68QNL5N&keywords=elements+of+programming+interviews+in+java+1st+edition&qid=1669594847&sprefix=elements+of+programming+interviews+in+java+1st+edition+%2Caps%2C72&sr=8-1> 
