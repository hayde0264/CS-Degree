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
  
  
  using namespace std;
  
  
  
  
  static int binarySearch(int arr[], int key) {
          int first = 0;
          int last = sizeof(*arr);
          int middle;
          while (first <= last) {
          middle = 1 + (last - first) / 2;
          if (arr[middle] == key) {
                  return middle;
          } else if (arr[middle] < key) {
                  last = middle + 1;
  
          } else {
          last = middle - 1;
          }
          }
          return -1;
  }
  
  
  int main() {
  
          int arr[] = {1, 2, 3, 4};
          int key = 2;
  
          int test = binarySearch(arr, key);
  
          cout << test; // Prints - 1
  
          return 0;
  }
``` 


 

