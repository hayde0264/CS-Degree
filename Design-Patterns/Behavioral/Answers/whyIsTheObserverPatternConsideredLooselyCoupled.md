


  
 # Why is the Observer Pattern considered loosely coupled? 
  
  
 ## The Observer Pattern is loosely coupled because: 
 - The only thing subjects know about observers is that **they implement a certain interface**.
 - Since the only thing the Subject depends on is the **list of objects that implement the Observer interface**, so we can **remove** or **add** observers whenever we'd like.
 - We never need to modify the subject **to add new types of observers**.
 - We can **reuse** subjects or objects while remaining **independent from each other**.
 - Changes to the Subject or the Observer **will not affect each other**.
  
 # References 
Bates, B., Freeman, E., Robson, E., Sierra, K. (2004). *Head First Design Patterns*. O'Reilly Media. <https://www.amazon.com/Head-First-Design-Patterns-Brain-Friendly/dp/0596007124/ref=d_pd_sbs_sccl_2_7/136-4263914-8338830?pd_rd_w=j9pLj&content-id=amzn1.sym.6ccaee5d-096a-4b4f-a8ba-f4ae5ec130a1&pf_rd_p=6ccaee5d-096a-4b4f-a8ba-f4ae5ec130a1&pf_rd_r=MYXZ6F5195T6T2W4DR7B&pd_rd_wg=MdrWa&pd_rd_r=7b160240-9299-47f7-81b9-e3b5456e3adb&pd_rd_i=0596007124&psc=1> 

