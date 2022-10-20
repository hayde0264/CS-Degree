# For

The keyword **for** is often identified in programming as a **loop**. Why is it called a loop? Loops earn their name through their behavior. Loops continually iterate (or **loop**) through sections of code **until a specified condition becomes satisfied**. 

Below I will instantiate an array containing elements. To retrieve the elements within the array, I can instruct my for loop to **loop** through the array **until all the elements are accessed**", at this point the **condition is consideredsatisfied** so the program will complete. 

> "Rather than say, **"until a condition is satisfied"**, which is ambigous for new developers if you realize that for loops and as well as other control-flow paridgms such (if/else, while, switch) execute based upon **booleans** the concepts become lucid. 

A major job developers ask of the for loop is to scan through a clump of data and and once finished returning such data. 

For instance, below, I'll create an **constant array of Strings** for holding the names of items within the warehouse. I'll then create a for loop asking it to print out the items we have in stock. 

## In Java: 
``` java 
public static void main(String[] args) {
   String[] inventory = {"anchors", "fire extinguishers", "catamaran sails"};
   for (String item: inventory) {
        System.out.println(item);
   }
}// Prints - anchors fire extinguishers catamaran sails
``` 

## In Go:
``` go 
func forSimple() {
        inventory := []string{"anchors", "fire extinguishers", "catamaran sails"}
        for item := range inventory {
                fmt.Println(item)
        }
}// Prints - anchors fire extinguishers catamaran sails 
``` 

## In Kotlin: 
``` kotlin 
fun forSimple() {
        inventory := []string{"anchors", "fire extinguishers", "catamaran sails"}
        for item := range inventory {
                fmt.Println(item)
        }
}// Prints - anchors fire extinguishers catamaran sails
``` 

## In Swift: 
``` swift 
func forSimple() {
    let inventory = ["anchors", "fire extinguishers", "catamaran sails"]
    for item in inventory {
        print(item)
    }
}// Prints - anchors fire extinguishers catamaran sails 
``` 



  


# References 
For loop. (2022, October 16). *Wikipedia*. <https://en.wikipedia.org/wiki/For_loop> 
