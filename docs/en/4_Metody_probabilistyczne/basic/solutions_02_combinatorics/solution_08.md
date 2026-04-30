# Task 8 — Sequences with Repetition

## 1. How many 5-digit PIN codes are possible if digits may repeat?

Each of the 5 positions can be any digit from 0 to 9, so there are 10 choices for each position.

\[
10^5 = 100000
\]

**Answer:** **100000**

---

## 2. How many such codes contain at least one repeated digit?

First count all possible 5-digit PIN codes:

\[
10^5 = 100000
\]

Now count the codes with **all digits different**:

- 10 choices for the first digit
- 9 choices for the second
- 8 choices for the third
- 7 choices for the fourth
- 6 choices for the fifth

\[
10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30240
\]

So the number of codes with **at least one repeated digit** is:

\[
100000 - 30240 = 69760
\]

**Answer:** **69760**

---

## 3. How many such codes have all digits different?

As calculated above:

\[
10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30240
\]

**Answer:** **30240**