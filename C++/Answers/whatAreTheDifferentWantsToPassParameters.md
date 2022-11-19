# What are the different ways to pass parameters? 

## You can pass parameters by: 
- **value** - Value is passed into the function and can be changed inside the function. **changes are not passed to the caller** 
- **constant value** - Value is passed into the function. **cannot be changed** 
- **reference** - Reference is passed to the function. **changes made to the parameter are reflected in the caller** 
- **constant reference** - Value cannot be changed in the function. **more efficient than constant call by value** 
- **array** Value is passed in and may be modified. **automatically turns arrays into reference parameters** 
- **address** Passes a pointer to an item. 

## For instance: 
```cpp 
  #include <iostream>                     
                                          
  using namespace std;                    
                                          
                                          
                                          
                                          
  int main() {                            
                                          
          void function1(int var);     	     // value
          void function2(const int var);  // constant value
          void function3(int &var);         // reference
          void function4(const int &var); // constant reference
          void function5(int array[]);    // array
          void function6(int *var);       // address
                                                    
                                                            
          return 0;                                         
  }                     
  ``` 
  
  

# References 
Oualline, S. (2003, January 1). *Practical C++ Programming* (2nd ed.). O'Reilly Media. <https://www.amazon.com/Practical-Programming-Second-Steve-Oualline/dp/0596004192/ref=sr_1_1?crid=YRU9QTDSQNLT&keywords=practical+c%2B%2B+programming&qid=1668720881&sprefix=%2Caps%2C56&sr=8-1>
