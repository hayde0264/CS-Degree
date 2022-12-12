# What is a structure? 

A structure is a blueprint from which objects are instantiated. 


## How are structures different from classes? 
Structures are different from classes because structures, by default, provide public members.  


## Creating A Structure: 
```cpp 
#include "iostream"

using namespace std;

// creating structure 
struct Developer {
    string name = "";
    int age = 0;
    bool equals(const Developer&);
};
``` 

## Instantiating an Object: 
```cpp 

int main() {
    Developer dev;
    dev.name = "Hayden";
    dev.age = 21;
    
    cout << "DEVELOPER DATA\n"
    << "name: " << dev.name << endl
    << "age: " << dev.age << endl;
    
    return 0;
}
/* OUTPUT:
 DEVELOPER DATA
 name: Hayden
 age: 21
*/
``` 

# References 
Delamater, M. & Murach, J. (2022, April 22). *Murach's C++ Programming* (2nd ed.). Mike Murach & Associates. <https://www.amazon.com/Murachs-Programming-2nd-Joel-Murach/dp/1943872961/ref=sr_1_1?crid=3V9YBH7SU7MZC&keywords=murachs+c%2B%2B+programming&qid=1670888260&sprefix=murachs+c%2B%2B+programming%2Caps%2C76&sr=8-1>  
