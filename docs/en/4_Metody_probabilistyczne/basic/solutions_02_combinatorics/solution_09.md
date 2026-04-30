# Task 9 — Digit Restrictions

## 1. How many 5-digit numbers exist?

A 5-digit number cannot start with 0.

- 9 choices for the first digit: \(1\) to \(9\)
- 10 choices for each of the remaining 4 digits

So the total number is:

\[
9 \cdot 10 \cdot 10 \cdot 10 \cdot 10 = 9 \cdot 10^4 = 90000
\]

**Answer:** **90000**

---

## 2. How many of them are even?

A 5-digit number is even if its last digit is one of:

\[
0,2,4,6,8
\]

So there are 5 choices for the last digit.

- 9 choices for the first digit
- 10 choices for each of the middle 3 digits
- 5 choices for the last digit

Thus:

\[
9 \cdot 10^3 \cdot 5 = 45000
\]

**Answer:** **45000**

---

## 3. How many contain no repeated digits?

We count 5-digit numbers with all digits different.

- First digit: 9 choices \((1-9)\)
- Second digit: 9 choices \((0-9\), except the first digit)
- Third digit: 8 choices
- Fourth digit: 7 choices
- Fifth digit: 6 choices

So:

\[
9 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 27216
\]

**Answer:** **27216**

---

## 4. How many contain at least one repeated digit?

Use subtraction:

\[
\text{total 5-digit numbers} - \text{numbers with no repeated digits}
\]

\[
90000 - 27216 = 62784
\]

**Answer:** **62784**