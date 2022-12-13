# Missing element in sorted array 


# In C++: 
```cpp 
#include <vector>

using namespace std;

// time: O(logn)
// space: O(1)
class Test {
public:
    int missingElement(vector<int>& arr, int i) {
        int low = 0;
        int high = arr.size() - 1;
        while (low <= high) {
            const auto& mid = low + (high - low) / 2;
            if (!check(arr, i, mid)) {
                high = mid - 1;
            } else {
                low = mid + 1;
            }
        }
        return arr[high] + (i - missingCount(arr, high));
    }
    
private:
    int missingCount(const vector<int>& arr, int i) {
        return (arr[i] - arr[0] + 1) - (i - 0 + 1);
    }
    bool check(const vector<int>& arr, int i, int j) {
        return i > missingCount(arr, i);
    }
};
``` 



