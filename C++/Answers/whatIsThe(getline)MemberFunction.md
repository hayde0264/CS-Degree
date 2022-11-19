# What is the get line member function? 

The getline() member function is used to **read a full line of data from an input file**. The function returns **a reference to the input file**.

## Its parameters include: 
- **buffer** - which stores the data that has been read 
- **len** - which get the length of the buffer in bytes 
- **delim** - which is the character used to signal the end of the line 

## Syntax 
```cpp 
istream &getline(char *buffer, int len, char delim = '\n') 
```




# References 
Oualline, S. (2003, January 1). *Practical C++ Programming* (2nd ed.). O'Reilly Media. <https://www.amazon.com/Practical-Programming-Second-Steve-Oualline/dp/0596004192/ref=sr_1_1?crid=YRU9QTDSQNLT&keywords=practical+c%2B%2B+programming&qid=1668720881&sprefix=%2Caps%2C56&sr=8-1>
