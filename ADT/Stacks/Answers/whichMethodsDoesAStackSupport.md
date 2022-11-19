# Which methods does a Stack support? 
- **push(e)** - inserts element e, to the **top** of the stack 
- **pop()** - removes and returns the **top** element of the stack and will throw an error if the stack is empty 
- **size()** - returns the number of elements in the stack 
- **isEmpty()** - returns a boolean indicating if the stack is empty 
0 **top()** - returns the top element of the stack **without removing it** and will throw an error if the stack is empty 

## In Java: 
```java 
// where Stack<E>
 public int size(); 
 public boolean isEmpty();
 public E top() throws EmptyStackException;
 public void push(E element);
 public E pop() throws EmptyStackException;                                             
``` 


## In an image: 
![stack](https://user-images.githubusercontent.com/109105989/202868836-b55566bc-7edb-4d8f-bd80-f9bbb90f9875.png)





# References 
Goodrich, M. & Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th. ed.). <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=23VA1V4BICEID&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1668886907&sprefix=data+structures+and+algorithms+in+java+4th+edition+%2Caps%2C61&sr=8-1>

