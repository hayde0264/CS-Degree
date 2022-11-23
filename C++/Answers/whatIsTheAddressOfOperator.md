# What is the address-of operator? 

The address of an object can be referenced to with the ampersand (&) sign which create**references to objects**. So if they are updated, the object they are **referenced** to do as well. 


## For instance: 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  int main() {
          int i = 1;
          int& j = i;
  
          cout << "i = " << i << endl; // Prints - i = 1 
          // change j which changes i             
          j = 2;                                  
          cout << "i = " << i; // Prints - i = 2
  } 
```



  

# References 
Stroustrup, B. (2000, February 11). *The C++ Programming Language* (3rd ed.). Addison-Wesley Professional. <https://www.amazon.com/Programming-Language-Special-3rd/dp/0201700735/ref=sr_1_1?crid=2LYS15FV29TAV&keywords=c%2B%2B+programming+third+edition&qid=1669162342&sprefix=c%2B%2B+programming+third+edition+%2Caps%2C72&sr=8-1> 

