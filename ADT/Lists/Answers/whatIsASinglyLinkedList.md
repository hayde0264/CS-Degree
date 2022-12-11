# What is a singly linked list? 

A singly linked list is a **data structure** which consists of nodes **that represent a sequence**. Each Node contains data as well as a **reference or link to the next Node in the sequence**. 

## What are the first and last elements? 

Within a singly linked list, the first Node is called the **"head"**, and the last Node is called the **tail**. So, when the tail is 
reached, we consider the next reference **null**. 

![headAndTail](https://user-images.githubusercontent.com/109105989/203698054-41ecae03-3f28-4dd9-b066-b463f9581efa.png)



## How do they compare to arrays? 
Like an array, singly linked lists keep elements in a particular order. This order is determined by the chain or next links between nodes. Unlike an array, a singly linked list does **not have a predetermined size and will use space proportionally to its number of elements**. So, when 
working with singly linked **, we do not keep track of any indices for the nodes within the list**. 

![arrayVsLinkedList](https://user-images.githubusercontent.com/109105989/203697887-b40b6023-2f18-41d6-8c70-036373dcdaf3.png)

## In C++: 
```cpp 
template <typename T>
struct ListNode {
    T data;
    shared_ptr<ListNode<T>> next;
};
``` 


## In Java: 
```java 
  public class Node {
          private String element; 
          private Node next; 
  
          public Node(String element, Node next) { this.element = element; this.next = next; }
          
          public String getElement() { return element; }
          public Node getNext() { return next; }  
          public void setElement(String element) { this.element = element; }
          public void setNext(Node next) { this.next = next; }
  }
                             
                             
 public class SinglyLinkedList {
          protected Node head;
          protected long size;
          
          public SinglyLinkedList() {
                  head = null;
                  size = 0;
          }       
  }  
``` 



# References 
Goodrich, M. & Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th. ed.). <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=23VA1V4BICEID&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1668886907&sprefix=data+structures+and+algorithms+in+java+4th+edition+%2Caps%2C61&sr=8-1>

