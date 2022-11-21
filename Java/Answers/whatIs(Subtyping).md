
# What is subtyping? 

In Java, a single type is considered a **" subtype** of another if they by **extend or implement** a particular class. 

## Examples include: 
- **Integer && Double** are a subtype of **Number** 
- **ArrayList<E>** is a subtype of **List<E>** 
- **Collection<E>** is a subtype of **Iterable<E>** 
 
## 
In the example below, if we have a collection of numbers, I can add an **integer or a double**since both 
  are subtypes of **Number** 
  
  ## 
  ```Java 
    public class Tests {
          public static void main(String[] args) {
          
          List<Number> nums = new ArrayList<Number>();
          nums.add(2);
          nums.add(3.14);
          assert nums.toString().equals("[2, 3.14]");
          
          }
  }
``` 
  
  

# References 
Naftalin, M. & Wadler, A. (2006, November 7). *Java Generics and Collections* (1st ed.). O'Reilly Media. <https://www.amazon.com/Java-Generics-Collections-Development-Process/dp/0596527756/ref=sr_1_1?crid=3FPU8ELZ643P6&keywords=java+generics+and+collections&qid=1669069636&sprefix=java+generics+and+collections%2Caps%2C66&sr=8-1>
