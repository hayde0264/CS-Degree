# Search 2D sorted array 


Design an algorithm that takes a 2D sorted array and a number and checks whether that number appears within the array. 

**Solution** - let the 2D array be A, and the input number be x. Binary search can be performed on each row independently with a 
time complexity of O(m log n), where *m* is the number of rows and *n* is the number of columns. 


## In C++: 
```cpp 
  #include <vector>
  #include <iostream>
  using namespace std;
  
  static bool matrixSearch(const vector<vector<int>>& arr, int key) {
          int row = 0;
          int column = arr[0].size() - 1;
          while (row < arr.size() && column >= 0) {
                  if (arr[row][column] == key) {
                          return true; 
                  } else if (arr[row][column] < key) {
                          ++row;
                  } else {
                          --column;
                  }
          }
          return false;
  }
``` 

## In Java: 
```java 
  import java.util.List;
                                       
  public class Test {
          public static boolean SearchMatrix(List<List<Integer>> arr, int key) {
                  int row = 0;
                  int column = arr.get(0).size() - 1;
                  while (row < arr.size() && column >= 0) {
                          return true;
                  } if (arr.get(row).get(column) < key) {     
                          ++row; 
                  } else {
                          --column;
                  }
          return false;  
          } 
  }
``` 


# References 
Aziz, A. Lee, T. Prakash, A. (2015). *Elements of Programming Interviews in Java* (1st ed.). <https://www.amazon.com/Elements-Programming-Interviews-Questions-Tsung-Hsien/dp/B00C7F0V3W/ref=sr_1_1?crid=SU7GU68QNL5N&keywords=elements+of+programming+interviews+in+java+1st+edition&qid=1669594847&sprefix=elements+of+programming+interviews+in+java+1st+edition+%2Caps%2C72&sr=8-1> 

