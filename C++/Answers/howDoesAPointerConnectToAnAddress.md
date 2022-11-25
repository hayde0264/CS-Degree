# How does a pointer connect to an address? 

An address operator (**&**) is an operator that returns the **memory address of its operand**. 

## For example: 
```cpp 
  #include <iostream>
  #include <string>
  #include <vector>
  
  
  using namespace std;
  
  
  int main() {
  
          int a = 4;
          int* ptr = &a;
  
          cout << ptr << endl; // Prints - "the address of a" (0x16f953698)
          cout << &a << endl; // Prints - (0x16f953698) notice its the same as (ptr)
          cout << *ptr; // Prints - "the value stored in variable a" (4)
  
          return 0;
  }
``` 

Above, (*ptr = &a), **assigns the address of the variable (a) to the pointer variable ptr**. So, the variable ptr is said to "**point to the address of a**." If the dereference the pointer (*ptr), "the value of the address of a will be rendered" notice (*ptr) prints 4. 

## Visually: 

![pointer](https://user-images.githubusercontent.com/109105989/201821431-127d1a97-e8ce-46b8-92f5-e12828b7d6bd.png)


  
# References 
Eckel, B. (2000, March 25). *Thinking in C++* (2nd. ed). Prentice Hall. <https://www.amazon.com/Thinking-Vol-Introduction-Standard-2nd/dp/0139798099/ref=sr_1_1?crid=OG7ZT44E93J4&keywords=thinking+in+c%2B%2B&qid=1668919926&sprefix=thinking+in+c%2B%2B%2Caps%2C86&sr=8-1>

