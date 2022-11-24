# What is binary search?


## In C++ (with standard-library help) 
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



