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

    public class GeneralStack<T> {
          private static calss StackNode<T> {
                  private T data;
                  private StackNode<T> next;
  
                  public StackNode(T data) { this.data = data; }
          }
  
          private StackNode<T> top;
  
  
          public T pop() {
                  if (top == null) throw new EmptyStackException();
                  T item = top.data;
                  top = top.next;
                  return item;
          }
          public void push(T item) {
                  StackNode<T> t = new StackNode<T>(item);
                  t.next = top;
                  top = t;
          }
          public T peek() {
                  if (top == null) throw new EmptyStackException();
                  return top.data;
          }
          public boolean isEmpty() {
                  return top == null;
          }
  }
``` 

## In C++: 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  template<class E>
  class Stack {   
          public:
                  virtual void initialize() = 0;                                          
                                                                                          
                  virtual bool isEmpty() const = 0;                                       
                                                                                          
                  virtual E top() const = 0;                                              
                                                                                          
                  virtual void push(const E& element) = 0;
  
                  virtual void pop() = 0; 
  };     
```


# References 
Goodrich, M. & Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th. ed.). <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=23VA1V4BICEID&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1668886907&sprefix=data+structures+and+algorithms+in+java+4th+edition+%2Caps%2C61&sr=8-1>
