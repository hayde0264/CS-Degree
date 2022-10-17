Control flow allows programmers to make decisions based on the values of variables and constants.

Boolean values are the **cornerstone of control flow**.  

## Go control flow constructs: 
- if/else  
- switch 
- for 

## If/Else 
An if/else statement basically says, **"do x if such-and-such is true; otherwise, do y."** 

## Booleans with operators: 
``` go 
func comparisons() {
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

## If/Else 
``` go 
func ifElseExample(num int) {
	if num%2 == 0 {
		fmt.Println("The number is even")
	} else {
		fmt.Println("The number is odd")
	}
}
``` 

## Short Circuiting
``` go 
func sunnyOutside() bool { // 1
	fmt.Println("Check if its sunny outside...")
	return true
}
func snowyOutside() bool { // 2
	fmt.Println("Check if its snowy outside...")
	return true
}
func stormyOutside() bool { // 3
	fmt.Println("Check if the weather is dangerous...")
	return true
}

func goHike() { // 4
	if sunnyOutside() && !stormyOutside() {
		fmt.Println("Let's go for a hike!")
	}
}

func goSki() { // 5
	if snowyOutside() && !stormyOutside() {
		fmt.Println("Let's go for a ski!")
	}
}

func chooseEither() {
	if sunnyOutside() || snowyOutside() { // 6
		fmt.Println("You choose the activity")
	}
}
``` 

## Switch 
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
}
``` 

## For 
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

