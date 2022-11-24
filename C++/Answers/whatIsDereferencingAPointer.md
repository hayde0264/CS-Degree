# What is dereferencing a pointer? 

You can **dereference a pointer** by creating a type that holds the value of the pointer, which **dereferences it**. 

## For example: 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  
  int main() {
  
          int one = 1;
          int* ptr = &one;
          int oneExtra = *ptr;
  
          cout << "ptr: " << ptr << endl; // Prints - ptr: 0x16b8d782c
          cout << "*ptr: " << *ptr << endl; // Prints - *ptr: 1
          cout << "oneExtra: " << oneExtra; // Prints - oneExtra: 1
  }
``` 


# References 
Stroustrup, B. (2000, February 11). *The C++ Programming Language* (3rd ed.). Addison-Wesley Professional. <https://www.amazon.com/Programming-Language-Special-3rd/dp/0201700735/ref=sr_1_1?crid=2LYS15FV29TAV&keywords=c%2B%2B+programming+third+edition&qid=1669162342&sprefix=c%2B%2B+programming+third+edition+%2Caps%2C72&sr=8-1> 
