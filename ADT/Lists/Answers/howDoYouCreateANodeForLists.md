# How do you create a Node for lists?  

A List node should have two properties. The first **a current field**and **next** which points to the next node in the list. 


## For example: 
```java 
 public class Node<E> {
          public E current;
          public Node<E> next;
  }
 ``` 
 
 ## Visually: 
 ![listNode](https://user-images.githubusercontent.com/109105989/204172257-d7f82d9b-c6b7-4d0d-9165-a6b921708f91.png)

  
# References 
Aziz, A. Lee, T. Prakash, A. (2015). *Elements of Programming Interviews in Java* (1st ed.). <https://www.amazon.com/Elements-Programming-Interviews-Questions-Tsung-Hsien/dp/B00C7F0V3W/ref=sr_1_1?crid=SU7GU68QNL5N&keywords=elements+of+programming+interviews+in+java+1st+edition&qid=1669594847&sprefix=elements+of+programming+interviews+in+java+1st+edition+%2Caps%2C72&sr=8-1> 
