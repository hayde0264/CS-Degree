# Operators 


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
