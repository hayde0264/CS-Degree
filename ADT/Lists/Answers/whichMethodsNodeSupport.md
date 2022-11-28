# Which methods does Node support? 

For a singly linked listed the List Node class will support methods such as **search, insert, and delete**. 

**search** - O(n)
**insert** - O(1)
**delete** - O(1) 

## For example: 
```java 
  public class Node<E> {
          public E current;
          public Node<E> next;
  }
  ``` 
  ```java 
  package com.example.hayde;
  
⚠ import com.example.hayde.Node;
  
  
  public class NodeMethods {
  
  
          // search
          public static Node<Integer> search(Node<Integer> N, int key) {
                  while (N != null && N.current != key) {
                          N = N.next;
                  }
                  return N;
          }
          // insert
          public static void insertAfter(Node<Integer> node, Node<Integer> newNode) {
                  newNode.next = node.next;
                  node.next = newNode;
          }
          // delete
          public static void deleteList(Node<Integer> someNode) {
                  someNode.next = someNode.next.next;
          }
  
  
  }
