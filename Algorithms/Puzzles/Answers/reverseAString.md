# How do you reverse a string? 

## Java 
```java 
  
  public class Test {
  
          private static String reverseStr(final String s) {
                  final StringBuilder builder = new StringBuilder(s.length());
                  for (int i = s.length() - 1; i >= 0; i--) {
                          builder.append(s.charAt(i));
                  }
                  return builder.toString();
          }
  
          // reverse a string in place
          public static String reverseInplace(final String s) {
                  final StringBuilder builder = new StringBuilder(s);
                  for (int i = 0; i < builder.length() / 2; i++) {
                          final char temp = builder.charAt(i);
                          final int farEnd = builder.length() - i - 1;
                          builder.setCharAt(i, builder.charAt(farEnd));
                          builder.setCharAt(farEnd, temp);
                  }
                  return builder.toString();
          }
  
          public static void main(String[] args) {
                  String test1 = reverseStr("Hayden");
                  String test2 = reverseInplace("Hayden");
  
                  System.out.println(test1); // Prints - nedyah
                  System.out.println(test2); // Prints - nedyah
          }
  }
``` 


# References 
Markham, N. (2014, February 17). *Java Programming Interviews Exposed*. Wrox. <https://www.amazon.com/Java-Programming-Interviews-Exposed-Markham/dp/1118722868/ref=sr_1_1?crid=2WXREDQA55QYL&keywords=java+programming+interviews+exposed&qid=1668642382&sprefix=java+programming+inter%2Caps%2C77&sr=8-1> 
