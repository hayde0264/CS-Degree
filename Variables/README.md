# Variables

Variables provide developers with "named storage." Variables allow us to **manipulate values**, through **methods** and **operations**. 

## Visually:
![variable](https://user-images.githubusercontent.com/109105989/208266035-a824a593-6be8-41b3-be61-900206699812.jpg)


## Variables have:
- **specific types**
- **different bit sizes**
- **different operators**
- **different methods** 

## How should you name a variable? 
A variable name should be readable, memorable, and appropriate. A tip for creating a variable with this methodology is to state in words
what the variable represents. Remember that the best variables are as specific as possible and explain "what" rather than "how."  

## Use opposites when you can: 
- begin-end
- first-last 
- locked-unlocked
- min-max
- next-previous 
- old-new 


## In Java: 
```java 
public class main { 
  public static void main(String args) {  
    int z, y, z;         // declares three ints 
    int a = 1, b, c = 3; // declares three ints, but only initializes a && c 
    byte b = 22;         // initializes b 
    char s = 's';        // the variable s has the value of 's'
  } 
} 
``` 

## In C++: 
```cpp 
#include <iostream>
using namespace std;

int main ()
{
  // declare:
  int a, b;
  int test;

  // process:
  a = 1;
  b = 3;
  a += 5;
  test = a - b;

  // print:
  cout << result;

  // terminate:
  return 0;
}
``` 


# References
Lajolie, J., Lippman, S., Moo, B. (2005, January 1). *C++ Primer* (4th ed.). <https://www.amazon.com/Primer-4th-Stanley-B-Lippman/dp/0201721481/ref=sr_1_5?crid=3HV7DQMG8Y3SE&keywords=c%2B%2B+primer&qid=1668463798&sprefix=c%2B%2B+prime%2Caps%2C91&sr=8-5>

McConnell, S. (2004, July 7). *Code Complete: A Practical Handbook of Software Construction* (2nd ed.). Microsoft Press. <https://www.amazon.com/Code-Complete-Practical-Handbook-Construction/dp/0735619670/ref=sr_1_1?crid=3PEFNPHI3VMWN&keywords=code+complete+2&qid=1671310969&sprefix=code+complete+2%2Caps%2C91&sr=8-1> 

