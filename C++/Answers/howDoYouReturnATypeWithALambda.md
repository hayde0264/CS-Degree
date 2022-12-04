# How do you return a type with a lambda? 

  #include <iostream>
  
  using namespace std;
  
  int main() {
  
          auto add = [] (int a, int b) -> int {
                  return a + b;
          };
  
          cout << add(1, 2); // Prints - 3  
          return 0;          
                             
  }      
