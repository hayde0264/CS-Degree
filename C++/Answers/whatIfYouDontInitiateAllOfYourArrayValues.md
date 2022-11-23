# What if you don't initiate all of your array values? 


If all of the elements within your array are not specified, the remaining elements are considered to be **0**. 

## For example: 
```cpp 
  #include <iostream>
  #include <vector>
  
  using namespace std;
  
  
  
  int main() {
  
        int ex1[4] = {1, 2};
        /* will be set to 
        int ex1[] = {1, 2, 0, 0};  
        */  
  }        
``` 

  
  

# References 
Stroustrup, B. (2000, February 11). *The C++ Programming Language* (3rd ed.). Addison-Wesley Professional. <https://www.amazon.com/Programming-Language-Special-3rd/dp/0201700735/ref=sr_1_1?crid=2LYS15FV29TAV&keywords=c%2B%2B+programming+third+edition&qid=1669162342&sprefix=c%2B%2B+programming+third+edition+%2Caps%2C72&sr=8-1> 
