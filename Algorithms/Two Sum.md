1.[Two Sum](https://leetcode.com/problems/two-sum/)
===========
>Given an array of integers, return indices of the two numbers such that they add up to a specific target.
>
>You may assume that each input would have exactly one solution.
>Example:
>>Given nums = [2, 7, 11, 15], target = 9,
>>
>>Because nums[0] + nums[1] = 2 + 7 = 9,
>>return [0, 1].


## My solutions:

```C++
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) 
    {
        int n = nums.size();
        vector<int> map;
        for(int i=0;i<n;i++)
        {   
            for(int j=++i;j<n;j++)
            {
                if(nums[i]+nums[j]==target) 
                {   map.push_back(i);
                    map.push_back(j);
                }
            }
        }
        return map;
    }
};
```