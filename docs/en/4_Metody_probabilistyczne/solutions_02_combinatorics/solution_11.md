# Task 11 — Modeling Outcomes

<<<<<<< HEAD
In combinatorics, the number of outcomes depends on **how we record the result** of an experiment.  
The same physical situation can produce different counting models depending on whether:

- objects are **distinguishable** or **indistinguishable**,
- order is **recorded** or **ignored**,
- positions are treated as **distinct**.

---

## 1. Distinguishable vs Indistinguishable Objects

A box contains:

- 4 red balls
- 4 blue balls
- 3 green balls

So there are \(11\) balls in total.

### (1) How many linear arrangements of all 11 balls are possible if balls of the same color are treated as indistinguishable?

Here, balls of the same color are identical, so this is a **permutation with repeated elements**.

We arrange 11 objects where:

- 4 are red,
- 4 are blue,
- 3 are green.

So the number of distinct arrangements is:

\[
\frac{11!}{4!4!3!}
\]

Now calculate:

\[
11! = 39916800,\qquad 4!=24,\qquad 3!=6
\]

\[
\frac{39916800}{24\cdot24\cdot6}=\frac{39916800}{3456}=11550
\]

**Answer:** **11550**

---

### (2) How many arrangements are possible if every ball is individually labeled?

Now each ball is different:

\[
R_1,R_2,R_3,R_4,\; B_1,B_2,B_3,B_4,\; G_1,G_2,G_3
\]

Since all 11 balls are distinct, the number of linear arrangements is:

\[
11! = 39916800
\]

**Answer:** **39916800**

---

### (3) Explain why the answers in parts (1) and (2) are different.

The answers are different because in part (1), balls of the same color are treated as **identical**, while in part (2), every ball is treated as **different**.

In part (1), swapping two red balls does **not** create a new arrangement, because they are indistinguishable.  
In part (2), swapping \(R_1\) and \(R_2\) **does** create a different arrangement, because the labels matter.

So part (2) has many more outcomes because it distinguishes arrangements that part (1) considers the same.

---

## 2. Recording Order vs Ignoring Order

Three balls are drawn without replacement from the same box.

### (1) How many outcomes are possible if only the set of colors is recorded (order ignored)?

Here we do **not** care which specific balls were drawn, only how many of each color appear.  
So we count color combinations of size 3 using:

- red (R),
- blue (B),
- green (G),

with the restrictions:

- at most 4 red,
- at most 4 blue,
- at most 3 green.

Since we only draw 3 balls, these supply limits do not exclude any ordinary 3-color multisets.

So we count the nonnegative integer solutions of:

\[
r+b+g=3
\]

The number of such solutions is:

\[
\binom{3+3-1}{3}=\binom{5}{3}=10
\]

These 10 outcomes are:

- RRR
- RRB
- RRG
- RBB
- RBG
- RGG
- BBB
- BBG
- BGG
- GGG

**Answer:** **10**

---

### (2) How many outcomes are possible if the sequence of colors is recorded?

Now order matters, so for each of the 3 draws we record the color in sequence.

Each draw can produce one of 3 colors:

- R
- B
- G

Since each color appears at least 3 times in the box, every 3-letter color sequence is possible.

So the number of color sequences is:

\[
3^3=27
\]

**Answer:** **27**

---

### (3) Explain why recording the order changes the counting model.

When order is ignored, outcomes that contain the same colors are treated as the same result.

For example:

- RBG
- RGB
- BRG

all represent the same outcome if we only care about the set or multiset of colors drawn.

But if order is recorded, these become different outcomes because the colors appear in different positions.

So:

- **ignoring order** leads to a **combination / multiset-type model**,
- **recording order** leads to a **sequence model**.

That is why the number of outcomes becomes larger when order is recorded.

---

## 3. PIN Code vs Number

A security system uses 4-digit PIN codes consisting of digits from 0 to 9.

### (1) How many different PIN codes are possible if repetition is allowed?

A PIN code has 4 positions, and each position can be any digit from 0 to 9.

So:

\[
10\cdot10\cdot10\cdot10=10^4=10000
\]

**Answer:** **10000**

---

### (2) Consider 4-digit numbers, where the first digit cannot be zero. How many such numbers exist?

For a 4-digit number:

- the first digit has 9 choices \((1\text{ to }9)\),
- each of the remaining 3 digits has 10 choices.

So:

\[
9\cdot10\cdot10\cdot10=9000
\]

**Answer:** **9000**

---

### (3) Explain why a PIN code and a 4-digit number are counted using different rules.

A PIN code is a **code**, not a numerical value.  
That means leading zeros are allowed.

For example:

- 0427 is a valid PIN code.

But 0427 is **not** a 4-digit number in the usual sense, because numbers cannot begin with 0.  
As a number, 0427 is just 427, which has only 3 digits.

So:

- PIN codes are counted as **4-position sequences**,
- 4-digit numbers are counted as **numbers with a nonzero first digit**.

That is why PIN codes have \(10000\) possibilities, while 4-digit numbers have only \(9000\).

---

### (4) Explain why the codes 1234 and 4321 must be treated as different outcomes.

A PIN code is determined by the digit in each **position**.

So:

- 1234 means:
  - first digit = 1
  - second digit = 2
  - third digit = 3
  - fourth digit = 4

while

- 4321 means:
  - first digit = 4
  - second digit = 3
  - third digit = 2
  - fourth digit = 1

Even though they use the same digits, the order is different, so they are different codes.

This is why PIN codes are counted as **ordered sequences**, not as unordered sets of digits.
=======
>>>>>>> 21a6b7cad34a38c08e661205954d50d437ad7cc9