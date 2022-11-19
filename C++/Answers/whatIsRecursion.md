# What is recursion? 

Recursion is when a function **calls itself directly or indirectly**. 

## A function is recursive if: 
- **it has an ending point** 
- **it makes the problem simpler** 

## For instance 
```cpp 
  int sumArray(int first, int last, int array[]) {
          if (first == last)                  
                  return (array[first]);      
          else                                
                  return (array[first] = sumArray(first + 1, last, array));
  }                                           
                                              
                                              
  int main() {                                
          // instance
          int some_array[5] = {0, 1, 2, 3, 4};
                                              
          // driver
          cout << sumArray(0, 4, some_array); // Prints - 4
                            
  
          return 0;
  }
``` 

  
  

# References 
Oualline, S. (2003, January 1). *Practical C++ Programming* (2nd ed.). O'Reilly Media. <https://www.amazon.com/Practical-Programming-Second-Steve-Oualline/dp/0596004192/ref=sr_1_1?crid=YRU9QTDSQNLT&keywords=practical+c%2B%2B+programming&qid=1668720881&sprefix=%2Caps%2C56&sr=8-1>
