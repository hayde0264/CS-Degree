# Trees

A tree is an abstract data type that stores elements **hierarchically**. Excluding the top element, each element in 
a tree has a **parent** element and **zero or more children** elements. 

## Hiercarchies 
Hierarchies create relationships among trees. Meaning objects, or more formally, **"nodes," exist **below** or **above** others. So, 
jargon for hierarchies include things such as **"parent," "child," "ancestor," and "descendent"**. 


## Instances: 
- **root nodes** - have **no parents** 
- **internal nodes** - sometimes called **"leaves"** have **one or more** children 
- **external nodes** - have **no children** 
- **sibling nodes** - are nodes that have the **same parent** 

## In an image: 

![tree](https://user-images.githubusercontent.com/109105989/202873378-77fcfce5-7694-455d-9418-e0955266b43d.png)


## In Java: 
```java 
  import java.util.Iterator;
  
  
  public interface Tree<E> {
          public int size(); // returns the number of nodes
  
          public boolean isEmpty(); // returns if a tree is empty or not
  
          public Iterator<E> iterator(); // returns an iterator of elements
  
          public Iterable<Position<E>> positions(); // returns an iterator collection

          public E replace(Position<E> v, E e) throws InvalidPositionExcpetion; // replaces the element stored at a specific node
                                      
          public Position<E> root() throws EmptyTreeException; // returns the root node
  
          public Position<E> parent() throws InvalidPositionExcpetion, BoundaryViolationException; // returns the parent node
  
          public Iterable<Position<E>> children(Position<E> v) throws InvalidPositionExcpetion; // returns an iterable collection of children nodes
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            public boolean isInternal(Position<E> v) throws InvalidPositionExcpetion; // returns if a node is internal or not
                                                                                                           
          public boolean isExternal(Position<E> v) throws InvalidPositionExcpetion; // returns if a node is external or not
                                                                                                                     
          public boolean isRoot(Position<E> v) throws InvalidPositionExcpetion; // returns if a node if the root or not
  }  


# References 
Goodrich, M. & Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th. ed.). <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=23VA1V4BICEID&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1668886907&sprefix=data+structures+and+algorithms+in+java+4th+edition+%2Caps%2C61&sr=8-1>

