# What is the this keyword? 

The **this** keyword allows you to **reference a current instance of a class**. This is useful when, for instance, you would like to pass the current object **as a parameter to some method** or **to reference a field inside a current object without a name clash of a variable defined within the current block. 

## Example: 
```java 
  public class ThisDemo {
    public int age = 21; // instance variable
  
    public void friendAge() {
      int age = 23; // different age
  
      System.out.println("The local age is " + age);
      System.out.println("The age field is " + this.age);
    }
  
    public static void main(String[] args) {
      ThisDemo demo = new ThisDemo();
      demo.friendAge();
    }
  }
  /* OUTPUT 
  The local age is 23 
  The age field is 21
  */ 
``` 

# References 
Goodrich, M. Tamassia, R. (1994, January 1). *Data Structures and Algorithms in Java* (4th ed.). Wiley, John & Sons, Incorporated. <https://www.amazon.com/Michael-T-Goodrich-Structures-Algorithms/dp/B008UYJYF0/ref=sr_1_1?crid=1OJL9289EWZ94&keywords=data+structures+and+algorithms+in+java+4th+edition&qid=1667519269&qu=eyJxc2MiOiIwLjAwIiwicXNhIjoiMC4wMCIsInFzcCI6IjAuMDAifQ%3D%3D&sprefix=data+structures+and+algorithms+in+java+4th+edition%2Caps%2C83&sr=8-1> 
