# What is the == operator? 

The **"=="** operator returns a boolean if the primitive values compared are equal. 


## For example: 
```java 
  public class Test {
          public static void main(String[] args) {
  
                  int a = 1;
                  int b = 2;
                  int c = a;
                  int d = 1;
  
  
                  boolean test1 = a == b ? true : false;
                  boolean test2 = a == c ? true : false;
                  boolean test3 = a != c ? true : false;
                  String test4 = a == d ? "points to same value in pool" : "doesn't point to same value in pool";
                  System.out.printf("%b, %b, %b, %s", test1, test2, test3, test4  );
                  /* Output
                  false, true, false, points to same value in pool 
                  */
          }
  }
``` 

## Visually: 

![==](https://user-images.githubusercontent.com/109105989/205467207-0352a482-90e6-4c59-88b7-466c9a077b12.png)



# References 
Guapta, M. (2013, April 2). *OOCA Java SE 7 Programmer I Certification Guide: Prepare for the 1Z0-803 exam* (1st ed.). Manning. <https://www.amazon.com/OCA-Java-Programmer-Certification-Guide-ebook/dp/B0977ZZ1MX/ref=sr_1_14?crid=OJB2X5MUTT51&keywords=java+se+7+certified&qid=1670094976&sprefix=java+se+7+certifie%2Caps%2C71&sr=8-14> 
