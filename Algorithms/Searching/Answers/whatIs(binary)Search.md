# What is binary search?



## In Java: 
```java 
  public class Test {
          public static int binarySearch(int[] arr, int key) {
                  int first = 0;
                  int last = arr.length - 1;
                  int middle;
                  while (first <= last) {
                          middle = 1 + (last - first) / 2;
                          if (arr[middle] == key) {
                                  return middle;
                          } if (arr[middle] < key) {
                                  last = middle + 1;
                          } else {
                                  last = middle - 1;
                          }
                  }
                  return -1;
          }
  
  
          public static void main(String[] args) {
                  int[] arr = {1, 2, 4, 2};
                  int key = 2;
  
                  int test = binarySearch(arr, key);
  
                  System.out.printf("%d\n", test); // Prints - 1
          }
  }
 ```
 ## In C++:
 ```cpp
  #include <cstddef>
  #include <iostream>
  #include <vector>
  
  using namespace std;
  
  static int binarySearch(vector<int> vec, int key) {
          int first = 0;
          int last = vec.size() - 1;
          int middle;
          while (first <= last) {
                  middle = 1 + (last - first) / 2;
                  if (vec[middle] == key) {
                          return middle;
                  } else if (vec[middle] < key) {
                          last = middle + 1;
                  } else {
                          last = middle - 1;
                  }
          }
          return -1;
  }
  
  
  int main() {
  
          vector<int> vec = {1, 2, 3, 4};
          int key = 3;
  
          int test = binarySearch(vec,  key);
  
          cout << test; // Prints - 2 
  
          return 0;
  }

``` 


 

