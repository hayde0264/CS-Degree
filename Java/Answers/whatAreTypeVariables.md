# What are type variables? 

Type variables (**<>**) indicate that a class handles **generics**, which means the programmer must enter a type at runtime. 

## In Classes:
```java 
public class List<E> { 
  ... 
  public void add(E element) {...} 
  public E get(int i) {...} 
} 

List<String> stringList; 

List<String> initiatedStringList = new ArrayList<>(); 

}
``` 
In this instance, the List class refers to the type variable with its body and methods **as if it were a real type** to be substituted later. 



# Visually: 
![typeVariable](https://user-images.githubusercontent.com/109105989/200458659-887729e1-d772-4103-bbf3-262753167476.png)





# References 
Leuck, D. & Niemeyer, P. (2014). *Learning Java*. O'Reilly. <https://www.amazon.com/Learning-Java-Bestselling-Hands-Tutorial/dp/1449319246/ref=sr_1_4?crid=3FZWUTVUHYMQZ&keywords=learning+java&qid=1667345409&qu=eyJxc2MiOiIyLjU2IiwicXNhIjoiMi4yMCIsInFzcCI6IjIuMDQifQ%3D%3D&sprefix=learning+java%2Caps%2C84&sr=8-4>
