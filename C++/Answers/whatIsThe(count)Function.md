# What is the count function? 

## Paramters: 
- **first** : Input Iterator 
- **last**  : Input Iterator 
- **val**   : const T& 
  
## Output: 
- **the number of elements within the range [first, last] that compare equal to val** 
  
## For example: 
```cpp 
  #include <iostream>
  #include <algorithm>
  #include <vector>
  
  using namespace std;
  
  
  int main() {
          // counting elements in an array
          int some_ints[] = {19, 42, 56, 12, 52}; // 5 elements
          int get_count = count(some_ints, some_ints + 5, 12);
          cout << "12 appears " << get_count << " time(s)." << '\n';
  
          // counting elements of a container
          vector<int> some_vector (some_ints, some_ints + 5);
          get_count = count(some_vector.begin(), some_vector.end(), 42);
          cout << "42 appears " << get_count << " time(s).";
  
          return 0;
          /* OUTPUT 
          12 appears 1 time(s).
          42 appears 1 time(s).
          */
  }
```
  
## Function template: 
  ```cpp 
    template <class InputIterator, class T>
         typename iterator_traits<InputIterator>::difference_type
          count (InputIterator first, InputIterator last, const T& val)
  {       
         typename iterator_traits<InputIterator>::difference_type ret = 0;
          while (first != last) {
                  if (*first == val) ++ret;
                  ++first;
          }       
          return ret;
  } 
```
  

# References 
Reference. (2022). *cplusplus*. <https://cplusplus.com/reference> 
  
