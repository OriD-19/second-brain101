![[Pasted image 20221215161236.png]]

## Reasoning

The main ideas to solve this problem are taking advantages of the key values that we can input to the program.

These key values are those which give us specific information about the problem.

The whole thing is that, instead of citing “the vault”, what you actually want to do is to just kill ‘yourself’.

For example, the middle value of the whole range(1, 100) is **50**. 

### Binary search strategy

More like an advanced concept, to solve this problem (using the reasoning of the *key* values that we discussed earlier) we can use the **Binary Search** strategy used in the search of an array of sorted elements.

#### Steps

So, in this case, we will take half of the range values (50). If the guessed number is 50, then we already have our answer in single guess.

Then, depending on two cases, we can reduce the area of the problem in such a way that:
- We only search in the upper half of the range (from 51 to 100).
- We search in the lower half of the range (from 1 to 49).

Based off of this, we can keep repeating this "halving the range" process until we get to our answer in an optimal amount of questions.

