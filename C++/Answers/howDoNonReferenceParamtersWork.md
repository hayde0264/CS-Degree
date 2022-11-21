# How do nonreference parameters work? 

Plain parameters or **nonreference parameters** are initialized by **copying their corresponding arguments**. This means changes made 
to the **parameter(s) are local copies**, so once the function terminates **they do as well**. 


## For instance: 
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
  
  
          cout << gcd(20, 25) << endl; // Prints - 5 (Termines so v1 && v2 == 0)
          cout << gcd(10, 2) << endl; // Prints - 10 (Termines so v1 && v2 == 0)
          cout << gcd(1, 2); // Prints - 1 (Termines so v1 && v2 ==0)
          return 0;
  }
  ``` 

# References 
Lippman, S., Lajoie, J., Moo, B. (2005). *C++ Primer* (4th ed.). <https://www.amazon.com/C-primer-fourth-Stanley-Lippman-ebook/dp/B0BKLV6F72/ref=sr_1_4?crid=HOJ0F3EYMPPV&keywords=c%2B%2B+primer&qid=1668976869&sprefix=c%2B%2B+primer%2Caps%2C87&sr=8-4> 
  
