# Hello World


## For instance: 
```cpp 
//
//  main.cpp
//  c++
//
//  Created by Hayden Howell on 12/11/22.
#include <iostream>
#include <thread>                               // 1 

void hi() {                                     // 2 
    std::cout << "Hello concurrent world\n";
}
int main() {
    std::thread t(hi);                         // 3 
    t.join();                                  // 4 
}
/* OUTPUT
 Hello concurrent world
*/
``` 
# References 
Williams, A. (2012, February 28). *C++ Concurrency in Action: Practical Multithreading* (1st ed.). Manning. <https://www.amazon.com/C-Concurrency-Action-Practical-Multithreading/dp/1933988770/ref=sr_1_4?crid=3NVCEA9LYBTCT&keywords=c%2B%2B+concurrency+in+action&qid=1670978226&sprefix=c%2B%2B+concurrency+in+action%2Caps%2C79&sr=8-4> 
