# Task 12 — Mixed Counting Problem

For each part, we identify the most appropriate counting model and compute the number of outcomes.

---

## 1. Student ID Codes

A student identifier consists of:

- 2 letters chosen from \(\{A,B,C,D,E\}\)
- followed by 3 digits chosen from \(\{0,1,2,\dots,9\}\)

### (a) How many identifiers are possible if letters and digits may repeat?

**Model:** sequence with repetition

- 2 letter positions, each with 5 choices
- 3 digit positions, each with 10 choices

\[
5^2 \cdot 10^3 = 25 \cdot 1000 = 25000
\]

**Answer:** **25000**

---

### (b) How many identifiers are possible if letters may not repeat but digits may repeat?

**Model:**  
- letters: \(k\)-permutation without repetition  
- digits: sequence with repetition

For the letters:

\[
P(5,2)=5\cdot4=20
\]

For the digits:

\[
10^3=1000
\]

So:

\[
20 \cdot 1000 = 20000
\]

**Answer:** **20000**

---

### (c) How many identifiers are possible if neither letters nor digits may repeat?

**Model:** \(k\)-permutation without repetition

For the letters:

\[
P(5,2)=5\cdot4=20
\]

For the digits:

\[
P(10,3)=10\cdot9\cdot8=720
\]

So:

\[
20 \cdot 720 = 14400
\]

**Answer:** **14400**

---

## 2. Medal Assignment

There are 12 runners, and medals are awarded for:

- gold
- silver
- bronze

Since the medals are different, order matters.

### (a) In how many ways can the medals be assigned?

**Model:** \(k\)-permutation (ordered selection without repetition)

\[
P(12,3)=12\cdot11\cdot10=1320
\]

**Answer:** **1320**

---

### (b) Suppose two particular runners must both receive medals. In how many ways can the medals be assigned?

Let the two particular runners be \(A\) and \(B\). They must both receive medals, so the third medal goes to one of the remaining 10 runners.

- Choose the third medalist: \(\binom{10}{1}=10\)
- Arrange the 3 medalists into gold, silver, bronze: \(3!=6\)

So:

\[
10 \cdot 6 = 60
\]

**Answer:** **60**

---

## 3. Committee Selection

A committee of 4 people is chosen from 10 students, including:

- 6 men
- 4 women

Since order does not matter, we use combinations.

### (a) How many committees are possible?

**Model:** combination

\[
\binom{10}{4}=210
\]

**Answer:** **210**

---

### (b) How many committees contain exactly two women?

**Model:** combination

Choose:

- 2 women from 4
- 2 men from 6

\[
\binom{4}{2}\binom{6}{2}=6\cdot15=90
\]

**Answer:** **90**

---

### (c) How many committees contain at least one woman?

**Model:** combination with complement

First count all committees:

\[
\binom{10}{4}=210
\]

Now subtract committees with no women, meaning all 4 members are men:

\[
\binom{6}{4}=15
\]

So:

\[
210-15=195
\]

**Answer:** **195**

---

## 4. Circular Seating

Seven people sit around a round table.

### (a) How many different seating arrangements are possible?

**Model:** circular permutation

For \(n\) distinct people around a circle:

\[
(n-1)!
\]

So:

\[
(7-1)!=6!=720
\]

**Answer:** **720**

---

### (b) In how many arrangements do two particular people sit next to each other?

Treat the two particular people as one block.

Then we have:

- 1 block
- 5 other people

So there are 6 objects around the circle.

Number of circular arrangements of 6 objects:

\[
(6-1)!=5!=120
\]

The two people inside the block can switch places in:

\[
2!=2
\]

So:

\[
120\cdot2=240
\]

**Answer:** **240**

---

## 5. Passwords

A password consists of 5 characters chosen from:

- the digits \(0\)–\(9\) → 10 choices
- the letters \(A\)–\(Z\) → 26 choices

So there are:

\[
10+26=36
\]

possible characters for each position.

### (a) How many passwords are possible if repetition is allowed?

**Model:** sequence with repetition

Each of the 5 positions has 36 choices:

\[
36^5
\]

Calculate:

\[
36^5=60466176
\]

**Answer:** **60466176**

---

### (b) How many passwords are possible if no character may repeat?

**Model:** \(k\)-permutation without repetition

We choose and arrange 5 distinct characters from 36:

\[
P(36,5)=36\cdot35\cdot34\cdot33\cdot32
\]

Calculate step by step:

\[
36\cdot35=1260
\]

\[
1260\cdot34=42840
\]

\[
42840\cdot33=1413720
\]

\[
1413720\cdot32=45239040
\]

**Answer:** **45239040**

---

### (c) Which counting model is used in each case?

- **If repetition is allowed:** sequence with repetition
- **If no character may repeat:** \(k\)-permutation (ordered selection without repetition)

This is because a password is an **ordered string** of characters, so changing the order gives a different password.