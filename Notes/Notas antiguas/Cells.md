---

name: Cells 
---
*tags: [[TON Blockchain]]*
Created at: 2022-12-06 21:16

---
# What is a cell?

A cell is part of the data structure of the [[TON Blockchain]]. It composes a **graph-like** data structure, where each cell can:

- Hold up to 4 references to other *cells*.
- Hold up to 1023 ($2^{10} - 1$) bits of values.

It is the main part of the blockchain, and it has two main **flavors** (essentially, ways of interacting with the cells):

- Slices, for reading data from a cell.
- Builders, for writing data to a cell.

---
## References:

- https://ton.org/docs/learn/overviews/Cells
