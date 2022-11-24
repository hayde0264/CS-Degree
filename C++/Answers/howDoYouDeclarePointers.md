# How do you declare a pointer? 
Pointers hold the addresses of objects. You can initialize a pointer with the **"asterisk"** and an **rval that has the (&) address of operator** 

```cpp 
char* ptr1; // pointer to an char  
int** ptr2; // pointer to a pointer to int 
int* arrayOfPointers[20]; // array of 20 pointers to ints 
int (*functionparameter) (char*) // pointer to a function taking a char* argument; returns an int 
int* f (char*); // function taking a char* argument; returns a pointer to an int;  
``` 


# References 
Deital, H. & Deital, P. (2002, January 1). *C++ How to Program* (4th Edition). Prentice Hall. <https://www.amazon.com/How-Program-4th-Harvey-Deitel/dp/0130384747/ref=sr_1_1?crid=3HOMKOI48QV88&keywords=c%2B%2B+how+to+program+4th+edition&qid=1667671512&sprefix=c%2B%2B+how+to+program+4th+edition%2Caps%2C83&sr=8-1>   

Stroustrup, B. (2000, February 11). *The C++ Programming Language* (3rd ed.). Addison-Wesley Professional. <https://www.amazon.com/Programming-Language-Special-3rd/dp/0201700735/ref=sr_1_1?crid=2LYS15FV29TAV&keywords=c%2B%2B+programming+third+edition&qid=1669162342&sprefix=c%2B%2B+programming+third+edition+%2Caps%2C72&sr=8-1> 
