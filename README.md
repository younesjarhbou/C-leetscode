# C-leetscode

#1
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        int first_index, second_index, i = -1, j;
        vector<int> result;
        
        result.reserve(2);
        while (++i < nums.size())
        {
            j = i;
            while (++j < nums.size())
            {
                if(nums.at(i) + nums.at(j) == target)
                {
                    result.push_back(i);
                    result.push_back(j);
                    break;
                }
            }
        }
        return (result);
    }
};


///saved for later
