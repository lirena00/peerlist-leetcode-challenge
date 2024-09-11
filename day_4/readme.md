## day 4 | product of array except self

```cpp
class Solution {
public:
    vector<int> productExceptSelf(vector<int>& nums) {
        int n = nums.size();
        vector<int> product(n, 1);
        vector<int> prefix(n, 1);

        for (int i = 1; i < n; i++) {
            prefix[i] = prefix[i - 1] * nums[i - 1];
        }

        int suffixproduct = 1;
        for (int i = n - 1; i >= 0; i--) {
            product[i] = suffixproduct * prefix[i];
            suffixproduct *= nums[i];
        }

        return product;
    }
};
```
