# What is the bitwise AND operator? 

The bitwise AND operator, denoted as (&), takes two operands and returns 1 if both integers contain 1; otherwise it returns 0; 

## Visually: 

![and](https://user-images.githubusercontent.com/109105989/207984903-98964974-44df-4d24-99b9-c3bc63dee9f7.png)


## For instance: 
```cpp 
//
//  test.cpp
//  play
//
//  Created by Hayden Howell on 12/11/22.
//
#include <iostream>
using namespace std;

int main() {
    int a = 1, b = 3;
    int c = 1;
    int d = 3;
    
    

    std::cout << "a = " << a << '\t' << "b = " << b << endl;
    std::cout << "a & b = " << (a & b) << endl;
    
    std::cout << "c = " << a << '\t' << "d = " << b << endl;
    std::cout << "c & d = " << (c & d) << endl;
    
    return 0;
}
/* OUTPUT
 a = 1    b = 3
 a & b = 1
 c = 1    d = 3
 c & d = 1
 Program ended with exit code: 0
 */
``` 

# References 
GeeksforGeeks. (2022). *Bitwise Operators in C/C++*. <https://www.geeksforgeeks.org/bitwise-operators-in-c-cpp/> 
