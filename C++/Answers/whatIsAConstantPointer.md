# What is a constant pointer? 

Since pointers are used to access variables by their address, when **non-constant**, pointers may **modify** the value pointed to. Constant 
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

## Example explanation: 
Here ptr points to a variable. However, the pointer (since it's constant) will **read the value pointed to** but cannot **change the value**. In this 
example the type of (&b), respectively, is **(int*)**, but is assigned to a pointer of **(const int*)**. Something to note here is a **pointer to a non-const** can implicitly convert **pointer to a constant**; however, **pointers to const** are not implicitly convertible to **pointers to non-const**. 

## Visually: 

![pointerEx](https://user-images.githubusercontent.com/109105989/203875139-55d35463-8ab7-418a-8f3b-25403621f380.png)


# References 
Reference. (2022). *cplusplus*. <https://cplusplus.com/reference> 
