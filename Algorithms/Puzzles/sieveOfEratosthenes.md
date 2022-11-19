# Sieve of Eratosthenes 

```cpp 
  # include <iostream>
  
  using namespace std;
  
  const int FINAL = 1000;
  
  int main() {
          int i;
          int j;
          int a[FINAL+1];
  
          // 1
          for (a[1] = 0, i = 2; i <= FINAL; i++)
                  a[i] = 1;
  
          // 2
          for (i = 2; i <= FINAL/2; i++)
                  for (j = 2; j <= FINAL/i; j++)
                          a[i*j] = 0;
  
          // 3
          for (i = 1; i <= FINAL; i++)
  
          // driver
          a[i] ? cout << i << " ": cout << "";
  }
``` 


# References 
Sedgewick, R. (1992). *Algorithms in C++*. Addison-Wesley. <https://www.amazon.com/Algorithms-C-Robert-Sedgewick/dp/0201510596/ref=sr_1_3?crid=1937U0Z5AW4O9&keywords=algorithms+in+c%2B%2B+sedgewick&qid=1668897598&sprefix=algorithms+in+c%2B%2B++%2Caps%2C66&sr=8-3>
