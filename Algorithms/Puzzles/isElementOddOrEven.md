# Is an element odd or even? 

## Java: 
```java 
 1 public class Test {
    2         public static void main(String[] args) {
    3                 String a = isOddOrEven(2);
    4                 String b = isOddOrEven(3);
    5                 String c = isOddOrEven(55);
    6 
    7                 System.out.println(a); // Prints - even
    8                 System.out.println(b); // Prints - odd
    9                 System.out.println(c); // Prints - odd
   10         }
   11         private static String isOddOrEven(int i) {
   12                 return  (i & 1) != 0? "odd" : "even";
   13         }
   14 
   15 }
   16 ``` 
   
