# What is an overloaded function? 

An overloaded function references creating two or more functions that same the **same** name but **different** parameter lists. 


## For instance: 
```cpp 
//
//  main.cpp
//  c++
//
//  Created by Hayden Howell on 12/11/22.
#include <iostream>
using  namespace std;

void print(int i) {
  cout << i << endl;
}
void print(double  f) {
  cout << f << endl;
}


int main(void) {

    print(1);
    print(2.11);

    return 0;
}
``` 



# References

Delamater, M. & Murach, J. (2022, April 22). *Murach's C++ Programming* (2nd ed.). Mike Murach & Associates. <https://www.amazon.com/Murachs-Programming-2nd-Joel-Murach/dp/1943872961/ref=sr_1_1?crid=3V9YBH7SU7MZC&keywords=murachs+c%2B%2B+programming&qid=1670888260&sprefix=murachs+c%2B%2B+programming%2Caps%2C76&sr=8-1>  
