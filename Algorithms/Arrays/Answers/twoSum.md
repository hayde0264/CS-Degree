# Two Sum 

Given an array of integers (arr) and an integer (key), return indices of the two numbers so that they add up to (key). 

# Ex. 1 
> Input: arr = [2, 5, 0, 8] target = 7 

> Ouput: [0, 1] (since arr[0] + arr[1] == 9] 

# Ex. 2 

> Input: arr = [1, 1, 6] target = 7 

> Output: [1, 2] 

## In C++: 
```cpp 
#include <unordered_map>
#include <vector>

// time: O(n)
// space: O(n)
class Test {
public:
    std::vector<int> twoSum(std::vector<int>& arr, int key) {
        std::unordered_map<int, int> m;
        for (int i = 0; i < arr.size(); ++i) {
            int t = key - arr[i];
            if (m.count(t)) return { m[t], i};
            m[arr[i]] = i;
        }
        return {};
    }
};
``` 

# References 
Leet Code. (2022). <https://leetcode.com>
