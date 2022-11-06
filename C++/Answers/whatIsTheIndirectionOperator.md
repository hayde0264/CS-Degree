# What is the indirection operator? 

The * operator, sometimes called the **indirection operator or dereferencing operator**, returns an "alias or nickname" for the object in which **its pointer 
operand points**. 

## For instance: 
```cpp
#include <iostream> 
using namespace std; 

int main() { 
int a; 
int *aPtr 

*aPtr = &a

cout << *aPtr << endl; 
cout << a << endl; 
*aPtr = 3; 
cin >> *aPtr; 
} 


