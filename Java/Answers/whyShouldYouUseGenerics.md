# Why should you use generics? 

Use generics because they create **abstract types which avoid explicit casts** a generics type is not defined at compile time but rather at **run time**. 


## Notice the flexibility: 
```java 
  import java.util.ArrayList;
  import java.util.Arrays;
  import java.util.List;
  
  public class Pair<K, V> {
    K key;
    V value;
  
  
    public Pair(K key, V value) {
      this.key = key;
      this.value = value;
    }
  
  
    public void printKey() { System.out.println(key); }
    public void printValue() { System.out.println(value); }
  
    public static void main(String[] args) {
      Pair<Integer, Integer> ex1 = new Pair<Integer,Integer>(2, 3);
      Pair<String, Integer> ex2 = new Pair<String,Integer>("yolo", 4);
      Pair<Boolean, List<String>> ex3 = new Pair<Boolean,List<String>>(true, Arrays.asList("3, 3, 3, 2, 54"));
  
  
      ex1.printKey(); // Prints - 2
      ex1.printValue(); // Prints - 3
      ex2.printKey(); // Prints - yolo
      ex2.printValue(); // Prints - 4
      ex3.printKey(); // Prints - true
      ex3.printValue(); // Prints - [3, 3, 3, 2, 54]
    }
  }
``` 


# References 
Goodrich, M. Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th ed.). Wiley, John & Sons, Incorporated. <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=1OJL9289EWZ94&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1667519269&qu=eyJxc2MiOiIwLjAwIiwicXNhIjoiMC4wMCIsInFzcCI6IjAuMDAifQ%3D%3D&sprefix=data+structures+and+algorithms+in+java+4th+edition%2Caps%2C83&sr=8-1> 
