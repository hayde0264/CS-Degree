# How do you make a generic class? 

To make a generic class, add the type parameters within the **header** of a class, **NOT**, in the constructor. 

## For instance: 
```java 
  class Pair<T, E> {
          private final T first;
          private final E second;
          
          public Pair(T first, E second) { this.first = first; this.second = second; }
           
          public T getFirst() { return first; }
          public T getSecond() { return second; }
  }       
``` 

Notice the generic types T and E are declared at the **beginning of a class**; The actual type parameters will be
passed to the constructor **as they are initiated**. 


  

# References 
Naftalin, M. & Wadler, A. (2006, November 7). *Java Generics and Collections* (1st ed.). O'Reilly Media. <https://www.amazon.com/Java-Generics-Collections-Development-Process/dp/0596527756/ref=sr_1_1?crid=3FPU8ELZ643P6&keywords=java+generics+and+collections&qid=1669069636&sprefix=java+generics+and+collections%2Caps%2C66&sr=8-1>
