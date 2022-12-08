# What is bubble sort? 


**time** - O(n * n) 
**space** - O(1) 

## In C++: 
```cpp 
  #include <iostream>    
  #include <vector>      
                         
  using namespace std;   
                         
  void bubbleSort(vector<int>& vec) {
          for (size_t i = 0; i < vec.size() - 1; ++i) {
                  for (size_t j = 0; j < vec.size() - 1; ++j) {
                          if (vec.at(j) > vec.at(j + 1)) {
                                  swap(vec.at(j), vec.at(j + 1));
                          }
                  }      
          }              
  }    
``` 

## In Java: 
```java 
  import java.util.ArrayList;
⚠ import java.util.Arrays;
  import java.util.Collections;
  import java.util.List;
  
  public class Test {
          public static void bubbleSort(List<Integer> arr) {
                  for (int i = 0; i < arr.size() - 1; i++) {
                          for (int j = 0; j < arr.size() - 1; j++) {
                                  if (arr.get(j) > arr.get(j + 1)) {
                                          Collections.swap(arr, j, j + 1);
                                  }
                          }
                  }
          }
  
  }
```

