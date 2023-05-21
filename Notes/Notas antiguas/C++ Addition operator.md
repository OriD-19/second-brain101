---
name: C++ Addition operator 
---
*tags: [[Competitive Programming]]*
Created at: 2022-12-17 20:37

---

Interesting enough, the "++" operator in C++ behaves differently depending in the position that you place it (this also applies for the "--" operator):

- If you place it before, it returns the value of the **incremented variable**; that is, if you have a variable "a" whose value is 5, if you use "++a" then you will get back "6" (the already incremented value).
- However, if you place it *after* the variable, then the program will return the **actual value** of the variable. So, the expression "a++" will return the value 5, and **then** increment the value of the "a" variable.

This behavior is important, as the first approach will cause some problems (especially when accessing indexes of an array, for example).

---
## References:
- [[@Principles of Algorithmic Problem Solving ()]], page 32.
