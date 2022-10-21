# Type checks and casts 

Use the **is** operator or its negated form **!is** to perform a runtime check that **idtenfies whether an object conforms to a give type**: 
``` kotlin 
fun checkType(obj: Any) {
    if (obj is String) {
        print(obj.length)
    }
    if (obj !is String) {   // !is == "NOT"
        print("Not a Sting")
    } else {
        print(obj.length)
    }
}
``` 


## Smart casts 
In most cases, you don't need to use explicit cast operators in Kotlin **because the compiler tracks the is-checks and explicit casts** for immutable values and inserts (safe) casts automatically when neccessay: 

``` kotlin 
fun smartCast(x: Any) {
    if (x is String) {
        print(x.length)     // will cast value to string
    }
}
``` 

The compiler is smart enough to know that a cast is safe if a negative check leads to a return. But remember 
> "smart casts only work when the compiler can guarantee that the variable won't change between the check and the usage" 

An example with or: 
``` kotlin 
fun smartCastWithOr(x: Any) {
    if (x !is String || x.length == 0) return   // x is automatically cast to a String on the ride side of ||
    if (x is String && x.length > 0) {
        print(x.length)        // x is automatically casted to a String
    }
}
```

An example withe when: 
``` kotlin 
fun smartCastWithWhen(x: Any) {
    when(x) {
        is Int -> print(x + 1 )
        is String-> print(x.length + 1)
        is IntArray -> print(x.sum())
    }
} 
``` 

# References 
Kotlin docs. *Kotlin*. <https://kotlinlang.org/docs/home.html> 
