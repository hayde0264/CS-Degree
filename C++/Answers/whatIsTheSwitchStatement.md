# What is the switch statement? 


A switch statement is a form of control flow that matches values. Switch statements are generally more explicit than if/else statements and perform faster under the hood as well. 


## For instance: 
```cpp 
//  Created by Hayden Howell on 12/11/22.
//

#include "iostream"

int main() {
    char c = 'c';
    switch(c) {
        case 'a':
            std::cout << "" << std::endl;
            break;
        case 'b':
            std::cout << "b" << std::endl;
            break;
        case 'c':
            std::cout << "c" << std::endl;
        default:
            break;
    }
    return 0;
}
``` 


# References 
Valeo, S. (2021). *C by Example*. <https://www.wbyexample.com> 
