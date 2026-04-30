# Task 10 — Urn Models

The urn contains:

- 5 red balls
- 4 blue balls
- 3 green balls

So the total number of balls is:

\[
5+4+3=12
\]

---

## 1. Three balls are drawn without replacement. How many samples are possible if order is ignored?

Since order is ignored, we use **combinations**:

\[
\binom{12}{3}=\frac{12!}{3!9!}=220
\]

**Answer:** **220**

---

## 2. How many samples contain exactly two red balls?

We choose:

- 2 red balls from 5
- 1 non-red ball from the remaining \(4+3=7\) balls

So:

\[
\binom{5}{2}\binom{7}{1}
\]

Calculate:

\[
\binom{5}{2}=10,\qquad \binom{7}{1}=7
\]

\[
10 \cdot 7 = 70
\]

**Answer:** **70**

---

## 3. Three balls are drawn and the order of colors is recorded. How many outcomes are possible?

Since the **order of colors** is recorded, we count all ordered draws of 3 balls without replacement.

This is a **k-permutation** of 12 balls taken 3 at a time:

\[
P(12,3)=12\cdot 11\cdot 10=1320
\]

**Answer:** **1320**

---

## 4. How many outcomes contain exactly two red balls?

We want ordered draws of 3 balls with exactly 2 red balls and 1 non-red ball.

### Step 1: Choose the balls
- Choose 2 red balls from 5:

\[
\binom{5}{2}=10
\]

- Choose 1 non-red ball from 7:

\[
\binom{7}{1}=7
\]

So the number of ways to choose the balls is:

\[
10 \cdot 7 = 70
\]

### Step 2: Arrange the 3 chosen balls
The 3 chosen balls are distinct, so they can be ordered in:

\[
3! = 6
\]

ways.

Thus the total number of ordered outcomes is:

\[
70 \cdot 6 = 420
\]

**Answer:** **420**