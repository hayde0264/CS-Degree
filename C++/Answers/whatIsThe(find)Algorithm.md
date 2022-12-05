# What is the find algorithm? 

The find algorithm looks for the first element in a container that has a specified value. 


## Instance (with find): 
```cpp 
  #include <iostream>
  #include <algorithm>
  
  using namespace std;
  
  int main() {
  
          int arr[] = {11, 22, 31, 45, 10};
          int* ptr = find(arr, arr+5, 10);
                      
          cout << (ptr-arr); // Prints - 4 
          return 0;                     
  }                          
``` 

## Instance (without find): 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  int main() {
  
          int arr[] = {11, 22, 31, 45, 10};
           
          for (int i = 0; i <= 5; i++) {
                  if (arr[i] == 45) {
                          cout << i;
                          break;
                  }
          }
  
          // Prints - 3  
                     
          return 0;
  }       
  ``` 
  
  # References 
  Lafore, R. (2001, December 29). *Object Oriented Programming in C++* (4th ed.). Sams <https://www.amazon.com/Object-Oriented-Programming-4th-Robert-Lafore/dp/0672323087/ref=sr_1_1?crid=7MN18J4LOROL&keywords=object+oriented+programming+in+c%2B%2B&qid=1670203772&sprefix=object+oriented+programming+in+c%2B%2B%2Caps%2C77&sr=8-1>  
