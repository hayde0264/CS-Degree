# What is vector? 

An array, which must have **constant bounds**, is different from a vector. A vector uses **variable bounds**. 

## For instance: 
```cpp 
  #include <iostream>
  #include <vector>
  
  using namespace std;
  
  
  void vectorEx(int i) {
          /*
          int array1[i];
         
          This will create an error because the array size IS NOT a constant expression.         
          */                                                                                    
                                                                                                
                                                                                                
          vector<int> vectorEx(i); // this works!
  }      
  ``` 
  
  

# References 
Stroustrup, B. (2000, February 11). *The C++ Programming Language* (3rd ed.). Addison-Wesley Professional. <https://www.amazon.com/Programming-Language-Special-3rd/dp/0201700735/ref=sr_1_1?crid=2LYS15FV29TAV&keywords=c%2B%2B+programming+third+edition&qid=1669162342&sprefix=c%2B%2B+programming+third+edition+%2Caps%2C72&sr=8-1> 
