# Stacks

A stack is a collection of objects that are **inserted and removed** according to a **last-in-first-out (LIFO)** paradigm. A stack included methods which allow 
developers to **insert elements, remove top elements, figure out the size of the stack, determine if a stack is empty, and peek at the top element**.  


## Life Metaphor 
A fun way to image a stack is to envision the PEZ candy dispenser. This dispenser stores candies in a spring-loaded 
container, which **"pops"** the top-most candy as the dispenser is lifted. 

## 
![pez](https://user-images.githubusercontent.com/109105989/202872237-474f6b2c-1aa5-481b-9f84-d94d4355e212.png)


## In Java: 
```java 
  import java.util.EmptyStackException;
  
  public interface Stack<E> {
          public int size(); // returns number of elements in Stack 
  
          public boolean isEmpty(); // returns a boolean indicating if the Stack is empty 
  
          public E top() throws EmptyStackException; // returns the top element of the stack, and throws error if Stack is empty   
          
          public void push(E element); // inserts the element E to the top of the Stack
  
          public E pop() throws EmptyStackException; // removes and returns top element of Stack, and throws error if Stack is emtpy                                                                                                                                                       
  }                                                
``` 


# References 
Goodrich, M. & Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th. ed.). <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=23VA1V4BICEID&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1668886907&sprefix=data+structures+and+algorithms+in+java+4th+edition+%2Caps%2C61&sr=8-1>
