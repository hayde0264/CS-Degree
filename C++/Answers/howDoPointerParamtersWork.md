# How do pointer parameters work? 

If a parameter is a pointer, the pointer is **copied**, just like all other **non-reference types**. So, if the 
the function is assigned a new pointer value, the calling pointer value **remains unchanged**. 


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
# References 
Lippman, S., Lajoie, J., Moo, B. (2005). *C++ Primer* (4th ed.). <https://www.amazon.com/C-primer-fourth-Stanley-Lippman-ebook/dp/B0BKLV6F72/ref=sr_1_4?crid=HOJ0F3EYMPPV&keywords=c%2B%2B+primer&qid=1668976869&sprefix=c%2B%2B+primer%2Caps%2C87&sr=8-4> 
