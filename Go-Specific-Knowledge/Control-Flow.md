# Control Flow 

Control flow allows programmers to make decisions based on the values of variables and constants.

Boolean values with operators are the **cornerstone of control flow**.  

## Operators in go: 
- *equal to* **(==)** 
- *not equal to*	**(!=)** 
- *less than* 	**(<)** 
- *less than or equal to* 	**(<=)** 
- **greater than** 		**(>)**
- *greater than or equal to* 	**(>=)** 
- *AND* 	**(&&)** 	- both operands must be true in order for the condition to evaluate to true 
- *OR* 	**(||)** 		- either operand must be true in order for the condition to evaluate to true 
- *NOT* 	**(!)** 		- reverses the boolean value - true becomes false and false becomes true 

## Booleans role in Control Flow
 
``` go 
// comparisons 
func comparisons() {s
	// == "equal to"
	num1 := 3
	fmt.Println(num1 == 3) // PRINTS - true

	num2 := 2
	fmt.Println(num2 == 5) // PRINTS - false

	// != "not equal to"
	num3 := 0
	fmt.Println(num3 != 4) // PRINTS - true

	num4 := 4
	fmt.Println(num4 != 4) // PRINTS - false

	// > "greater than"
	num5 := 11
	fmt.Println(num5 > 8) // PRINTS - true

	num6 := 23
	fmt.Println(num6 > 99) // PRINTS - false

	// >= "greater than or equal to"
	num7 := 3
	fmt.Println(num7 >= 3) // PRINTS - true

	num8 := 9
	fmt.Println(num8 >= 10) // PRINTS - false

	// < "less than"
	num9 := 3
	fmt.Println(num9 < 9) // PRINTS - true

	num10 := 4
	fmt.Println(num10 < 1) // PRINTS - false

	// <= "less than or equal to"
	num11 := 20
	fmt.Println(num11 <= 20) // PRINTS - true

	num12 := 25
	fmt.Println(num12 <= 30) // PRINTS - false
}
```  
## Go control flow constructs: 
- if/else  
- switch 
- for 

## If/Else 
An if/else statement basically says, **"do x if such-and-such is true; otherwise, do y."** 
 
``` go 
// if/else 
func ifElseExample(num int) {
	if num %2 == 0 {
		fmt.Println("The number is even")
		} else {
			fmt.Println("The number is odd")
	}	
}	// ifElseExample(num: 2) PRINTS - The number is even 
``` 

``` go 
// short circuiting if/else
func sunnyOutside() bool { 
	fmt.Println("Check if its sunny outside...")
	return true
}
func snowyOutside() bool {
	fmt.Println("Check if its snowy outside...")
	return true
}
func stormyOutside() bool { 
	fmt.Println("Check if the weather is dangerous...")
	return true
}

func goHike() { 
	if sunnyOutside() && !stormyOutside() {
		fmt.Println("Let's go for a hike!")
	}				
}	// PRINTS - Let's go for a hike!

func goSki() { // 5
	if snowyOutside() && !stormyOutside() {
		fmt.Println("Let's go for a ski!")
	}				
}	// PRINTS - Let's go for a ski!

func chooseEither() {
	if sunnyOutside() || snowyOutside() { 
		fmt.Println("You choose the activity.")
	}
}	// PRINTS - You choose the activity.
``` 

## Switch  
Switch is useful when you have **multiple conditions to evaluate**. Switch statements avoids writing redundant if/else statements. A switch statement is passed a variable whos value is compared **to each case value**. When a match is found, the corresponding block of statements become executed. 

``` go 
// switch
func talkWithCustomer(customerInput string) {
	switch customerInput {
	case "Hello":
		fmt.Println("Hey, I'm Dorthy the intelligent computer.")
	case "I have an issue":
		fmt.Println("Sorry, have you seen our customer service page?")
	case "I want to cancel my account":
		fmt.Println("Okay, go to the delete acount tab.")
	default:
		fmt.Println("I'm sorry I don't understand your message")
	}
}	// talkWithCustomer(customerInput: "I want to cancel my account") PRINTS - Okay, go to the delete tab
``` 

## For 
For statments are also called **loops**. 

## For statements contain: 
- a **init** statement: is executed befoer the first iteration starts 
- a **condition** expression: which is the expression evaluated before the iteration starts to determine if the iteration should continue
- a **operator** : which increments or decrements the inital statement


``` go 
// standard loops
func elementIncrement() {
	for i := 0; i < 5; i++ {
		fmt.Println(i)
	}
} // PRINTS - 0 1 2 3 4
func elementDecrement() {
	for i := 0; i >= 0; i-- {
		fmt.Println(i)
	}
} // PRINTS - 4 3 2 1 0
``` 
Besides using the **for** statement to perform a set of statements repeatedly, you often will use it to **iterate through sequences** to extract values. 

``` go 
// range loops
func forRange() {
	var Computers [3]string
	Computers[0] = "Dell"
	Computers[1] = "Mac"
	Computers[2] = "Microsoft"

	for index, value := range Computers {
		fmt.Println(index, value)
	}
} // PRINTS - 0 Dell 1 Mac 2 Windows
``` 
# References 
Lee, W. (2021). *Go Programming Langauge For Dummies*. John Wiley & Sons. <https://www.amazon.com/Programming-Language-Dummies-Wei-Meng-Lee-ebook/dp/B0921HHN48/ref=sr_1_7?crid=3DQARY10K4826&keywords=go+programming+language&qid=1666043979&qu=eyJxc2MiOiIzLjg2IiwicXNhIjoiMi45MSIsInFzcCI6IjIuMDcifQ%3D%3D&sprefix=go+programming+language%2Caps%2C76&sr=8-7>
