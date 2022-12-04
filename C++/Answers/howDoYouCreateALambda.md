# How do you create a lambda? 

Lambdas are prefixed with the **auto** keyword, have lambda introducers **([])**, which denote the start of a lambda, parameter lists **()**, and can even return types **(->)**. 


## For instance: 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  int main() {
  
          auto greeting = [] () { cout << "hello, world"; };
  
          greeting(); // Prints - hello, world
          return 0;
  
  }
  ```
  
  # References 
C++ Lambda. (2022). *Programiz*. <https://www.programiz.com/cpp-programming/lambda-expression> 
