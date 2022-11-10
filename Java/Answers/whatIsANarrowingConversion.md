# What is a narrowing conversion? 

A narrowing conversion occurs when a type <T> is converted into a smaller or "narrower" type <S>. 
  
## Common cases include: 
- T and S **are class types, and S is a subclass of T** 
- T and S **are interface types, and S is a subinterface of T** 
- T **is an interface implemented by class S** 
  
  
  ```java 
   
Number n = new Integer(5); // widening from Integer to Number 
Integer i = (Integer) n;  // narrowing from Number to Integer 
``` 
  
  
# References 
Goodrich, M. Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th ed.). Wiley, John & Sons, Incorporated. <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=1OJL9289EWZ94&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1667519269&qu=eyJxc2MiOiIwLjAwIiwicXNhIjoiMC4wMCIsInFzcCI6IjAuMDAifQ%3D%3D&sprefix=data+structures+and+algorithms+in+java+4th+edition%2Caps%2C83&sr=8-1> 
