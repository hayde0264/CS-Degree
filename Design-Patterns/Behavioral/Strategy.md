# Strategy Pattern 

Class: **Behavioral** 

The *strategy design pattern* is a behavioral software design pattern 
that enables the programmer **to select an algorithm at runtime**. Rather 
than use a single algorithm directly, objects can receive run-time instructs 
as to which algorihtm to implement.

### Remember to progrogram to interfaces, not implementations  

## How does it work? 
To adhere to the strategy pattern, behaviors of classes **should not** 
be inhereited. Instead, behaviors should be **encapsulated with interfaces**.
This references that open/closed principal, which states classes **should be 
open for extension but closed for modification**. The strategy pattern uses 
composition (has - a) instead of inheritance (is - a). 

### Steps 
- Seperate behaviors into seperate interfaces 
- Create classes that implement such behaviors  
- Create an abstract class that references each interface 
- Extend the abstract class with concrete examples 

![Strategy-Pattern](https://user-images.githubusercontent.com/109105989/194192512-b21efbe6-0343-45b5-bf0d-e1946e158c5a.png)


``` java 
abstract class Programmer {
    CodingStyle codingStyle;
    Programmer() {}

    public void setCodingStyle(CodingStyle codingStyle) {
        this.codingStyle = codingStyle;
    }
    public void getCodingStyle () {
        codingStyle.style();
    }
    public void hasNotBeenEvaluated() {
        System.out.println("This employee's code has not yet been evaluated");
    }
}
interface CodingStyle {
    public void style();
}
class MessyCode implements CodingStyle {
    @Override
    public void style() {
        System.out.println("Anyone want spaghetti?");
    }
}
class CleanCode implements CodingStyle {
    @Override
    public void style() {
        System.out.println("They certainly read Clean Code by Robert Martin");
    }
}
class Jennie extends Programmer {
    public Jennie() {
        codingStyle = new CleanCode();
    }
}
class Ben extends Programmer {
    public Ben() {
        codingStyle = new MessyCode();
    }
}
class EmployeesOverall {

    public static void main(String[] args) {
        Programmer jenny = new Jennie();
        jenny.getCodingStyle();

        Programmer ben = new Ben();
        ben.getCodingStyle();
        ben.setCodingStyle(new CleanCode());
    }

}
``` 

``` go 


``` 

``` swift 

``` 

``` kotlin 


``` 

# References 
Wikipedia. (2022, August 26). *Strategy Pattern*. <https://en.wikipedia.org/wiki/Strategy_pattern> 

