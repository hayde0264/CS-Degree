# Control Flow 

Swift provides a variety of control flow statements. 

## These include: 
- *while* loops to perform a task multiple times 
- *if, guard, switch* statements to execute different branches of code on certain conditions. 
- *break & continue* to transfer the flow of execution to another point in the code 

Swift also provides a **for-in** loop that makes it easy **to iterate over arrays, dictionaries, ranges, strings, and other sequences**. 

Swift's **switch** statement is considerably more powerful than its counterpart in many C-like languages. Cases can match many different patterns, including **interval matches, tuples, and casts to specific types**. 

Matched values in a switch case **can be bound to temporary constants or variables for the use within the case's body**, and complex matching conditions can be expressed with a **where** clause for each case. 

## For-In Loops 
You use the **for-in** loop to iterate over a sequence, such as items in an array, 
ranges of numbers or characters in a string. 

![for-loop-javascript](https://user-images.githubusercontent.com/109105989/196009601-3cf0d01f-69b6-40f0-9318-42f29ada822c.png)

``` swift
// standard for-in loop
let workStaff = ["Bill", "Katy", "Susie", "Reggie"]
let readForInLoop = { for worker in workStaff {
            print("Hello \(worker)!")
    }
}
print(readForInLoop())
// Hello, Bill!
// Hello, Katy!
// Hello, Susie!
// Hello, Reggie!
``` 

You can also iterate over a dictionary **to access its key-value pairs**. Each item in the dictionary is returned as a **(key, value)** tuple when the dictionary is iterated, and you can decompose the **(key, value** tuple's members as explicitly named constants for use within the body of the for-in loop. 

``` swift 
// for-in dictionary loop
let playerWithHits = ["Jackie": 4, "Ben": 10, "Ryan": 6]
let readDictionaryLoop = { for (player, hits) in playerWithHits {
    print("\(player) has \(hits) hits this season.")
    }
}
print(readDictionaryLoop())
// Ryan has 6 hits this season.
// Ben has 10 hits this season.
// Jackie has 4 hits this season. 
``` 
### Remember the contents of a Dictionary are inherently unordered, so iterating over them doesn't guarantee the order in which they will be retrieved. 

``` swift 
// for-in range loop
let readRangeLoop = { for i in 1...5 {
    print("\(i) times 2 is \(i * 2).")
    }
}
print(readRangeLoop())
// 1 times 2 is 2.
// 2 times 2 is 4.
// 3 times 2 is 6.
// 4 times 2 is 8.
// 5 times 2 is 10.
``` 
The sequence being iterated over is a **range of numbers from 1 to 5**, inclusive as indicated by the use of the closed range operator **(...)**. The value of 
**i** is set to the first number in the range **1**, and the statements inside the loop are executed. 

In this case, the loop **contains only one statement**, which prints an entry from the two-times table for the current value of **i**. 

After the statement is executed, the value of **i** is updated to contain the second value in the range **2**, and the print() function is called again. This process continues until the end of the range is reached.

## While-Loops 
A **while** loop performs a set of statements until **a condition becomes false**. 

These kinds of loops are best used when **the number of iterations isn't known before the first iteration begins**. 

**while** - evaluates its condition at the **start** of each pass through the loop. 

**repeat-while** - evaluates its condition at the **end** of each pass through the loop. 

A while loop starts by evaluating a single condition. **If the condition is true, a set of statements is repeated until the condition becomes false**. 

![word-image](https://user-images.githubusercontent.com/109105989/196009731-7cd92672-f0ce-4e8a-87a6-ce29150d6eba.png)

``` swift
// general while loop  
var cash = 0 
var spendLimit = 10 
let getShoppingSpree = { while cash < spendLimit {
    // start spending 
    cash += 1
    
    // warn if spent seven dollars
    if cash == 7 {
        print("Slow down cowboy, you'll run through it all! I'll transfer some more from savings.")
    }
    
    // update savings
    spendLimit = 15
    
    // the spending statement "cash += 1" remained TRUE 
    if cash == spendLimit {
        print("You'll have to wash the dishes to leave this restaurant.")
        }
    }
}
print(getShoppingSpree())
// Slow down, cowboy. You'll run through it all! I'll transfer some more from my savings.
// You'll have to wash the dishes to leave this restaurant.  
``` 

The other variation of the while loop, known as the **repeat-while loop**, performs a single pass through the loop block first, **before** considering the loop's condition is false. 

``` swift 
var cash = 0
var spendLimit = 10
// reapeat-while loop
let evaluateAtEnd = { repeat {
    
    // spend a dollar
    cash += 1
    
    } while cash <= spendLimit
    print("You're outta loot, bub.")
}
print(evaluateAtEnd())
// You're outta loot, bub.
``` 

The loops condition **(while cash <= spendLimit)** is the same as before, but this time it's not evaluated **until the end of the first run through the loop**. 

![While-and-Do-While-flowchart_structure_loop](https://user-images.githubusercontent.com/109105989/196009744-4ae2ec1f-d7e2-4a50-8032-4755bb6ad116.png)

# References
Apple. (2022). *The Swift Programming Language* (5.7 Edition).  