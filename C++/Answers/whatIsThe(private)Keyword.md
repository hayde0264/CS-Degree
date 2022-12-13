# What is the private keyword? 

The private keyword prevents code outside of a class from directly accessing data members. This is often called **encapsulation**. 


## For instance: 
```cpp 
//

#include "iostream"

using namespace std;

class Developer {
private:                    // NOTICE PRIVATE (all objects will not have direct access to name or age) 
    string name = "";
    int age = 0;
public:
    string getName();       
    void setName(string);
    int getAge();
    void setAge(int);
};

// member functions
string Developer::getName() {
    return name;
}
void Developer::setName(string name) {
    this->name = name;
}
int Developer::getAge() {
    return age;
}
void Developer::setAge(int age) {
    this->age = age;
}

int main() {
    Developer dev;
    dev.setAge(21);         // OK!
    dev.setName("Hayden");  // OK!
    
    
    cout << "DEVELOPER DATA\n"
    << "name: " << dev.getName() << endl
    << "age: " << dev.getAge() << endl;
}
/* OUTPUT
DEVELOPER DATA
name: Hayden
age: 21
*/

``` 

## Error Version: 
![Screen Shot 2022-12-12 at 7 11 45 PM](https://user-images.githubusercontent.com/109105989/207191633-dbf74f1a-0706-4659-acfe-4d6216ed8d9f.png)


# References 
Delamater, M. & Murach, J. (2022, April 22). *Murach's C++ Programming* (2nd ed.). Mike Murach & Associates. <https://www.amazon.com/Murachs-Programming-2nd-Joel-Murach/dp/1943872961/ref=sr_1_1?crid=3V9YBH7SU7MZC&keywords=murachs+c%2B%2B+programming&qid=1670888260&sprefix=murachs+c%2B%2B+programming%2Caps%2C76&sr=8-1>  
