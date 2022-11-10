# What is a widening conversion? 

A **widening conversion** is when a type <T> is converted into a **wider type** <U>. 
  
  
## Common cases include: 
  - T and U are **class types** and **U is the superclass of T** 
  - T and U are **interface types** and **U is a super interface of T** 
  - T is a **class that implements interface U**. 
  
  
  ## For example: 
  Widening conversions are performed to **store the result of an expression into a variable**, which gets rid of the need for an **explicit cast**. 
  
  ```java 
    
  Integer i = new Integer(5); 
  Number n = i; // this is the conversion which widens Integer to Number 
  ``` 
  
  
# References 
Goodrich, M. Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th ed.). Wiley, John & Sons, Incorporated. <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=1OJL9289EWZ94&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1667519269&qu=eyJxc2MiOiIwLjAwIiwicXNhIjoiMC4wMCIsInFzcCI6IjAuMDAifQ%3D%3D&sprefix=data+structures+and+algorithms+in+java+4th+edition%2Caps%2C83&sr=8-1> 
