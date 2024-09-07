## Day-1 Two Sum Problem

```cpp
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        unordered_map<int, int> num_to_index;
        vector<int> result;

        for (int i = 0; i < nums.size(); ++i) {
            int complement = target - nums[i];

            if (num_to_index.find(complement) != num_to_index.end()) {
                result.push_back(num_to_index[complement]);
                result.push_back(i);
                return result;
            }

            num_to_index[nums[i]] = i;
        }

        return result;
    }
};
```
