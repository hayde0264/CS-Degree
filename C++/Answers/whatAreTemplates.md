# What are Templates? 

Templates give programmers the ability to create generic functions or classes. 


## For instance: 
```cpp 

#include "iostream"

template <class T>
T getSmaller(T n1, T n2) {
    return (n1 < n2) ? n1 : n2;
}


int main() {
    int a = 1;
    int b = 2;
    std::string c = "hayden";
    std::string d = "bill";
    
    std::cout << getSmaller(a, b) << std::endl;
    std::cout << getSmaller(c, d) << std:: endl;
    
    return 0;
}
``` 

# References 
Valeo, S. (2021). *C by Example*. <https://www.wbyexample.com> 


