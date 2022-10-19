# Why should you program to interfaces, not implementations? 

1. Clients remain unaware of the specific types of objects they use  
2. Clients remain unaware of the classes that implement these objects. Clients only 
   know about the abstract class(es) defining the interface. 

### This will reduce the dependencies between susbsystems, which aids code resuse.

## What can you do about it? 
Don't declare variables to be instances of classes. Instead, 
commit only to an interface defined by an abstract class. 

# References  
Gamma, H. Helm, R. Johnson, R. Vissides, J. (1994, October 31) *Design Patterns: Elements of Resusable Object-Oriented Software*. Addison-Wesley Professional. <https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612/ref=sr_1_1?crid=1WYDG0P22KC4I&keywords=design+patterns&qid=1665371243&qu=eyJxc2MiOiIyLjY4IiwicXNhIjoiMS45NCIsInFzcCI6IjIuMDEifQ%3D%3D&sprefix=design+pattern%2Caps%2C242&sr=8-1>
