# What are Structure Bindings? 

Structure bindings give developers a convenient way to initialize multiple variables within a tuple, pair, or struct; and are 
commonly used to capture various return values. 


## For instance: 
```cpp 
#include "iostream"

struct Person {
    std::string name;
    int age;
};

int main() {
    Person hayden = {"Hayden", 21};
    
    auto[a, b] = hayden;
    
    std::cout << a << std::endl;
    std::cout << b << std::endl;
    return 0;
}
/* OUTPUT
 Hayden
 21
*/
``` 

# References 
Valeo, S. (2021). *C by Example*. <https://www.wbyexample.com> 
