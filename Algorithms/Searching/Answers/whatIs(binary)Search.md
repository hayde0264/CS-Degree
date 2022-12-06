# What is binary search?



## In Java: 
```java 
             public static int binarySearch(List<Integer> arr, int key) {
                  int low = 0;
                  int high = arr.size() - 1;
                  int result = -1;
                  while (low <= high) {
                          int middle = low + ((high - low) / 2);
                          if (arr.get(middle) == key) {
                                  return middle;
                          } else if (arr.get(middle) < key) {
                                  low = middle + 1;
                          } else {
                                  high = middle - 1;
                          }
                  }
                  return result;
          }
 ```
 ## In C++:
 ```cpp
  #include <vector>
  #include <iostream>
  using namespace std;
  
  static int binarySearch(const vector<int>& arr, int key) {
          int low = 0;
          int high = arr.size() - 1;
          int result = -1;
          while (low <= high) {
                  int middle = low + ((high - low) / 2);
                  if (arr[middle] == key) {
                          return middle;
                  } else if (arr[middle] < key) {
                          low = middle + 1;
                  } else {
                          high = middle - 1;
                  }
          }
          return result;
  }
``` 


 

