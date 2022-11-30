# How long does memory exist in the free store? 

Objects within the free are available until **you explicitly state you are done** (by freeing such storage). For instance, 
if you reserve memory on the free store with a function, the memory will exist when the function returns (opposite of objects on the stack). 


# References 
Jones, B., Libert, J., Rao, Siddhartha. (2008, January 1). *Sams Teach Yourself C++ in One Hour a Day* (6th ed.). Sams. <https://www.amazon.com/Sams-Teach-Yourself-One-Hour/dp/0672329417/ref=sr_1_4?crid=2RB86BRDXC98Z&keywords=sams+teach+yourself+c%2B%2B+in+one+hour+a+day&qid=1669771498&sprefix=sams+teach+yourself+c%2B%2B+in+one+hour+a+day+%2Caps%2C72&sr=8-4> 
