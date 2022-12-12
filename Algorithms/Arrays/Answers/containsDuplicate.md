# Contains Duplicate 

Given an array of integers <code>arr</code>, return <code>true</code> if any value appears twice within the array; return <code>false</false> if there are no repeats within the array. 

## Ex. 1: 
> Input: arr = [2, 3, 4, 2] 

> Output: true 

## Ex. 2: 
> Input: arr = [1, 2, 3, 4] 

> Output: false 


## In C++: 
```cpp 
#include "iostream"
#include <vector>
#include <unordered_set>

using namespace std;

// time: O(n)
// space: O(n)
class Test {
public:
    bool containsDuplicate(vector<int>& arr) {
        unordered_set<int> s(begin(arr), end(arr));
        return s.size() != arr.size();
    }
};
``` 


# References 
Valeo, S. (2021). *C by Example*. <https://www.wbyexample.com> 
