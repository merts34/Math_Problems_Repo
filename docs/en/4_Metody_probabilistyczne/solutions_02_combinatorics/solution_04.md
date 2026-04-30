# Task 4 — Circular Permutations

## 1. In how many ways can 7 people sit around a round table?

For seating around a round table, rotations are considered the same, so the number of circular arrangements of \(n\) distinct people is:

\[
(n-1)!
\]

For 7 people:

\[
(7-1)! = 6! = 720
\]

**Answer:** **720**

---

## 2. In how many ways can they sit if two particular people must sit next to each other?

Treat the two particular people as one block.

Then we have:

- 1 block of 2 people
- 5 other people

So there are **6 objects** to arrange around the table.

The number of circular arrangements of 6 objects is:

\[
(6-1)! = 5!
\]

Inside the block, the two people can switch places in:

\[
2!
\]

So the total number of arrangements is:

\[
5! \cdot 2 = 120 \cdot 2 = 240
\]

**Answer:** **240**

---

## 3. In how many ways can they sit if those two people must sit opposite each other?

Fix one of the two particular people in a seat.  
Since the table is round, this removes rotational symmetry.

The other particular person must then sit in the seat directly opposite.

Now the remaining 5 people can be arranged freely in the remaining 5 seats:

\[
5! = 120
\]

**Answer:** **120**