# Is odd? 

## Java: 
```java 
public class isOdd { 
      private static boolean isOdd1(int i) { 
              return i / 2 == 0; 
      } 
      
      // slightly more efficient with bitwise AND (&) 
      private static boolean isOdd2(int i) { 
              return (i & 1) != 0; 
      } 
      
      public static void main(String[] args) { 
              boolean test1 = isOdd1(2); 
              boolean test2 = isOdd2(3); 
              
              System.out.printf("%s ", test1); // Prints - false 
              System.out.printf("%s ", test2); // Prints - true 
      } 
 } 
 ``` 
 
 
 
 
 
