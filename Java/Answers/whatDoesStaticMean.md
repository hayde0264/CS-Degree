# What does static mean? 

Static methods and variables can be defined as **" belonging to a class rather than an instance"**. This means variables 
and methods can be accessed through **referencing a class rather than initializing an object**. 


## Example: 
```java 


  package com.hayde.src.main.java.learning;
  
  
  
  public class Test {
          public static void main(String[] args) {
                  System.out.println(SomeClass.EX_INT); // Notice no need for initialization // Prints - 10
          }                                                                                             
  }
  
  class SomeClass {
          public static int EX_INT = 10;
  }
``` 


# References 
Markham, N. (2014, February 17). *Java Programming Interviews Exposed*. Wrox. <https://www.amazon.com/Java-Programming-Interviews-Exposed-Markham/dp/1118722868/ref=sr_1_1?crid=2WXREDQA55QYL&keywords=java+programming+interviews+exposed&qid=1668642382&sprefix=java+programming+inter%2Caps%2C77&sr=8-1> 
