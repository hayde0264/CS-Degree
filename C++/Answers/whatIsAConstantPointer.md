# What is a constant pointer? 

Since pointers are used to access variables by their address, when **non constant**, pointers may **modify** the value pointed to. Constant 
pointers allow you **read** objects that are pointed to, but not **write** values. 

## For example: 
```cpp 
  #include <algorithm>
  #include <iostream>
  #include <iterator>
  #include <vector>
  
  using namespace std;
  
  
  
  int main() {
  
          int a;
          int b = 10;
  
          const int* ptr = &b;
          a = *ptr;        // ok: reading value at ptr 
>>        *ptr = 11;       // ERROR: read-only variable is not assignable   
>>        *ptr = b;        // ERROR: read-only variable is not assignable
                             
                                                                              
          cout << a; // Prints - 10                                           
  }   
``` 
