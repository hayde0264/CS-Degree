# Generics 

Generics enable types (classes and interfaces) **to be parameters when defining classes, interfaces and methods**. 

Type parameters provide a way for you to **re-use the same code with different inputs**. 

# Why use generic code? 
-stronger type checks at compile time. (Fixing compile-time errors is easier than fixing runtime errors). 
- elimination of casts 

>"By using generics, a programmer may implement algorithms that work on collections of different types, can be customized, and are type safe while also creating easier-to-read code." 

## An example without generics: 
``` java 
  List list = new ArrayList();
  list.add("Hi");
  String s = (String) list.get(0); // notice the cast
``` 

## An example with generics: 
``` java 
  List<String> list = new ArrayList<String>();
  list.add("Hi");
  String s = list.get(0); // notice NO cast
``` 

# Generic Types 
A **generic type** is a generic class or interface that is parameterized over types. 

The following **Box** class with be modified to explain. 

``` java 
class Box { 
    private Object obj;
    
    public void get(Object obj) { this.obj = obj; }
    public Object set(Object obj) { return obj; }
}
``` 

Since this class's methods **accept or return an Object, you are free to pass in whatever you want, as long as it is not a primitive type**. There is no way to verify, at compile time, how the class is sued. One part of the code may place an **Integer** in the box and expect to get objects of type **Integer** out of it, while another part of the code may mistakenly pass in a **String**, resulting in a runtime error. 

## A Generic Version of the Box Class: 
``` java 
class GenericBox<T> { 
    // T stands for "Type" 
    private T t;

    public void setT(T t) { this.t = t; }
    public T getT() { return t; }
}
``` 

Notice that all occurrences of **Object are replaced by T**. A type variable can be any non-primitive type you specify: any class type, any interface type, or even another variable type. 

# Type Parameter Naming Conventions 
By convention, type parameter names are **single, uppercase letters**. This stands in sharp contrast to the variable naming conventions, and with good reason: without this convention, it would be difficult to differentiate between a type variable and an ordinary class or interface name. 

## The most commonly used type parameter names are: 
- **E** - Element 
- **K** - Key 
- **N** - Number 
- **T** - Type 
- **V** - Value 
- **S,U,V etc.** - 2nd, 3rd, 4th types

# Invoking and Instantiate a Generic Type 
To referne the generic **Box** class from within your code, you must perform a generic type invocation, which **replaces T with some concrete value, such as Integer**: 

``` java 
Box<Integer> intBox; 
``` 

You can think of a generic type invocation as **being similar to an ordinary method invocation, but instead of passing an argument to a method, you are passing a type argument - Integer in this case - to the Box class itself**. 

Like any other variable declaration, this code **does not actually create a new Box object**. It simply declares that **intBox will hold a reference to a "Box of Integer," which is how Box<Integer> is read**. 

To instantiate this class, **use the new keyword, as usual, but place <Integer>** between the class name and the parenthesis: 
``` java 
Box<Integer> intBox = new Box<Integer>(); 
``` 

# Type Inference and Generic Methods 
**Type inference** is a Java compiler's ability to **look at each method invocation and corresponding declaration to determine the type argument(s) that make the applicable invocation**. The inference algorithm determines the types of the arguments and, if available, **the type that the result is being assigned or returned**. 

In the following example, inference determines that the second argument passed to the pick method is of type **Serializable**: 
``` java 
class TypeInference<T> {
    static <T> T pick(T a, T b) { return b; }
    Serializable s = pick("F", new ArrayList<String>());
}
``` 

Generic methods enable you to **invoke a generic method as you would an ordinary method, but without specifying a type between angle brackets**. 

## Notice how BoxDemo, requires the GenericBox class:
``` java 
class GenericBox<T> {
    // T stands for "Type"
    private T t;

    public void setType(T t) { this.t = t; }
    public T getType() { return t; }
}

// Using Generic Classes within Classes
class BoxDemo {
    public static <U> void addBox(U u, java.util.List<GenericBox<U>> boxes) {
        GenericBox<U> box = new GenericBox<>();
        box.setType(u) ;
        boxes.add(box);
    }

    public static <U> void outputBoxes(java.util.List<GenericBox<U>> boxes) {
        int count = 0;
        for (GenericBox<U> box : boxes) {
            U boxContents = box.getType();
            System.out.println(" Box #: " + count + "contains [" + boxContents.toString() + "]");
            count++;
        }
    }

    public static void main(String[] args) {
        java.util.ArrayList<GenericBox<Integer>> listOfIntBoxes = new java.util.ArrayList<>();
        BoxDemo.<Integer>addBox(Integer.valueOf(10), listOfIntBoxes);
        BoxDemo.addBox(Integer.valueOf(20), listOfIntBoxes);
        BoxDemo.addBox(Integer.valueOf(30), listOfIntBoxes);
        BoxDemo.outputBoxes(listOfIntBoxes);
    }
}
/* Output: 
Box #0 contains [10] 
Box #1 contains [20] 
Box #2 contains [30]  
*/
``` 

# References 
