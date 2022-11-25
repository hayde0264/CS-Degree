# What is an abstract node list? 

An abstract node list **abstracts the concrete linked list data structure**. Which is achieved by 
using a **related abstract position type**, which abstracts the concept of **place** in a node list. 

## The Goal 
The goal is to define methods that take nodes parameters from **singly and doubly linked lists** and provide **nodes as return types**, thus 
providing **significant** speedups compared to index-based methods. 

## What's needed? 
To make this work, we'll need two interfaces: a Position and PositonList interface. 

## The position interface will contain: 
- **element()** - its job is to return the element at a stored position 

## The position list interface will contain: 
- **size()** - returns the number of elements within the list 
- **isEmpty()** - returns whether a list is empty or not 
- **first()** - returns the first node 
- **last()** - returns the last node 
- **next()** - returns the node after a specified node 
- **prev()** - returns the previous node after a specified node 
- **addFirst()** - inserts an element at the start of the list, returning its new position 
- **addLast()** - inserts an element at the end of the list, returns its new position 
- **addAfter()** - inserts an element after a specified node 
- **addBefore()** - inserts an element before a specified node 
- **remove()** - removes a node from the list, returning the element 
- **set()** - replaces the element stored, returning the old element 


## Implementation: 
```java
public interface Position<E> {
          E element();
  }
  
public interface PositionList<E> {
          public int size();
  
          public boolean isEmpty();
  
          public Position<E> first();
  
          public Position<E> last();
  
          public Position<E> next(Position<E> p) throws InvalidPositionException, BoundaryViolationException;
  
          public Position<E> previous(Position<E> p) throws InvalidPositionException, BoundaryViolationException;
  
          public void addFirst(E e);
  
          public void addLast(E e);
  
          public void addAfter(Position<E> p, E e) throws InvalidPositionException;
   
          public void addBefore(Position<E> p, E e) throws InvalidPositionException;
  
          public E remove(Position<E> p) throws InvalidPositionException;
  
          public E set(Position<E> p, E e) throws InvalidPositionException;
  }
  ```
  

# References 
Goodrich, M. & Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th. ed.). <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=23VA1V4BICEID&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1668886907&sprefix=data+structures+and+algorithms+in+java+4th+edition+%2Caps%2C61&sr=8-1>


  
