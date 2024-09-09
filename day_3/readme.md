## day 3 | maximum subarray

```cpp
class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        int sol=nums[0];
        int maxi=nums[0];
        for (int i =1;i<nums.size();i++){
            maxi=max(maxi+nums[i],nums[i]);
            sol=max(sol,maxi);
        }
        return sol;
    }
};

int speedUp = [] {
    std::ios::sync_with_stdio(0);
    std::cin.tie(0);
    return 0;
}();
```
