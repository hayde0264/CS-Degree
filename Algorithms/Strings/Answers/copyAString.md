# Copy a string 

I - **Time** == O(m) **Space** == O(1) *where m is length of string1* 
R - **Time** == O(m) **Space** == O(1) *where m is length of string1*


Given two string, copy one string to other iteravely and recursively. 


> Input: s1 = "hi"
>        s2 = "bye"
> Output s2 = "hi" 


## Java: 
```java 
  package com.src.main.hayde.learning;
  
  
  public class Tests {
  
          // iterative
          public static void iterativeCopy(char s1[], char s2[]) {
                  int i = 0;
                  for (i = 0; i < s1.length; i++) {
                          s2[i] = s1[i];
                  }
          }
  
          // driver
          public static void main(String[] args) {
                  char string1[] = "hayde".toCharArray();
                  char string2[] = new char[string1.length];
  
                  iterativeCopy(string1, string2);
  
                  System.out.println(String.valueOf(string2)); // Prints - hayde
          }                                                               
  }                                                            
``` 



