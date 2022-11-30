# How do you allocate memory on the free store? 

In C++, you allocate memory on the free store by using the **new** keyword. By using the new keyword **before the 
an object is declared**, the compiler becomes notified of the type of object you plan to allocate and how much memory will 
be required for such an object. 

## For instance: 
```cpp 
int* ptr; 
ptr = new int; 
// or 
int* ptr = new int; 
``` 


# References 
Jones, B., Libert, J., Rao, Siddhartha. (2008, January 1). *Sams Teach Yourself C++ in One Hour a Day* (6th ed.). Sams. <https://www.amazon.com/Sams-Teach-Yourself-One-Hour/dp/0672329417/ref=sr_1_4?crid=2RB86BRDXC98Z&keywords=sams+teach+yourself+c%2B%2B+in+one+hour+a+day&qid=1669771498&sprefix=sams+teach+yourself+c%2B%2B+in+one+hour+a+day+%2Caps%2C72&sr=8-4> 
