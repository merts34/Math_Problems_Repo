# Task 7 — k-Permutations (Ordered Selections Without Repetition)

## 1. In how many ways can the first three places be assigned among 12 runners?

Since 1st, 2nd, and 3rd places are different positions, order matters.  
So we use a **k-permutation**:

\[
P(12,3)=\frac{12!}{(12-3)!}=\frac{12!}{9!}=12\cdot 11\cdot 10=1320
\]

**Answer:** **1320**

---

## 2. How many 4-digit numbers with distinct digits can be formed from the digits 1–9?

We form a 4-digit number using distinct digits from 1 to 9.

- 9 choices for the first digit
- 8 choices for the second digit
- 7 choices for the third digit
- 6 choices for the fourth digit

So:

\[
9\cdot 8\cdot 7\cdot 6 = 3024
\]

Equivalently:

\[
P(9,4)=\frac{9!}{5!}=3024
\]

**Answer:** **3024**

---

## 3. How many of these numbers are divisible by 5?

A number is divisible by 5 only if its last digit is **5**.  
Since the digits are chosen from 1–9 and must be distinct, we fix the last digit as 5.

Now we choose and arrange the first 3 digits from the remaining 8 digits:

\[
P(8,3)=8\cdot 7\cdot 6=336
\]

**Answer:** **336**