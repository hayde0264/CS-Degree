# How do you create a for loop with a pointer? 

## Example: 
```cpp 
  #include <iostream>
  
  
  using namespace std;
  
  
  int main() {
          // numbers of elements an array can hold (notice ssize_t keyword)
          const ssize_t array_size = 5;
          int some_array[array_size] = {3, 2, 4, 5, 2};
  
          // start (points to first element) && end (point to last element)
          for (int *start = some_array, *end = some_array + array_size; start != end; ++start)
                  cout << *start << " "; // Prints - 3 2 4 5 2
  
          return 0;
  }
```


