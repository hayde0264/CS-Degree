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
~       
```


