# Control Flow 

## If expression 
In Kotlin, **if** is an expression: so it returns a value. Therefore, there is no ternary operator **(condition ? then : else)** because ordinary **if** works fine in this role. 

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

If you're using **if** as an expression, for example, for returning its value orassigning it to a variable, the **else** branch is mandatory. 

