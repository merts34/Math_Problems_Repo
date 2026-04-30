

# Task 2 — Discrete Distribution Given by a CDF Table

---

## 0. Given information

We are given a cumulative distribution function:

| x    | -1   | 0    | 2    | 4    | 6    |
| ---- | ---- | ---- | ---- | ---- | ---- |
| F(x) | 0.15 | 0.35 | 0.60 | 0.85 | 1.00 |

---

# 1. What are we trying to understand?

We are NOT directly given probabilities.

We are given:

$$
F(x)=P(X \le x)
$$

So the key idea is:

> CDF tells cumulative mass, not individual probabilities.

We must extract PMF from jumps.

---

# 2. Construct probability space (conceptual)

---

## Step 1 — Interpretation

We assume a finite experiment where outcomes are grouped into:

* values of X: {-1, 0, 2, 4, 6}
* each value corresponds to a probability mass

---

## Step 2 — Key idea

Each jump in CDF = probability at that point:

$$
P(X=x) = F(x) - F(x^-)
$$

where:

* (F(x^-)) = value just before x

---

# 3. Reconstruct PMF

---

## x = -1

Before -1:

$$
F(-1^-)=0
$$

So:

$$
P(X=-1)=0.15 - 0 = 0.15
$$

---

## x = 0

$$
P(X=0)=0.35 - 0.15 = 0.20
$$

---

## x = 2

$$
P(X=2)=0.60 - 0.35 = 0.25
$$

---

## x = 4

$$
P(X=4)=0.85 - 0.60 = 0.25
$$

---

## x = 6

$$
P(X=6)=1.00 - 0.85 = 0.15
$$

---

## Final PMF table

| x      | -1   | 0    | 2    | 4    | 6    |
| ------ | ---- | ---- | ---- | ---- | ---- |
| P(X=x) | 0.15 | 0.20 | 0.25 | 0.25 | 0.15 |

---

# 4. WHY this works

---

## Core principle

CDF is defined as:

$$
F(x)=\sum_{t \le x} P(X=t)
$$

So:

> CDF is cumulative sum of PMF

Therefore:

$$
\text{PMF = differences of CDF}
$$

---

# 5. Draw PMF (interpretation)

---

We now interpret:

* -1 → 0.15
* 0 → 0.20
* 2 → 0.25
* 4 → 0.25
* 6 → 0.15

---

## Shape insight

This distribution is:

* symmetric-ish
* center-heavy at 2 and 4
* lighter tails at -1 and 6

---

# 6. Redraw CDF (step structure)

---

## Key rule

CDF is:

* constant between points
* jumps at support points

---

## Stepwise form:

### x < -1

$$
F(x)=0
$$

---

### -1 ≤ x < 0

$$
F(x)=0.15
$$

---

### 0 ≤ x < 2

$$
F(x)=0.35
$$

---

### 2 ≤ x < 4

$$
F(x)=0.60
$$

---

### 4 ≤ x < 6

$$
F(x)=0.85
$$

---

### x ≥ 6

$$
F(x)=1
$$

---

# 7. Jump interpretation

---

## Key identity

At any point:

$$
\text{jump size} = P(X=x)
$$

---

## Why?

Because:

$$
F(x)=P(X \le x)
$$

So the increase at x is exactly the probability mass at x.

---

# 8. Probability computations using CDF

---

## 1. P(X ≤ a)

Direct:

Example:

$$
P(X \le 2)=0.60
$$

---

## 2. P(X < a)

We exclude the jump:

Example:

$$
P(X < 2)=F(0)=0.35
$$

---

## 3. P(X = a)

Difference form:

Example:

$$
P(X=4)=F(4)-F(4^-)
$$

$$
=0.85 - 0.60 = 0.25
$$

---

## 4. P(a < X ≤ b)

Example:

$$
P(0 < X \le 4)
$$

Use:

$$
F(4) - F(0)
$$

$$
=0.85 - 0.35 = 0.50
$$

---

## 5. P(X > a)

Use complement:

Example:

$$
P(X > 2)=1 - F(2)
$$

$$
=1 - 0.60 = 0.40
$$

---

# 9. Comparison with Task 1

---

## PMF gives:

* direct probabilities
* local structure

---

## CDF gives:

* cumulative structure
* interval probabilities easily

---

## Key insight:

| PMF                           | CDF                       |
| ----------------------------- | ------------------------- |
| local values                  | accumulated values        |
| direct P(X=x)                 | easy intervals            |
| needs summation for intervals | intervals are subtraction |

---

# 10. Fundamental takeaway

---

## Big idea:

CDF is not “different information” — it is:

> a transformed version of PMF using cumulative sums

And PMF is:

> the discrete derivative of CDF

---

## Mathematical relationship:

$$
P(X=x)=F(x)-F(x^-)
$$

and

$$
F(x)=\sum_{t \le x} P(X=t)
$$

---

# FINAL SUMMARY

---

We learned:

### 1. From CDF → PMF

* take jumps

### 2. From PMF → CDF

* take cumulative sums

### 3. Interpretation

* PMF = local probability structure
* CDF = global accumulation structure

