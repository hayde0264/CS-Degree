# What is linear search? 


## In C++:
```cpp 
  #include <cstddef>
  #include <iostream>
  #include <vector>
  
  
  using namespace std;
  
  
  
  static int linearSearch(vector<int> vec, int key) {
          for (int i = 0; i < vec.size() ; i++) {
                  if (vec[i] == key)
                          return i;
          }
          return -1;
  }
  
  
  int main() {
  
          vector<int> vec = {1, 2, 3, 4};
          int key = 4;
  
          int test = linearSearch(vec, key);
  
          test != -1 ? cout << "element located at index " << test : cout << "element not found"; // Prints - element located at index 3  
                                                                                                                                
          return 0;                                                                                                                             
  }                                                                                                                                                   
```

## In Java: 
```java 
  public class Test {
  
          public static int linearSearch(int arr[], int key) {
                  for (int i = 0; i < arr.length; i++) {
                          if (arr[i] == key) {
                                  return i;
                          }
                  }
                  return -1;
          }
  
          public static void main(String[] args) {
                  int arr[] = {1, 2, 3, 4};
                  int key = 2;
                  int implementation = linearSearch(arr, key);
                  String getResult = implementation == -1 ? "element not exsistent" : "element located at index " + implementation;
                                                                                                         
                  System.out.printf("%s", getResult); // Prints - element located at index 1
                                                                                    
          }                                                                                             
  } 
``` 

