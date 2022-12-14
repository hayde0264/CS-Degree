# Search a sorted array for the first occurrence of k 

**Solution** - use binary search to find the index of any element equal to the key (k). If (k) is not present, return -1. After finding such 
element, transverse backward from the middle to find the first occurrence of that element. 

**time for binary search** - O(log n) where n == number of entries in array 

## In C++: 
```cpp 
  #include <vector>
  
  using namespace std;
  
  int searchFirstForK(const vector<int>& arr, int key) {
          int low = 0;
          int high = arr.size() - 1;
          int result = -1;
          while (low <= high) {
                  int mid = low + ((high - low) / 2);
                  if (arr[mid] == key) {
                          return mid;
                  } else if (arr[mid] < key) {
                          low = mid + 1;
                  } else {
                          high = mid - 1;
                  }
          }
          return result;
  }
  ``` 
## In Java: 
```java 
          public static int searchFirstOfK(List<Integer> arr, int key) {
                  int low = 0;
                  int high = arr.size() - 1;
                  int result = -1;
                  while (low <= high) {
                          int mid = low + ((high - low) / 2);
                          if (arr.get(mid) == key) {
                                  return mid;
                          } if (arr.get(mid) < key) {
                                  low = mid + 1;
                          } else {
                                  high = mid - 1;
                          }
                  }
                  return result;
          }
```  


# References 
Aziz, A. Lee, T. Prakash, A. (2015). *Elements of Programming Interviews in Java* (1st ed.). <https://www.amazon.com/Elements-Programming-Interviews-Questions-Tsung-Hsien/dp/B00C7F0V3W/ref=sr_1_1?crid=SU7GU68QNL5N&keywords=elements+of+programming+interviews+in+java+1st+edition&qid=1669594847&sprefix=elements+of+programming+interviews+in+java+1st+edition+%2Caps%2C72&sr=8-1> 
