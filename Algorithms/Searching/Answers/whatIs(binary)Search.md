# What is binary search?


## In C++ (with standard-library help): 
```cpp 
  #include <algorithm>
  #include <iostream>
  #include <iterator>
  #include <vector>
  
  using namespace std;
  
  
            
  int main() {
  
          int arrayInts[] = {1, 2, 1, 45, 15};
          vector<int> v(arrayInts, arrayInts + 5);
  
          // must sort
          sort(v.begin(), v.end());
  
  
  
          // search for 45
          const char* result = binary_search(v.begin(), v.end(), 45) ? "found" : "not found";
          cout << result << "\n"; // Prints - found                                               
                 
          // search for 4        
          const char* result2 = binary_search(v.begin(), v.end(), 4) ? "found" : "not found";                                
          cout << result2; // Prints - not found                                                                             
  } 
``` 

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
 
 

