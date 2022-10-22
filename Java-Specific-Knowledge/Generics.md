# Generics 

Generics enable types (classes and interfaces) **to be parameters when defining classes, interfaces and methods**. 

Type parameters provide a way for you to **re-use the same code with different inputs**. 

# Why use generic code? 
- stronger type checks at compile time. (Fixing compile-time errors is easier than fixing runtime errors). 
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

Notice that all occurrences of **Object are replaced by T**. A type var

