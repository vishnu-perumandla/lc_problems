# smallest range I
```c++
class Solution {
public:
    int smallestRangeI(vector<int>& nums, int k) {
        int min=nums[0];
        int max=nums[0];
        for(auto i:nums){
            if(i<min){
                min=i;
            }
            if(i>max){
                max=i;
            }
        }
        min=min+k;
        if((max-k)<min){
            max=min;
        }
        else{
            max=max-k;
        }
        return max-min;
    }
};
```