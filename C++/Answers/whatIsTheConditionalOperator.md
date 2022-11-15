# What is the conditional operator? 

The conditional operator is the **ternary operator** of C++. This allows programmers to 
add simple **if-else** statements in an expression. 

## Syntax: 
```cpp 
condition ? expression1 : expression2; 
``` 

## For instance 
```cpp 
  #include <iostream>            
                                 
  using namespace std;           
                                 
  int main() {                   
          const string a = "string";
          const string b = "string";
          const string c = "not a string";
          const string differentString = "different string";
          const string sameString = "same string";
                                 
          string test1 = a == b ? sameString : differentString;
          string test2 = a == c ? sameString : differentString;
          string test3 = a == b ? "exact" : "different";
          string test4 = a == c ? "exact" : "different";
                                 
          cout << test1 << endl; // Prints - same string 
          cout << test2 << endl; // Prints - different string 
          cout << test3 << endl; // Prints - exact 
          cout << test4 << endl; // Prints - different
  }   
```

# References
Lajolie, J., Lippman, S., Moo, B. (2005, January 1). *C++ Primer* (4th ed.). <https://www.amazon.com/Primer-4th-Stanley-B-Lippman/dp/0201721481/ref=sr_1_5?crid=3HV7DQMG8Y3SE&keywords=c%2B%2B+primer&qid=1668463798&sprefix=c%2B%2B+prime%2Caps%2C91&sr=8-5>
