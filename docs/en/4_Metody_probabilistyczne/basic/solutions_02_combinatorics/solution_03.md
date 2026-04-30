# Task 3 — Permutations with Repeated Elements

## 1. How many distinct arrangements of the word MISSISSIPPI are possible?

The word **MISSISSIPPI** has 11 letters in total:

- M = 1
- I = 4
- S = 4
- P = 2

The number of distinct arrangements of a word with repeated letters is:

\[
\frac{11!}{4!4!2!}
\]

Now calculate:

\[
11! = 39916800
\]

\[
4! = 24,\quad 2! = 2
\]

\[
\frac{39916800}{24 \cdot 24 \cdot 2} = \frac{39916800}{1152} = 34650
\]

**Answer:** **34650**

---

## 2. How many distinct arrangements of STATISTICS are possible?

The word **STATISTICS** has 10 letters in total:

- S = 3
- T = 3
- A = 1
- I = 2
- C = 1

So the number of distinct arrangements is:

\[
\frac{10!}{3!3!2!}
\]

Now calculate:

\[
10! = 3628800
\]

\[
3! = 6,\quad 2! = 2
\]

\[
\frac{3628800}{6 \cdot 6 \cdot 2} = \frac{3628800}{72} = 50400
\]

**Answer:** **50400**

---

## 3. How many of the arrangements of STATISTICS start with the letter S?

Fix one **S** at the beginning.

Now we arrange the remaining 9 letters:

- S = 2
- T = 3
- A = 1
- I = 2
- C = 1

The number of distinct arrangements is:

\[
\frac{9!}{2!3!2!}
\]

Now calculate:

\[
9! = 362880
\]

\[
2! = 2,\quad 3! = 6
\]

\[
\frac{362880}{2 \cdot 6 \cdot 2} = \frac{362880}{24} = 15120
\]

**Answer:** **15120**