![[Pasted image 20221216141411.png]]

## Pseudo code for the solution

For the problem described in the [[Exercise 1.4]] we need to think about the size of the range of numbers that we are considering. 

Then, we also need to think about how to reduce this range which each iteration and the information that the program is giving us.

So, something very simple would look like this:

````
random_num <- random(Between 1 and 100) // select a random number

upper_border <- 100
lower_border <- 1

guess <- floor(upper_border + lower_border / 2) // start at the middle

// Given that the possible hints are:
// l -> the guess is too low
// g -> the guess is too high
// e -> we found the number

while guess is not equal to random_num do
	hint <- input("Hint: ")
	if hint is equal to l then
		lower_border <- guess + 1
	else if hint is equal to g then
		higher_border <- guess - 1
	else if hint is equal to e then
		output <- "You won the game!"

```