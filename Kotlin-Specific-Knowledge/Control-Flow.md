# Control Flow 

## If expression 
In Kotlin, **if** is an expression: so it returns a value. Therefore, there is no ternary operator **(condition ? then: else)** because ordinary **if** works fine in this role. 

![if](https://user-images.githubusercontent.com/109105989/196064958-6986c6bf-ff4b-41c9-afcf-cb0e59f7d697.png)

![expressionif](https://user-images.githubusercontent.com/109105989/196064959-d3c50ad7-98c2-4ba1-86c1-e8f9a0bac1d6.png)

``` kotlin
// if
fun ifExample(a: Int, b: Int) {
    var higherInt = a
    if (a < b) higherInt = b
}

// if-else
fun ifElseExample(a: Int, b: Int) {
    var higherInt: Int
    if (a > b) {
        higherInt = a
    } else {
        higherInt = b
    }
}

// as an expression
val asExpression = { a: Int, b: Int -> if (a > b) a else b }
``` 

Branches of an **if** expression can be blocks. In this case, the last expression is the value of a block: 

``` kotlin 
// expressions with blocks 
val expressionWithBlocks = { a: Int, b: Int -> 
    if (a > b) {
        println("Choose a")
        a 
    } else {
        println("Choose b")
        b
    }
}
``` 

If you're using **if** as an expression, for example, for returning its value or assigning it to a variable, the **else** branch is mandatory. 

## When expression 
The **when** expression defines a conditional expression with multiple branches. It is similar to the **switch** statement in C-like languages. 

``` kotlin 
// when statement
fun whenStatement(i: Int) {
   when(i) {
       1 -> print("i is 1")
       2 -> print("i is 2")
       else -> { print("i is neither 1 or 2") }
   }
}
``` 

The **when** statement matches its arguments against all branches sequentially until some branch condition is satisfied. 

The **when** statement can be used either as an expression or as a statement. If it is used as an expression, the value of the first matching branch becomes the value of the overall expression. If it is used as a statement, the values of individual branches are ignored. Just like with if, each branch can be a block, and its value is the value of the last expression block. 

The **else** branch is evaluated if none of the other branch's conditions are satisfied. 

If **when** is used as an expression, the **else** branch is mandatory unless the compiler can prove that all possible cases are covered with branch conditions, for example, with **enum** class entries and **sealed** class subtypes. 

### When statements are mandatory when: 
- when has a subject of a Boolean, enum, or sealed type, or their nullable counterparts 
- branches of when don't cover all possible cases for this subject

``` kotlin 
// else not required because all cases are covered
enum class Color {
    Red, Green, Blue
}
fun elseNotRequired(c: Color) {
    when(c) {
        Color.Red -> println("red")
        Color.Green -> println("green")
        Color.Blue -> println("blue")
    }
}
fun elesRequired(c: Color) {
    when(c) {
        Color.Red -> println("red")
        else -> println("color isn't red")
    }
}
``` 

To define common behavior for multiple cases, combine their conditions in a single line with a comma: 
``` kotlin
// defining common behaviors for multiple cases
fun multipleCases(x: Int) {
    when (x) {
        0, 1 -> println("x is 0 or x is 1")
        else -> println("neither 0 or 1")
    }
}
``` 
 
You can use arbitrary expressions (not only constants) as branch conditions: 
``` kotlin 
// arbitrary branches
fun arbitraryBranches(x: Int, s: String) {
    when(x) {
        s.toInt() -> println("s encodes x")
        else -> print("s will not encode x")
    }
}
``` 

You can also check a value for being in or !in a range or a collection: 
``` kotlin 
// check range or collections 
fun checkSequence(x: Int) {
    when (x) {
        in 1..10 -> print("x is within 1 to 10")
        else -> print("not within range")
    }
}
``` 

## For Loops 
The **for** loop iterates through anything that provides an iterator. This is equivalent to the **foreach** loop in languages like C#. 

![for](https://user-images.githubusercontent.com/109105989/196064676-f04a800b-3955-4350-b84d-7c4d278b5412.png)

Iterate over a range of numbers: 
``` kotlin 
// iterate over a range of numbers 
fun rangeIteration() {
    for (i in 1..3) { 
        println(i) 
    } 
    for (i in 10 downTo 0 step 2) { 
        println(i) 
    } 
}
``` 

A **for** loop over a range or an array is compiled to an index-based loop that **does not** create an iterator object. 

So, if you want to iterate through an array or list with an index, implement: 
``` kotlin 
// iterate with indices 
fun iterationWithIndices(array: List<Int>) { 
    for (i in array.indices) {
        println(array[i])
    }
}
``` 

Alternatively, you may use the withIndex library function: 
``` kotlin 
// iterate with library functions 
fun iterationWithIndexMethod(array: List<Int>) { 
    for ((index, value) in array.withIndex()) {
            println("the element at $index is $value")
    }
}
``` 

## While Loops 
**while** and **do-while** loops execute their body **continuously while their condition is satisfied**. The difference between them is the condition checking time: 

- **while** checks the condition and, if it's satisfied, executes the body and then returns to the condition check. 

- **do-while** executes the body and then checks the condition. If it's satisfied, the loop repeats. So, the body of **do-while** is executed at least once, regardless of the condition. 

# References 
*Kotlin docs*. (2022). Kotlin. <https://kotlinlang.org/docs/home.html> 
