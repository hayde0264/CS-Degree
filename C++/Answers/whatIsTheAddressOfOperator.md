
  # What is the address-of operator? 

The address-of operator **(&)** will **return the address of an element as it's stored in memory**. To use the address-of operator, prefix an identifier 
name with **"&"**, this will notify the compiler. 

```cpp 
  #include <iostream>
  #include <string>
  #include <vector>
  
  
  using namespace std;
  
  
  int main() {
  
          int a = 1;
          long b = 7658978;
          bool c = true;
  
  
  
          cout << "a: " << &a << "\n"; // Prints - a: 0x16eec7698
          cout << "b: " << &b << "\n"; // Prints - b: 0x16eec7690
          cout << "c: " << &c; // Prints - c: 0x16eec768
                                          
          return 0;            
  } 
  ``` 
  
  ## Visually: 
  ![memAddress](https://user-images.githubusercontent.com/109105989/203900052-410a403f-db03-42fd-8fa0-48c1bb9483a7.png)

  
  
# References 
Eckel, B. (2000, March 25). *Thinking in C++* (2nd. ed). Prentice Hall. <https://www.amazon.com/Thinking-Vol-Introduction-Standard-2nd/dp/0139798099/ref=sr_1_1?crid=OG7ZT44E93J4&keywords=thinking+in+c%2B%2B&qid=1668919926&sprefix=thinking+in+c%2B%2B%2Caps%2C86&sr=8-1>
