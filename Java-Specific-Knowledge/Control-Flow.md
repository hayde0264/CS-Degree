# Control Flow

## If-Then Statement 
The **if-then** statement is the most basic of all control flow statements. It tells your program to execute a certain section of code **only if a particular test evaluates to true**. For example, in the **Person**, you would only supply sunscreen **if you have fair skin**. 

![if](https://user-images.githubusercontent.com/109105989/196064958-6986c6bf-ff4b-41c9-afcf-cb0e59f7d697.png)

![expressionif](https://user-images.githubusercontent.com/109105989/196064959-d3c50ad7-98c2-4ba1-86c1-e8f9a0bac1d6.png)

``` java 
class Person {
    private boolean hasFairSkin;

    Person(boolean hasFairSkin) {
        this.hasFairSkin = hasFairSkin;
    }

    public void applySunscreen() {
        // check here for if statement
        if (hasFairSkin) {
            System.out.println("Apply Sunscreen");
        }
    }

    public static void main(String[] args) {
        Person matt = new Person(true);
        matt.applySunscreen();	// Prints - Apply Sunscreen 

        Person sydney = new Person(false);
        sydney.applySunscreen();	// Prints nothing 
    }
}
``` 
## The If-Else Statement 
The if-else statement provides a secondary path of execution when at **"if" clause evaluates to false**. So, in the **Person** class, if an object doesn't implement fair skin, we can return an expression. 

``` java 
 public void applySunscreen() {
        if (hasFairSkin) {   
	// if hasFairSkin == true 
	System.out.println("Apply Sunscreen")      
  	} else {  
	// if hasFairSkin == false 
        System.out.println("Jump right in!");
     }
 }
``` 

## While and Do-while Statements 
The **while** statement continually executes a block of statements while a particular **condition is true**. 

The **while** statement evaluates an expression, which must **return a boolean value**. If the expression evaluates to true, **the while statement will continue executing statement(s) within the block**. The while statement will continue testing the expression and executing its block **until the expression evaluates to false**. 

``` java 
class WhileDemo {
    public static void main(String[] args) {
        int spendingLimit = 10;
        while (spendingLimit < 10) {
            System.out.println("You've spent " + spendingLimit);
            spendingLimit++;
        }
    }
} 
``` 

Java also provides a **do-while** statement. The difference between **do-while** and **while** is that **do-while** evaluates its expression **at the bottom of the loop instead of the top**. This means statements within the **do** block **are always executed at least once**. 


``` java 
class DoWhileDemo {
    public static void main(String[] args) {
        int spendingLimit = 10;
        do {
            System.out.println("You've spent" + spendingLimit);
            spendingLimit++;
        } while (spendingLimit < 10);
    }
}
``` 

## The For Statement 
The **for** statement provides a compact way to **iterate over a range of values**. Programmers often refer to it as the "for loop" because of the way in which **it repeatedly loops until a particular condition is satisfied**. 

### Every for statement has: 
- a **initialization** expression which initializes the loop (gives the loop a starting point)
- a **condition** expression comes next. Once this expression evaluates to false the loop terminates
- an **increment** expression which is invoked after each iteration through the loop; this expression can increment or decrement a value

``` java 
class ForDemo { 
    public static void main(String[] args) { 
    	// initialize i with 0, as long as i is less than 11, incement i by 1 
        for (int i = 0; i < 11; i++) {
            System.out.println("Count is " + i);
        } 
    }
}
/* Output 
Count is 1 
Count is 2 
Count is 3 
Count is 4 
Count is 5 
Count is 6 
Count is 7 
Count is 8 
Count is 9 
Count is 10 
 */
``` 

The **for** statement is also designed **to iterate through Collections and arrays**. This form is sometimes referred to as the **enhanced for statement** and can be used to make your loops **more compact and easy to read**. 

``` java 
class EnhancedForDemo { 
    public static void main(String[] args) { 
        int[] arrayOfNums = {1, 2, 3, 4, 5, 6, 7, 8}; 
	// here num represents each element within the arrayOfNums
        for (int num: arrayOfNums) {
            System.out.println("Number is " + num);
        }
    }
}
/*  Output 
Number is 1 
Number is 2 
Number is 3 
Number is 4 
Number is 5
Number is 6 
Number is 7 
Number is 8 
 */
``` 

# References 
*Learn Java*. (2022). Java. <https://dev.java.learn/> 
