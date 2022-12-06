# What is pass by value? 

When passing by value, local copies are made within a function. These local copies are created but then **thrown away** when the function 
returns as its local storage becomes deallocated. 

## For instance: 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  
  void swap(int a, int b) {
          cout << "before swap" << '\t' << "a = " << a << " b = " << b << endl;
  
          int t = a;
          a = b;
          b = t;
  
          cout << "after swap" << '\t' << "a = " << a << " b = " << b << endl;
  }
  
  
  int main() {
  
          int a = 5;
          int b = 10;
  
  
          cout << "before swap" << '\t' << "a = " << a << " b = " << b << endl;
  
          swap(a, b);
  
          cout << "after swap" << '\t' << "a = " << a << " b = " << b << endl;
  
  
          return 0;
  
          /* OUTPUT
          before swap     a = 5 b = 10
          before swap     a = 5 b = 10
          after swap      a = 10 b = 5
          after swap      a = 5 b = 10
          */
  }
  ``` 
  
# References 
Jones, B., Libert, J., Rao, Siddhartha. (2008, January 1). *Sams Teach Yourself C++ in One Hour a Day* (6th ed.). Sams. <https://www.amazon.com/Sams-Teach-Yourself-One-Hour/dp/0672329417/ref=sr_1_4?crid=2RB86BRDXC98Z&keywords=sams+teach+yourself+c%2B%2B+in+one+hour+a+day&qid=1669771498&sprefix=sams+teach+yourself+c%2B%2B+in+one+hour+a+day+%2Caps%2C72&sr=8-4> 
