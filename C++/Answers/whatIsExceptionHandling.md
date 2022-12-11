# What is Exception Handling? 

Exception handling is a solution to runtime errors. Exception handling 
handles errors by delegating control to another part of the program. 

## For instance: 
```cpp 
#include "iostream"

double divide(double dividend, double divisor) {
    if (divisor == 0) {
        throw "Cannot divide by 0\n";
    }
    return dividend / divisor;
}

int main() {
    try {
        std::cout << divide(5, 0) << std::endl;
    } catch (const char* err) {
        std::cout << err << std::endl;
    }
    
    return 0;
}
``` 


# References 
Valeo, S. (2021). *C by Example*. <https://www.wbyexample.com> 
