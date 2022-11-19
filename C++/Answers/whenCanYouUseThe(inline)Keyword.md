# When can you use the inline keyword? 

You can use the inline keyword when **a function is small**. This keyword tells the C++ compiler **" this code is small and simple**. The compiler 
can put the code into a **code stream** instead of generating a call to the function. 

## For instance: 
```cpp
  inline int add(int value1, int value2) {
          return (value1 + value2);
  }
  
  int main() {
  
          cout << add(2, 5); // Prints - 7
                             
          return 0;          
  }   
``` 

# References 
Oualline, S. (2003, January 1). *Practical C++ Programming* (2nd ed.). O'Reilly Media. <https://www.amazon.com/Practical-Programming-Second-Steve-Oualline/dp/0596004192/ref=sr_1_1?crid=YRU9QTDSQNLT&keywords=practical+c%2B%2B+programming&qid=1668720881&sprefix=%2Caps%2C56&sr=8-1>
