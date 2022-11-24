# How should you create function arguments? 

When creating function arguments, it's good practice to **avoid functions that modify their arguments**. A better practice 
is to return a value from the function **explicitly or require a pointer argument**. 

## For example: 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  int next(int a) { return a + 1; }
  void increment(int* b) { (*b)++; }
  
  int main() {
  
          int x = 10;
  
          // with a pointer argument
          increment(&x);
          cout << x << endl; // Prints - 11
  
          // explictly
          x = next(x);
          cout << x << endl; // Prints - 12
  
          return 0;
  }
  ```
  

  

# References 
Stroustrup, B. (2000, February 11). *The C++ Programming Language* (3rd ed.). Addison-Wesley Professional. <https://www.amazon.com/Programming-Language-Special-3rd/dp/0201700735/ref=sr_1_1?crid=2LYS15FV29TAV&keywords=c%2B%2B+programming+third+edition&qid=1669162342&sprefix=c%2B%2B+programming+third+edition+%2Caps%2C72&sr=8-1> 

  
