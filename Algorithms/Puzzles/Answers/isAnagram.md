# Is anagram? 

## In C++: 
```cpp 
  #include <iostream>
  
  using namespace std;
  
  int linearSearch(int arr[], int start, int end, int key) {
          for (int i = start; i < end; ++i) {
                  if (arr[i] == key) {
                          return i;
                  }
          }
          return -1;
  }
  
  
  int main() {
  
          int arr[] = {2, 4, 11, 25, 91};
          int arraySize = sizeof(arr)/sizeof(*arr);
  
          int key = 11;
          int test = linearSearch(arr, 0, arraySize - 1, key);
  
          test != -1 ? cout << "value found at index " << test : cout << "element not found";
  
          return 0;
  }
```

