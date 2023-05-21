![[Pasted image 20221216160124.png]]

## 1. Algorithm

For solving this problem, the process is quite easy.

We only need to determine whether or not the input number $n$ is prime, which also means that is only divisible by 1 and $n$.

With this information, if we can get all the divisors of a number, and determine that it only has two divisors, then we have all the data we needed to answer the main question.

## 2. Formalizing and pseudo code

Now, for determining the divisors of a number, we need to perform a series of operations...

One approach (slow) is to iterate on all the numbers that are previous to said number. This is because we're looking for a divisor $d$ such that $n \div d \geq 1$.

When we're iterating in the range of numbers from (1, $n$) we can determine how many divisors a number has.

```
count <- 0 // the number of divisors, starting at zero

for i <- 1 until i is equal to n do
	if n mod i is equal to 0 then
		count <- count + 1

if count is equal to 2 then
	return yes
otherwise return no

```