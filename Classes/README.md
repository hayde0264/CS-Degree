# Classes 

A *class* **is a blueprint for which objects 
are created**.

## Classes contain: 
- **attributes** - which is data (social security number, date of birth, item name, item quantity). 

- **methods** - are behaviors within classes instantiated by invoking the method. They are commonly used to **get** (read) and **set** (write) data between classes and objects. (ex. getAge(), setAge(), getName(), setName()). 

``` java 
public class Classes {}

// ex. 1 
class Coffee { 
    // attributes (variable data of coffee)
    private String name;
    private Float price;

    // Methods (getters- allows instantiated objects to read data)
    public String getName() {
        return name;
    }
    public Float getPrice() {
        return price;
    }
    // (setters - allows instantiated objects to write data)
    public void setName(String name) {
        this.name = name;
    }
    public void setPrice(Float price) {
        this.price = price;
    }
}
```  

# References 
Oracle. (2022). *Lesson: Object-Oriented Programming Concepts*. <https://docs.oracle.com/javase/tutorial/java/concepts/index.html>  

Weisfeld, M. (January 1, 2003). *The Object-Oriented Thought Process*. Sams; 2ndedition. <https://www.amazon.com/Object-Oriented-Thought-Process-Matt-Weisfeld/dp/0672326116/ref=sr_1_6?crid=2VEMQXKI3JBVB&keywords=the+object+oriented+thought+process&qid=1666031958&qu=eyJxc2MiOiIxLjEzIiwicXNhIjoiMC42MCIsInFzcCI6IjEuMTUifQ%3D%3D&sprefix=the+object+oriented+%2Caps%2C87&sr=8-6>
