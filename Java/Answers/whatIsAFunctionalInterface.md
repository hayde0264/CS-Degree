# What is a Functional Interface? 

A functional interface is an interface that declares **exactly one abstract method**. 

## Some common Functional Interfaces Java provides: 
```java 
@FunctionalInterface 
public interface Predicate<T> { 
    boolean test(T t); 
} 

@FunctionalInterface 
public interface Consumer<T> { 
    void accept(T t); 
} 

@FunctionalInterface 
public interface Function<T, R> { 
    R apply(T t); 
} 

@FunctionalInterface 
public interface Supplier<T> { 
    T get(); 
 } 
 ``` 


# References 
Fusco, M., Mycroft, A., Urma, R.G. (2014, September 2). *Java 8 in Action: Lambdas, Streams, and functional-style programming* (1st ed.). Manning Publications. <https://www.amazon.com/Java-Action-Lambdas-functional-style-programming/dp/1617291994/ref=sr_1_1?crid=3HQU2KUN42FRP&keywords=java+8+in+action&qid=1669665829&sprefix=java+8+in+action%2Caps%2C85&sr=8-1> 
