# How do you traverse a stream? 


## For example: 
```java 
import java.util.Arrays;
import java.util.List;
import java.util.stream.*;
  
  
public class Test {
        public static void main(String[] args) {
  
        List<String> l = Arrays.asList("1", "2", "3");
        Stream<String> s = l.stream();
  
        s.forEach(System.out::println); // Prints - 1 2 3
        }
}
```

# References 
Fusco, M., Mycroft, A., Urma, R.G. (2014, September 2). *Java 8 in Action: Lambdas, Streams, and functional-style programming* (1st ed.). Manning Publications. <https://www.amazon.com/Java-Action-Lambdas-functional-style-programming/dp/1617291994/ref=sr_1_1?crid=3HQU2KUN42FRP&keywords=java+8+in+action&qid=1669665829&sprefix=java+8+in+action%2Caps%2C85&sr=8-1> 
