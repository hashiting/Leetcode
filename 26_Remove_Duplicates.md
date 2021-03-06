> Q:Given a sorted array, remove the duplicates in place such that each element appear only once and return the new length.

> Do not allocate extra space for another array, you must do this in place with constant memory.

> For example,
> Given input array nums = [1,1,2],

> Your function should return length = 2, with the first two elements of nums being 1 and 2 respectively. It doesn't matter what you leave beyond the new length.

> Solution:

```C++
int removeDuplicates(vector<int>& nums) {
        int initial = 0;
        if(nums.size() == 0) return 0;
        initial = nums[0];
        vector<int>::iterator it = nums.begin()+1;
        for(;it != nums.end();it++){
            if(*it != initial){
                initial = *it;
            }
            else{
                nums.erase(it);
                it--;
            }
        }
        return nums.size();
}
```

> The key is to use the iteration of vector and remember i-- when you erase a element cause position i have been replace.
