#Bronze #USACO

Problem link: [USACO](http://www.usaco.org/index.php?page=viewproblem2&cpid=526)

---

For this problem, we can use an auxiliary string to evaluate the number of repetitions from the original `S` string.

The idea is to copy the characters, and evaluate them individually. The comparison occurs with the string `T`, as expected.

So, we iterate through the whole set of characters of `S`, and then we search for the occurrences of `T` when they happen at the end of the string. This way, we avoid searching the whole string back to back in `O(n^2)`, because the problem constraints do not allow such complexity.

Code:
```cpp
#include <bits/stdc++.h>

using namespace std;

int main() {

  freopen("censor.in", "r", stdin);
  freopen("censor.out", "w", stdout);

  string s, t; cin >> s >> t;

  string censored;

  int k = t.size();

  for(auto a : s) {

    censored += a;
    int n = censored.size();

    if(n >= k && censored.substr(n - k) == t) {
      censored.resize(n - k);
    }

  }

  cout << censored;
  return 0;

}

```

Notes:
- The use of `string.resize()` instead of substring, which is way faster!