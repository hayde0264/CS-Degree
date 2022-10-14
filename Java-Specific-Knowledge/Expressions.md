# Expressions 

An *expression* is a construct made up of **variables, operators, and method invocations**, which are constructed according to the syntax of the language that evaluates to a single value. 

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

If you take a look at the other expressions, you can see that expressions can return other types as well, such as *void, boolean, or String*. 

### Compound Expressions
The Java programming language allows you to construct compound expressions from various smaller expressions *as long as the data type required by one part of the expression matches the data type of the other*

``` java 
int multipleIntsExpression = 5 * 3 * 9;
``` 

In this example, the order in which the expression is evaluated is unimportant 
