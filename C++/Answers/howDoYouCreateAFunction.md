# How do you create a function? 

To make a function in C++, you must specify the **return type, the name of the function, and parameters** (if they take arguments). 

```cpp 
int returnInt(void); // prototype (can omit argument identifiers) 
int returnArguement(int); // prototype 
int addInts(int, int); // prototype 


int returnInt(void) { // initialization 
  return 4; 
}
int returnArgument(int a) { // initialization 
    return a; 
}
int addInts(int a, int b) { // initialization 
  return a + b; 
}

 ``` 
 

# References 
Eckel, B. (2000, March 25). *Thinking in C++* (2nd ed.). Prentice Hall. <https://www.amazon.com/Thinking-Vol-Introduction-Standard-2nd/dp/0139798099/ref=sr_1_1?crid=KXETJPHJO8MM&keywords=thinking+in+c%2B%2B&qid=1668559578&sprefix=thinking+in+c%2B%2B%2Caps%2C84&sr=8-1>
