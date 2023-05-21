---
name: Database Cursor 
---
*tags: [[Backend Development]] [[Databases]]*
Created at: 2022-12-12 16:22

---

A database cursor is a pointer to a single row of the table.

In a relational database this is the same as considering a single **row** on the table.

We can think of cursors as a *pair of tweezers*, which we can use to select a single entry of the bag of results (a **database transaction**).

Normally, a single query is treated as a collection of data. With a pointer, we can treat each piece of data (i.e., each row) as a **single piece of information**.

This is also useful for performance in an application, since a cursor only holds **one register in memory** at a time, giving us the possibility to *lazy load* the data in our database, and only load those entries that we are currently using.

---
## References:
- [[@What is a Database Cursor_ (2021)]]
