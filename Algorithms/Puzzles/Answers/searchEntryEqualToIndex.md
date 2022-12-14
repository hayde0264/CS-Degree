# Search a sorted array for an entry equal to its index 

Design an algorithm that takes a sorted array of integers and returns an index (i) so that the element at index *i* equals *i*. 

For example: when the input is {-2, 0, 2, 4, 6, 7, 9}, the algorithm should return 2 or 3. 

**Solution** - rather than use a brute-force approach, opt for binary search 

**time** - O(log n) 

## In C++: 
```cpp 
  #include <vector>
  #include <iostream>
  using namespace std;
  
  
  int seachEntryEqualToIndex(const vector<int>& arr) {
          int low = 0;
          int high = arr.size() - 1;
          while (low <= high) {
                  int middle = low + ((high - low) / 2);
                  int difference = arr[middle] - middle;
                  if (difference == 0) {
                          return middle;
                  } else if (difference > 0) {
                          high = middle - 1;
                  } else {
                          low = middle + 1;
                  }
          }
          return -1;
  }
  ``` 
  
## In Java: 
```java 
          public static int searchEntryEqualToItsIndex(List<Integer> arr) {
                  int low = 0;
                  int high = arr.size() - 1;
                  int result = -1;
                  while (low <= high) {
                          int middle = low + ((high - low) / 2);
                          int difference = arr.get(middle) - middle;
                          if (difference == 0) {
                                  return middle;
                          } if (difference > 0) {
                                  high = middle - 1;
                          } else {
                                  low = middle - 1;
                          }
                  }
                  return result;
          }
``` 
# References 
Aziz, A. Lee, T. Prakash, A. (2015). *Elements of Programming Interviews in Java* (1st ed.). <https://www.amazon.com/Elements-Programming-Interviews-Questions-Tsung-Hsien/dp/B00C7F0V3W/ref=sr_1_1?crid=SU7GU68QNL5N&keywords=elements+of+programming+interviews+in+java+1st+edition&qid=1669594847&sprefix=elements+of+programming+interviews+in+java+1st+edition+%2Caps%2C72&sr=8-1> 
