# What is an array? 


An array is a collection of items that are stored within **contiguous** memory locations. You can retrieve elements within an 
array through indices (subscripting). 


## For instance: 
```cpp 

#include "iostream"
#include "array"

int main() {
    std::array<int, 10> some_array;
    
    for (int i = 0; i < some_array.size(); ++i) {
        some_array[i] = i;
    }
    
    std::cout << some_array[4] << std::endl;
    return 0;
}
/* OUTPUT
 4
*/
``` 

# References 
Valeo, S. (2021). *C by Example*. <https://www.wbyexample.com> 


