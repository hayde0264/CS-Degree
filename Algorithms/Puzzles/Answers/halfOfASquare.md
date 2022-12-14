# Half of a sqaure 


**Problem**: write a problem that uses only two output statements (cout << "#" && cout << "\n") to produce a pattern of hash symbols 
shaped like half of a perfect 5 x 5 square. 

## Instance: 
```cpp 
//
//  main.cpp
//  c++
//
//  Created by Hayden Howell on 12/11/22.
#include <iostream>
#include <thread>

void halfSquare() {
    for (int row = 1; row <= 5; row++) {
        for (int hashNum = 1; hashNum <= 5; hashNum++) {
            std::cout << "#";
        }
        std::cout << "\n";
    }
}
int main() {
    halfSquare();
}
/* OUTPUT
 #####
 #####
 #####
 #####
*/
``` 


# References 
Spraul, A. (2012). *Think Like a Programmer: An Introduction to Creative Problem Solving* (1st ed.). No Starch Press. <https://www.amazon.com/Think-Like-Programmer-Introduction-Creative/dp/1593274246/ref=sr_1_1?crid=2GTUCO5WRS6LU&keywords=think+like+a+programmer&qid=1670979747&sprefix=think+like+a+programme%2Caps%2C87&sr=8-1> 

