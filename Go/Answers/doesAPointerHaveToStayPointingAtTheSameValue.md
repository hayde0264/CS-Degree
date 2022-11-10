# Does a pointer have to stay pointing at the same value? 

No, pointers **can** change the value to which they point. 


## For example: 
```go 
a := 30 // a is of type int 
b := &a // b is of type *int (pointer to int) 
c := &b // c is of type **int (pointer to pointer to int)

fmt.Println(a, *b, **c) // Prints - 30 30 30 
**c++ 
fmt.Println(a, *b, **c) // Prints - 31 31 31 
``` 


# References 
Summerfield, M. (2012, May 1). Programming in Go: Creating Applications for the 21st Century (Developer's Library) (1st ed.). Addison-Wesley Professional. https://www.amazon.com/Programming-Go-Creating-Applications-Developers-ebook/dp/B007Y6KDTG/ref=sr_1_5?crid=2S0HRDQDG9LCW&keywords=programming+in+go&qid=1668118234&sprefix=programming+in+go+%2Caps%2C95&sr=8-5
