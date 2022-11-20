# How do pointer paramters work? 

If a paramter is a pointer, the pointer is **copied**, just like all other **nonreference types**. So, if the 
function assigned a new pointer value to a paramter, the calling pointer value **remains unchanged**. 


## For instance: 
```cpp 
  #include <iostream>
                                  
  using namespace std;            
                                  
  void reset(int *ptr) {    
          *ptr = 0; // will change the value of the OBJECT to which ptr points to
          ptr = 0;  // will change the LOCAL value of ptr, but argument is UNCHANGED
  }                               
                                  
                                  
  int main() {                    
                                  
          int i = 10;             
          int *ptr_to_i = &i;          
                                  
          cout << "i = " << *ptr_to_i << endl; // Prints - i = 10 
          reset(ptr);       
          cout << "i = " << *ptr_to_i; // Prints - i = 0
                                             
                                             
          return 0;                          
  } 
  ``` 
  
