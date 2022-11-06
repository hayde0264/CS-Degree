# What is an address operator? 

An address operator (**&**) is an operator that returns the **memory addres of its operand**. 

## For example: 
```cpp 
int a = 5; 
int *aPtr; 
aPtr = &a;
``` 

Above, (aPtr = &a), **assigns the address of the variable (a) to the pointer variable aPtr**. So, the variable aPtr is said to "**point to a**". At this point, aPtr **indirectly references variable a's value**. 

## Visually: 
![pointerToVar](https://user-images.githubusercontent.com/109105989/200148234-dafc5ced-455c-489d-8186-59c0323f6eaf.png)


# References 
Deital, H. & Deital, P. (2002, January 1). *C++ How to Program* (4th Edition). Prentice Hall. <https://www.amazon.com/How-Program-4th-Harvey-Deitel/dp/0130384747/ref=sr_1_1?crid=3HOMKOI48QV88&keywords=c%2B%2B+how+to+program+4th+edition&qid=1667671512&sprefix=c%2B%2B+how+to+program+4th+edition%2Caps%2C83&sr=8-1>   