# What is the purpose of the append method? 

The built-in function **append()** takes a slice with one or more values, and **returns a new slice assuming you've added values**. 

## For instance: 
```go 
  package main
  
  
  import (
    "fmt"
  )
  
  func main() {
    a := []string{"a", "b", "c"}
    b := []string{"X", "Y", "Z"}
  
  
    individual:= append(a,"d", "e", "f") // appends individual values
    appendDeclaredSlice := append(a, b...) // appends all of the b's values
    appendCertainElements := append(a, b[0:1]...) // appends subslice
  
    fmt.Printf("%s \n %s \n %s", individual, appendDeclaredSlice, appendCertainElements)
    /* OUTPUTS 
    [a b c d e f] 
    [a b c X Y Z] 
    [a b c X]
    */ 
  }
``` 

# References 
Summerfield, M. (2012, May 1). Programming in Go: Creating Applications for the 21st Century (1st ed.). Addison-Wesley Professional. https://www.amazon.com/Programming-Go-Creating-Applications-Developers-ebook/dp/B007Y6KDTG/ref=sr_1_1?crid=84JN5Z7QKJEE&keywords=programming+in+go+mark&qid=1668300545&sprefix=programming+in+go+mark+%2Caps%2C82&sr=8-1

