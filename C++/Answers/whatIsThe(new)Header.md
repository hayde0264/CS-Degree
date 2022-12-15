# What is the new header? 

The new header describes a function used to manage dynamic storage. 

## Functions: 
- **operator new** - allocates storage space 
- **operator new[]** - allocates storage space for an array 
- **operator delete** - deallocates storage space 
- **operator delete[]** - deallocates storage space for an array 
- **set_new_handler** - sets new handler function 
- **get_new_handler** - get new handler function 


## Types: 
- **nothrow_t** - nothrow type 
- **new_handler** - type of new handler function 
- **bad_alloc** - exception thrown on failure allocating memory 
- **bad_array_new_length** - exception on bad array length 

## Constanats: 
- **nothrow** - nothrow constant 


## For example: 
```cpp 
//
//  test.cpp
//  play
//
//  Created by Hayden Howell on 12/11/22.
//
#include <iostream>
#include <new>
using namespace std;

struct Class {
    int data[100];
    Class() {std::cout << "constructed [" << this << "]\n";}
};

int main() {
    std::cout << "1: ";
    Class* p1 = new Class;
    // allocated memory by calling operator new (sizeOf(Class))
    // then constructs an object at the newly acquired space
    
    
    std::cout << "2: ";
    Class* p2 = new (std::nothrow)Class;
    // allocates memory by calling operator new (sizeOf(Class), std::nothrow)
    // then constructs an object at the newly acquired space
    
    std::cout << "3: ";
    new (p2) Class;
    // does not allocate memory -- calls: operator new (sizeOf(Class), p2)
    // consturcts an object at p2
    
    std::cout << "4: ";
    Class* p3 = (Class*)::operator new(sizeof(Class));
    // allocates memory by calling: operator new (sizeOf(Class))
    // but does not call Class's constructor
    
    
    delete p1;
    delete p2;
    delete p3;
    
    
    
    return 0;
}
/* OUTPUT 
1: constructed [0x100504470]
2: constructed [0x100504600]
3: constructed [0x100504600]
4: Program ended with exit code: 0
```

# References 
cplusplus. (2022). *<new>*. <https://cplusplus.com/reference/new/> 



