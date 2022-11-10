# What is the purpose of a constructor? 

A constructor is a **way to perform initialization** within a class. Constructors allow greater flexibility within your programs since
**you can call methods at run time to determine their initial values**. 

## Giving objects initialized variables: 
```java 
  
  public class ConstructorDemo {
    int i;
    String s;
    boolean v;
  
  
    public ConstructorDemo() {
      i = 1; // initalizing i
      s = "some string"; // initalizing s
      v = true; // initalizing v
    }
  
    public void printI() { System.out.println(i); }
    public void printS() { System.out.println(s); }
    public void printV() { System.out.println(v); }
  
    public static void main(String[] args) {
      ConstructorDemo d = new ConstructorDemo();
      d.printI(); // Prints - 1
      d.printS(); // Prints - some string
      d.printV(); // Prints - true
    }
  }
``` 

## Letting objects decide variables: 
```java 
 public class ConstructorDemo {
    int i;
    String s;
    boolean v;
  
  
    public ConstructorDemo(int i, String s, boolean v) {
      this.i = i; // let object instantiate 
      this.s = s; // let object instantiate 
      this.v = v; // let object instantiate 
    }
  
    public void printI() { System.out.println(i); }
    public void printS() { System.out.println(s); }
    public void printV() { System.out.println(v); }
  
    public static void main(String[] args) {
      ConstructorDemo d = new ConstructorDemo(3, "a string", false);
      d.printI(); // Prints - 3
      d.printS(); // Prints - a string
      d.printV(); // Prints - false
    }
``` 

  
# References 
Eckel, B. (2006, February 10). *Thinking in Java* (4th ed.). Pearson. <https://www.amazon.com/Thinking-Java-4th-Bruce-Eckel/dp/0131872486/ref=sr_1_1?crid=23ZTC7TRPPHR1&keywords=thinking+in+java&qid=1667521991&qu=eyJxc2MiOiIxLjg0IiwicXNhIjoiMC45NiIsInFzcCI6IjEuMTUifQ%3D%3D&sprefix=thinking+in+java%2Caps%2C87&sr=8-1>
