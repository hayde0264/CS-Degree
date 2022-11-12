# Can you use pointers with value types? 

You **can** use pointers with value types whenever you'd like to modify values of **non-reference type**. 

Go provides two keywords for creating variables and setting pointers to them: the **new()** function and the **address of operator**. 

## For instance: 
```go 

  package main
  
  
  import (
    "fmt"
  )
  
  type pal struct {
    name string
    birthYear int
  }
  
  func main() {
  grayson := pal{"Grayson", 2002} // pal value
  
  olivia := new(pal) // pointer to pal (notice new())
  olivia.name, olivia.birthYear = "Olivia", 2000
  
  sophie := &pal{} // pointer to pal (notice &)
  sophie.name, sophie.birthYear = "Sophie", 2001
  
  marty := &pal{"Marty", 2002} // pointer to pal
  
  fmt.Println(grayson)
  fmt.Println(olivia, sophie, marty)
  
  /* OUTPUTS 
  {Grayson 2002}
  &{Olivia 2000} &{Sophie 2001} &{Marty 2002}
  */
  }
``` 

# References 
Summerfield, M. (2012, May 1). Programming in Go: Creating Applications for the 21st Century (Developer's Library) (1st ed.). Addison-Wesley Professional. https://www.amazon.com/Programming-Go-Creating-Applications-Developers-ebook/dp/B007Y6KDTG/ref=sr_1_5?crid=2S0HRDQDG9LCW&keywords=programming+in+go&qid=1668118234&sprefix=programming+in+go+%2Caps%2C95&sr=8-5

