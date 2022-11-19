# How can you find the sum of an array? 


```cpp 
  #include <iostream>
  
  using namespace std;
  
  int sumArray(int first, int last, int array[]) {
          if (first == last)
                  return (array[first]);
          else
                  return (array[first] + sumArray(first + 1, last, array));
  }
  
  int main() {
          int some_array[2] = {0, 1};
  
          cout << sumArray(0, 1, some_array); // Prints - 1
  
          return 0;
  }
``` 

# References 
Oualline, S. (2003, January 1). *Practical C++ Programming* (2nd ed.). O'Reilly Media. <https://www.amazon.com/Practical-Programming-Second-Steve-Oualline/dp/0596004192/ref=sr_1_1?crid=YRU9QTDSQNLT&keywords=practical+c%2B%2B+programming&qid=1668720881&sprefix=%2Caps%2C56&sr=8-1>
