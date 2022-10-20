# For

The keyword **for** is often identified in programming as a **loop**. Why is it called a loop? Loops earn their name through their behavior. Loops continually iterate (or **loop**) through sections of code **until a specified condition becomes satisfied**. 

> "Rather than say, **"until a condition is satisfied"**, which is ambiguous, you can save yourself time if you realize that for loops and as well as other control-flow paradigms such (if/else, while, switch) execute based upon **booleans**. 

<img align="right" src="https://user-images.githubusercontent.com/109105989/196835097-4ff631fc-dcff-46a5-a3e5-e2a68e197447.png">

Notice in the picture as long as a task is still running, loops consider this state **true**. Once a task finishes, the loop considers the task to be **false**, thus ending the process. " 

Developers depend upon the for loop to scan through a clump of data and, once complete, reveal or alter such data. 

Below I will instantiate an array containing elements. To retrieve the elements within the array, I can instruct my for loop to **loop** through the array **until all the elements are accessed**" at this point, the **condition is considered false**, so the program will end. 

For instance, below, I'll create a **constant array of Strings**, which give the for loop **the task of iterating through such data**. I'll ASK the for loop to acknowledge each item within the warehouse (taskInProgress == true), and once it's finished (taskInProgress == false), let me know what you found. 

## In Java: 
``` java 
public static void main(String[] args) {
   String[] inventory = {"anchors", "fire extinguishers", "catamaran sails"};
   for (String item: inventory) {
        System.out.println(item);
   }
}  // Prints - anchors fire extinguishers catamaran sails
``` 

## In Go:
``` go 
func forSimple() {
        inventory := []string{"anchors", "fire extinguishers", "catamaran sails"}
        for item := range inventory {
                fmt.Println(item)
        }
}  // Prints - anchors fire extinguishers catamaran sails 
``` 

## In Kotlin: 
``` kotlin 
fun forSimple() {
        inventory := []string{"anchors", "fire extinguishers", "catamaran sails"}
        for item := range inventory {
                fmt.Println(item)
        }
}  // Prints - anchors fire extinguishers catamaran sails
``` 

## In Swift: 
``` swift 
func forSimple() {
    let inventory = ["anchors", "fire extinguishers", "catamaran sails"]
    for item in inventory {
        print(item)
    }
}  // Prints - anchors fire extinguishers catamaran sails 
``` 



  


# References 
For loop. (2022, October 16). *Wikipedia*. <https://en.wikipedia.org/wiki/For_loop> 
