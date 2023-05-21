Every function in Haskell is an expression. That means, it **always has to return something**. 
That's why we can't omit the *else* statement when we use a conditional.

Also, when a function doesn't use any parameters, we consider that function to be a **definition**, with no special behavior from the literal. For example:
```hs
doubleMe = 4 + 5
-- Same thing as using 4 + 5 directly
```