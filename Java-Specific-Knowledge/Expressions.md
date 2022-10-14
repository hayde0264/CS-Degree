# Expressions 

An *expression* is a construct made up of **variables, operators, and method invocations**, which are construced according to the syntax ofthe language, that evaluates to a single value. 

### The data type of the value returned by an expression depends on the elements used in the expression. 

``` java 
public class Expressions {
    public static void main(String[] args) {
        // declarations
        int[] anArray = {};
        int value1 = 3;
        int value2 = 2;
        int x = 3;
        int y = 4;

        // expressions
        int age = 0;
        anArray[0] = 5;
        System.out.println("Element 1 at index 0: " + anArray[0]);
        int findResult = 1 + 2;
        if (value1 > value2) {
            System.out.println("Value1 is greater than Value2");
        }

        // compound expressions
        int multipleIntsExpression = 5 * 3 * 9;
        int ambiguousExpression = x + y * 100;
        int recommendExpressionInitialization = (x + y) / 2;
    }
}
``` 
The expression *age = 0* returns an int **because the assignment operator returns a value of the same data type as its left-hand operand**.

If you take a look at the other expressions, you can see than expressions can return other types as well, such as *void, boolean, or String*. 

### Compound Expressions
The Java programming language allows you to construct compound expressions from various smaller expressions *as long as the data type requried by one part of the expression match the data type of the other*

``` java 
int multipleIntsExpression = 5 * 3 * 9;
``` 

In this example, the order in which the expression is evaluated is unimportant because the result of the multiplication is **independent oforder**. However, this is not try for all expressions. 

### For instance, the following expression will give different results, depending on whether you perform the addition or division operation first.

``` java 
int ambiguousExpression = x + y * 100;  
``` 

Instead of the ambiguousExpression shown above, specify exactly how an expression will be evaluated using parenthesis **( and )**. 

### Refactored: 

``` java 
int recommendExpressionInitialization = (x + y) / 2; 
``` 

If you don't explicity indicate the order for operations to be performed, **the order is determined by the precedence assigned to the operators in use within the expression**. So, with that being said, **operators that have a higher precedence get evaluated first**. 

### Best practice: 
When writing compound expressions, **be explicit and indicate with parentheses with operators should be evaluated first**. 

## References
Java. (2022). *Learn Java*. <https//dev.java/learn/>     
