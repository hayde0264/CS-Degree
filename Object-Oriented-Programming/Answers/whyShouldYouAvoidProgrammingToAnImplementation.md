

 # Why should you avoid programming to an Implementation? 
  
 Avoid programming to an implementation because this forces you to code to a **concrete type**.
  
 ## Example of programming to a concrete type: 
 ```java                 
 Dog d = new Dog();                   
 d.bark();
 ```
 ## Refactor to an interface/supertype: 
 ```java          
 Animal animal = new Dog();
 animal.makeSound();
 ```
  
 # References 

Bates, B., Freeman, E., Robson, E., Sierra,    K. (2004). *Head First Design Patterns*. O'Reilly Media. <https://www.amazon.com/Head-First-Design-Patterns-Brain-Friendly/dp/0596007124/ref=d_pd_sbs_sccl_2_7/136-4263914-8338830?pd_rd_w=j9pLj&content-id=amzn1.sym.6ccaee5d-096a-4b4f-a8ba-f4ae5ec130a1&pf_rd_p=6ccaee5d-096a-4b4f-a8ba-f4ae5ec130a1&pf_rd_r=MYXZ6F5195T6T2W4DR7B&pd_rd_wg=MdrWa&pd_rd_r=7b160240-9299-47f7-81b9-e3b5456e3adb&pd_rd_i=0596007124&psc=1> 
