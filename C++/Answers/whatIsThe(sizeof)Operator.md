# What is the sizeof operator? 

The sizeof the operator returns **the size in bytes of its arguments**. 

```cpp 
  #include <iostream>
  
  
  using namespace std;
  
  
  int main() {
  
          long int some_array[3];
          char string[19];
  
          cout << sizeof(some_array) << endl; // Prints - 24
          cout << sizeof(string); // Prints - 19
  
          return 0;
  }
```






# References 
Oualline, S. (2003, January 1). *Practical C++ Programming* (2nd ed.). O'Reilly Media. <https://www.amazon.com/Practical-Programming-Second-Steve-Oualline/dp/0596004192/ref=sr_1_1?crid=YRU9QTDSQNLT&keywords=practical+c%2B%2B+programming&qid=1668720881&sprefix=%2Caps%2C56&sr=8-1>
