# Boxing-Unboxing-Autoboxing 


**boxing** - is the transformation of a primitive type to object 
**unboxing** - is the transformation of an object to a primitive type 
**autoboxing** - refers to the Java compiler's automatic conversion of a primitive type into its corresponding object (wrapper type) 


## In Java: 
```java 
  import java.util.ArrayList;
                                 
  public class Test {
          public static void main(String[] args) {
                  ArrayList<Integer> list = new ArrayList<Integer>();
                                                                     
                  
                  // autoboxing
                  list.add(1); // type == object
                  list.add(2); // type == object
                                                  
                  // also autoboxing     
                  Integer a = 10;        
                                 
                  // unboxing  
                 int unboxList = list.get(0); // type == int (primitive)
                                                                          
                  // also unboxing
                 int unboxA = a; // type == int (primitive)
          }                                                                   
  }                            
``` 

## Visually: 
![boxing](https://user-images.githubusercontent.com/109105989/205767290-cd7149d2-00f7-4632-a78a-faade4ea2f11.png)



# References 
Boxing (computer science). (2022, August 17). *Wikipedia*. <https://en.wikipedia.org/wiki/Boxing_(computer_science)> 

