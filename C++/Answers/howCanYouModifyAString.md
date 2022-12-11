# How can you modify a string? 

Since string literals are **constants**, so in order to modify a string, the **characters must be copied into an array**. 

## For example: 
```cpp 
#include <iostream>
#include <vector>  
 
 int main() {
  
  
        char hayden[] = "hayden";
        hayden[0] = 'Q';
 
        std::cout << hayden; // Prints - Qayden 
}                       
``` 

  

# References 
Stroustrup, B. (2000, February 11). *The C++ Programming Language* (3rd ed.). Addison-Wesley Professional. <https://www.amazon.com/Programming-Language-Special-3rd/dp/0201700735/ref=sr_1_1?crid=2LYS15FV29TAV&keywords=c%2B%2B+programming+third+edition&qid=1669162342&sprefix=c%2B%2B+programming+third+edition+%2Caps%2C72&sr=8-1> 
