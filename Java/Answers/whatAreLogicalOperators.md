
# What are logical operators? 

Logical operators in Java are used to **evaluate expressions**. Such expressions should return **boolean values**. 

## They include: 
- **and** (&&) 
- **or** (||) 
- **not** (!) 

## For instance: 
```java

# What are logical operators? 

Logical operators in Java are used to **evaluate expressions**. Such expressions should return **boolean values**. 

## They include: 
- **and** (&&) 
- **or** (||) 
- **not** (!) 

## For instance: 
```java 
  public class Test {
          public static void main(String[] args) {
  
                  int a = 0;
                  int b = 1;
                  int c = 2;
  
                  boolean test1 = a + b < c ? true : false;
                  boolean test2 = a > 1 && b > 1 ? true : false;
                  boolean test3 = c <= 0 || a >= 1 ? true : false;
  
  
  
                  System.out.printf("%b, %b, %b", test1, test2, test3); // Prints - true, false, false
  
          }
  }
``` 



# References 
Guapta, M. (2013, April 2). *OOCA Java SE 7 Programmer I Certification Guide: Prepare for the 1Z0-803 exam* (1st ed.). Manning. <https://www.amazon.com/OCA-Java-Programmer-Certification-Guide-ebook/dp/B0977ZZ1MX/ref=sr_1_14?crid=OJB2X5MUTT51&keywords=java+se+7+certified&qid=1670094976&sprefix=java+se+7+certifie%2Caps%2C71&sr=8-14> 
