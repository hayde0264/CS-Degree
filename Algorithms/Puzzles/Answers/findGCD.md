# Find GCD 


## In C++: 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  
  
  int gcd(int v1, int v2) {
          while (v2) {
          int temp = v2;
          v2 = v1 % v2;
          v1 = temp;
          }
          return v1;
  }
  
  int main() {
  
          cout << gcd(1, 5) << endl; // Prints - 1
          cout << gcd(2, 10) << endl; // Prints - 2
          cout << gcd(30, 10); // Prints - 10
          return 0;
  }
``` 

# References 
Lippman, S., Lajoie, J., Moo, B. (2005). *C++ Primer* (4th ed.). <https://www.amazon.com/C-primer-fourth-Stanley-Lippman-ebook/dp/B0BKLV6F72/ref=sr_1_4?crid=HOJ0F3EYMPPV&keywords=c%2B%2B+primer&qid=1668976869&sprefix=c%2B%2B+primer%2Caps%2C87&sr=8-4> 
