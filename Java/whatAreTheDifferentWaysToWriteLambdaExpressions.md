# What are the different ways to write lambda expressions? 

```java 
Runnable withoutParams = () -> System.out.println("some message"); // ex. 1 

ActionListener singleParam = onClick -> System.out.println("button clicked"); // ex. 2 

Runnable multipleStatements = () -> {       // ex. 3 
  System.out.print("Hayden"); 
  System.out.println(" Howell"); 
}; 

BinaryOperator<Long> addTwoParams = (a, b) -> a + b; // ex. 4 

``` 

# Explanations: 
1. Indentifies a lambda expression with **no arguments**. To signify, we use an **empty pair of parenthesis ()**. This says, "We're implementing Runnable, whose only method **run** takes **no** arguments, and it's return type is **void**. 
2. Identifies a lambda expression with **one argument**. This lets us **omit the parenthesis () around the argument**. 
3. Identifies a lambda expression as a **block with multiple statements**. Remember, with lambdas, you can **return or throw exceptions**, and you can also use braces with a single-line lambda to clarify where it **begins and ends**. 
4. Recognize this line of code **doesn't just add two numbers**; this function creates **a function that adds up two numbers**. The variable called **"addTwoParams"** that's a **BinaryOperator<Long>** isn't the result of adding two numbers; but rather is **the code that adds together two numbers**. 





# References 
Warburton, R. (2014, April 22). *Java 8: Functional Programming For The Masses*. O'Reilly Media. https://www.amazon.com/Java-Lambdas-Functional-Programming-Masses/dp/1449370772/ref=sr_1_fkmr2_2?crid=3EGTTE9HN27ZA&keywords=java+8+lambas&qid=1667851133&sprefix=java+8+lambas+%2Caps%2C81&sr=8-2-fkmr2
