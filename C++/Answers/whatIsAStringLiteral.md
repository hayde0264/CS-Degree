# What is a string literal? 

A string literal is a character sequence that lies between quotes. The type of a string liter is **constant char**. Which means 
you're not allowed to modify a string literal **through a pointer**. 


## For example: 
  #include <iostream>
  
  
  
  int main() {
  
        char* literal = "I'm a string literal"; 
  
        /* 
        char[1] = 'e';  
          
        is an error because your trying to assign a pointer to a constant
        */
  } 
  ``` 
  
  

# References 
Stroustrup, B. (2000, February 11). *The C++ Programming Language* (3rd ed.). Addison-Wesley Professional. <https://www.amazon.com/Programming-Language-Special-3rd/dp/0201700735/ref=sr_1_1?crid=2LYS15FV29TAV&keywords=c%2B%2B+programming+third+edition&qid=1669162342&sprefix=c%2B%2B+programming+third+edition+%2Caps%2C72&sr=8-1> 

  
