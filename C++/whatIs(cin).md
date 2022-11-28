# What is (cin)? 

**cin** - is an **istream** object which is used to receive input 

## For example: 
```cpp 
#include <iostream>
  
using namespace std;
  
  
int main() {
        const char NAMELIMIT = 20;
        char name[NAMELIMIT];
  
        cout << "what's your name?" << '\n';
        cin >> name;
        cout << '\n';
        cout << "its nice to meet you " << name;
        return 0;
}
``` 

## Output: 
![Screen Shot 2022-11-28 at 6 37 46 PM](https://user-images.githubusercontent.com/109105989/204403301-5b4e237e-91ee-4311-9cd3-92a4296e794d.png)




# References 
Lajolie, J., Lippman, S., Moo, B. (2005, January 1). *C++ Primer* (4th ed.). Addison-Wesley Professional. <https://www.amazon.com/Primer-4th-Stanley-B-Lippman/dp/0201721481/ref=tmm_pap_swatch_0?_encoding=UTF8&qid=1669678717&sr=8-4> 
