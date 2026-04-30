# Task 5 — Combinations

## 1. A committee of 4 people is chosen from 12 students. How many committees are possible?

Since order does not matter, we use combinations:

\[
\binom{12}{4}=\frac{12!}{4!8!}=495
\]

**Answer:** **495**

---

## 2. How many committees contain a particular student?

Fix that particular student in the committee.

Now we only need to choose the remaining 3 members from the other 11 students:

\[
\binom{11}{3}=\frac{11!}{3!8!}=165
\]

**Answer:** **165**

---

## 3. How many committees contain at least one of two particular students?

We count committees that contain **at least one** of the two particular students.

First, count all possible committees:

\[
\binom{12}{4}=495
\]

Now subtract committees that contain **neither** of the two students.  
If neither is included, we choose all 4 members from the remaining 10 students:

\[
\binom{10}{4}=210
\]

So:

\[
\binom{12}{4}-\binom{10}{4}=495-210=285
\]

**Answer:** **285**

---

## 4. How many committees contain exactly two women if the group consists of 7 men and 5 women?

We must choose:

- 2 women from 5
- 2 men from 7

So the number of such committees is:

\[
\binom{5}{2}\binom{7}{2}
\]

Calculate:

\[
\binom{5}{2}=10,\qquad \binom{7}{2}=21
\]

\[
10 \cdot 21 = 210
\]

**Answer:** **210**