# Type Casting-Conversion

Both type casting, as well as type conversion are different ways to change an expression from one data type to another. This can happen **explicitly**, which is known as type casting, or **implicitly**, also known as type conversion. 

# Casting 
**type casting** - also known as a **"narrowing conversion"** since the **destination type is always smaller than the source type** (for instance, int -> byte won't be performed automatically because a byte is smaller than an int)

## For instance: 
```java 
  public class Test {
          public static void main(String[] args) {
                  byte b;
                  int i = 257;
                  double d = 323.142;
  
                  b = (byte) i;
                  i = (int) d;
                  b = (byte) d;
  
                  // 1
                  System.out.println("\nint -> byte");
                  System.out.println("i (int): " + i + "\t" + " b (byte): " + b);
                  // 2
                  System.out.println("\ndouble -> int");
                  System.out.println("d (double): " + d + "\t" + " i (int): " + i);
                  // 3
                  System.out.println("\ndouble -> byte");
                  System.out.println("d (double): " + d + "\t" + " b (byte): " + b);
          }
  }
  /* OUTPUT 
  int -> byte
  i (int): 323     b (byte): 67
  
  double -> int
  d (double): 323.142      i (int): 323
  
  double -> byte
  d (double): 323.142      b (byte): 67
  */
  ``` 
  ## Conversion 
**type conversion** - is also known as a **"widening conversion"** since the **destination type is 
larger than the **source type** (for instance byte -> int can be done automaticlly)

## For instance: 
```java 
  public class Test {
          public static void main(String[] args) {
                  byte b = 22;
                  char c = 'b';
                  short s = 1024;
                  int i = 100;
                  float f = 1.24F;
                  double d = .245;
  
                  // promote b -> float && promote i/c -> int && promote s -> double
                  double test = (f * b) + (i / c) + (d * s);
                  System.out.println("test: " + test);
          }
  }
  /* OUTPUT
  test: 279.1600006866455 
  */
``` 

## Visually:
![cast-conver](https://user-images.githubusercontent.com/109105989/206016981-d12d85cd-995c-4730-b7c7-c8ff624767dd.png)



# References 
Schildt, H. (2014, April 1). *Java: The Complete Reference* (9th ed.). McGraw-Hill Education. <https://www.amazon.com/Java-Complete-Reference-Herbert-Schildt/dp/0071808558/ref=sr_1_1?crid=25QFH9GYUS8XW&keywords=java+the+complete+reference+ninth+edition&qid=1670358704&sprefix=java+the+complete+reference+ninth+edition%2Caps%2C79&sr=8-1> 


