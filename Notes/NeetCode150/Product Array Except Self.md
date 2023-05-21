The trick for this problem is using a **Prefix Product** and **Suffix Product** arrays.
This way, we can process each part of the input in the following way:

- Taking the *ith* element of the array of `nums`, we can find the product of all elements except such item with the formula:
    `prefix[i - 1] * suffix[i + 1]`
Notice that the indices can be out of bound, so we have to manage that.

For processing each array separately, we just need to append the products of the `nums` array as follows:
- For the prefix, just do a normal prefix product.
- For the suffix, reverse iterate the original array, keeping track of the product and appending the results in reverse order.

## Code
```cpp
vector<int> productExceptSelf(vector<int>& nums) {

    // Use the prefix product and suffix product technique

    vector<int> prefix, suffix(nums.size()), ans;

    for(int i = 0; i < nums.size(); i++) {
        if(prefix.size() == 0) prefix.push_back(nums[i]);
        else prefix.push_back(prefix[i - 1] * nums[i]);
    }

    int stored = 1;

    for(int i = nums.size() - 1; i >= 0; i--) {
        stored *= nums[i];
        suffix[i] = stored;
    }

    for(int i = 0; i < nums.size(); i++) {
        if(i == 0) ans.push_back(suffix[i + 1]);
        else if(i == nums.size() - 1) ans.push_back(prefix[i - 1]);
        else ans.push_back(prefix[i - 1] * suffix[i + 1]);
    }

    return ans;

}
```
