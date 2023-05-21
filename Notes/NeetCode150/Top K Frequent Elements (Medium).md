For this problem, use a hash map to count all of the elements...

After that, we can use a **priority queue** to sort all of the elements by the count of each one. Finally, we can use the same priority queue to pop all *k* elements that we are looking for.

Code:
```cpp
vector<int> topKFrequent(vector<int>& nums, int k) {
    unordered_map<int, int> count;

    // Count all the repetition of all numbers
    for(auto a : nums)
        count[a]++;

    priority_queue<pair<int, int>, vector<pair<int, int>>, less<pair<int, int>>> pq;

    // Use the pq to sort them
    for(auto m : count)
        pq.push({m.second, m.first});

    vector<int> ans;

    // Store the ones that are most repeated
    while(pq.size()) {
        if(ans.size() == k) return ans;
        ans.push_back(pq.top().second);
        pq.pop();
    }

    return ans;

}
```
