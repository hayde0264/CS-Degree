# What are Lambda Expressions? 


Lambda expressions or lambda functions give developers a simplified notation for defining and using 
anonymous functions, which can capture variables located within scope. 

## For instance: 
```cpp 
#include "iostream"

int main() {
    
    int a = 1;
    auto add = [&a](int b) -> int {
        return a + b;
    };
    
    std::cout << add(2) << std::endl;
    std::cout << add(4) << std::endl;
    return 0;
}
/* OUTPUT
 3
 5
 */
``` 


# References 
Valeo, S. (2021). *C by Example*. <https://www.wbyexample.com> 
