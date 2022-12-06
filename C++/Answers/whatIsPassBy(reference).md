# What is pass by reference? 

**with pointers** - if you pass in a pointer as an argument, you pass in the **address of** an object, so within the function, you
can manipulate the value at such address. You can access such values by **dereferencing the pointer(s)**. 

**with references** - you can also pass arguments as references, but with the address of operator **(&)**  **, there's no need to dereference pointers**. 

## For exmaple (with pointers): 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  
  void swap(int* a, int* b) {
          cout << "before swap" << '\t' << "a = " << *a << " b = " << *b << endl;
  
          int t = *a;
          *a = *b;
          *b = t;
  
          cout << "after swap" << '\t' << "a = " << *a << " b = " << *b << endl;
  }
  
  
  int main() {
  
          int a = 5;
          int b = 10;
  
  
          cout << "before swap" << '\t' << "a = " << a << " b = " << b << endl;
  
          swap(&a, &b);
  
          cout << "after swap" << '\t' << "a = " << a << " b = " << b << endl;
  
  
          return 0;
  
          /* OUTPUT
          before swap     a = 5 b = 10
          before swap     a = 5 b = 10
          after swap      a = 10 b = 5
          after swap      a = 10 b = 5 // notice swap exist after function deallocation!  
          */                                               
  }
``` 

## For example (with references): 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  
  void swap(int& a, int& b) {
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
          after swap      a = 10 b = 5 // notice swap exists after function deallocation (and how much cleaner compared to passing by pointer)!
          */                                                                                                                        
  }                                                                                                                          
 ``` 
 
 


# References 
Jones, B., Libert, J., Rao, Siddhartha. (2008, January 1). *Sams Teach Yourself C++ in One Hour a Day* (6th ed.). Sams. <https://www.amazon.com/Sams-Teach-Yourself-One-Hour/dp/0672329417/ref=sr_1_4?crid=2RB86BRDXC98Z&keywords=sams+teach+yourself+c%2B%2B+in+one+hour+a+day&qid=1669771498&sprefix=sams+teach+yourself+c%2B%2B+in+one+hour+a+day+%2Caps%2C72&sr=8-4> 
 
 
