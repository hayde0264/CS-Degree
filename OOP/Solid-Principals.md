# Design Principals to implement 

==============
Principal One 
============== 
1. *Identify the aspects of your application that 
   vary and seperate them from your constants* 
## Take what variaes and "encapsulate" it from the rest of your code 
### Why?
This principal make it simpler to update (refactor) 
your code due to changes. Which creates more 
flexibility among your systems. 

=============
Principal Two
============= 
2. *Program to interfaces (protocols), not to implementations (structs or classes)* 
## Use protocols or interfaces to create methods, instead of placing them within a class. 
## Why? 
Placing methods within classes forces specific implementation, which prevents 
the ability for changing behavior, thus forcing you to write more code. If you 
use this pricipal, other objects can implement such methods because **such behaviors 
are not longer hidden in concrete classes**. Iterfaces allow you to **reuse** your code 
without the baggage that inheritance presents. Remember, by using iterfaces you can 
reference **polymorphically** rather than **concretely**. 

================
Principal Three 
================
3. *Prefer composition over inheritance*
## 
## Why? 


===============
Principal Four 
=============== 
4. *Seek to make loosely coupled designs between objects that interact* 
## 
## Why? 


===============
Principal Five
=============== 
5. *Classes or structs should be open for extension, but closen for modification* 
## 
## Why? 


==============
Principal Six 
==============
6. *Depend on abstractions, NOT concrete classes* 
## 
## Why? 


===============
Principal Seven
=============== 
7. *Principal of Least Knowledge- "only talk to your closests friends"* 
## 
## Why? 


================
Principal Eight
================ 
8. *The Hollywood principal- "don't call us, we'll call you"* 
## 
## Why? 


=============== 
Principal Nine 
=============== 
9. 























 



# References 
Bates, B., Freeman, E., Robson, E., Sierra, K. (2004). *Head First Design Patterns* 
	O'Reilly Media. <https://www.amazon.com/Head-First-Design-Patterns-Brain-Friendly/dp/0596007124> 
