
# Task 1 — Discrete Distribution Given by a PMF Table

---

## 0. Construct a probability space and define X

---

### Given PMF:

| x      | -2   | 0    | 1    | 3    | 5    |
| ------ | ---- | ---- | ---- | ---- | ---- |
| P(X=x) | 0.10 | 0.25 | 0.30 | 0.20 | 0.15 |

---

## Step 1 — What are we trying to build?

We want:

* a sample space Ω
* a probability measure P on Ω
* a random variable X: Ω → ℝ
* such that X produces exactly this distribution

---

## Step 2 — Construct Ω

We convert probabilities into **frequencies interpretation**.

We choose 100 elementary outcomes:

| Value | count |
| ----- | ----- |
| -2    | 10    |
| 0     | 25    |
| 1     | 30    |
| 3     | 20    |
| 5     | 15    |

So we define:

$$
\Omega = {\omega_1, \omega_2, ..., \omega_{100}}
$$

---

## Step 3 — Define probability on Ω

Each elementary outcome has equal probability:

$$
P(\omega_i)=\frac{1}{100}
$$

---

## Step 4 — Define random variable X

We define:

* X(ω) = -2 for first 10 outcomes
* X(ω) = 0 for next 25 outcomes
* X(ω) = 1 for next 30 outcomes
* X(ω) = 3 for next 20 outcomes
* X(ω) = 5 for last 15 outcomes

---

## WHY this works

Because:

$$
P(X=x) = \frac{\text{number of ω mapping to x}}{100}
$$

So we exactly reproduce PMF.

---

# 1. Check if valid probability distribution

---

We check:

### Condition:

$$
\sum P(X=x) = 1
$$

Compute:

$$
0.10 + 0.25 + 0.30 + 0.20 + 0.15
$$

Step-by-step:

* 0.10 + 0.25 = 0.35
* 0.35 + 0.30 = 0.65
* 0.65 + 0.20 = 0.85
* 0.85 + 0.15 = 1.00

---

### Conclusion:

✔ Valid PMF
because total probability = 1

---

# 2. PMF graph

---

## What PMF represents

PMF is:

$$
p(x)=P(X=x)
$$

It is a **discrete spike function**.

---

## Interpretation

Each x-value is a “mass point”:

* -2 → 0.10
* 0 → 0.25
* 1 → 0.30
* 3 → 0.20
* 5 → 0.15

---

## Key idea

PMF is NOT continuous → it is:

* set of vertical bars
* probability concentrated at points

---

# 3. Construct CDF

---

## Definition

$$
F(x)=P(X \le x)
$$

---

## Step-by-step build

We accumulate probabilities from left to right.

---

### x ≤ -2

$$
F(x)=0.10
$$

---

### -2 < x ≤ 0

$$
F(x)=0.10 + 0.25 = 0.35
$$

---

### 0 < x ≤ 1

$$
F(x)=0.35 + 0.30 = 0.65
$$

---

### 1 < x ≤ 3

$$
F(x)=0.65 + 0.20 = 0.85
$$

---

### 3 < x ≤ 5

$$
F(x)=0.85 + 0.15 = 1.00
$$

---

## Final CDF structure

| interval   | F(x) |
| ---------- | ---- |
| x < -2     | 0    |
| -2 ≤ x < 0 | 0.10 |
| 0 ≤ x < 1  | 0.35 |
| 1 ≤ x < 3  | 0.65 |
| 3 ≤ x < 5  | 0.85 |
| x ≥ 5      | 1    |

---

## WHY CDF is step function

Because:

* probability only increases at support points
* between points nothing happens

So CDF is:

> piecewise constant, jumping at support values

---

# 4. Graph of CDF

---

## Key properties

* starts at 0
* ends at 1
* only jumps at x ∈ {-2,0,1,3,5}

---

## Jump sizes = PMF values

At each point:

$$
\Delta F(x) = P(X=x)
$$

---

# 5. Relationship between PMF and CDF

---

## Core identity:

$$
P(X=x) = F(x) - \lim_{t \to x^-} F(t)
$$

---

## Interpretation

* PMF = jump height
* CDF = accumulated probability

---

## Intuition

CDF is like:

> water filling a container step by step

PMF is:

> how much water is added at each step

---

# 6. Probability computations

---

## 1. P(X = a)

Directly from PMF:

Example:

$$
P(X=1)=0.30
$$

---

## 2. P(X ≤ a)

Use CDF:

Example:

$$
P(X \le 1)=0.65
$$

---

## 3. P(X < a)

Important distinction:

Example:

$$
P(X < 1)=0.35
$$

because we exclude jump at 1.

---

## 4. P(a < X ≤ b)

Example:

$$
P(0 < X \le 3)
$$

Step:

$$
F(3) - F(0)
$$

$$
=0.85 - 0.35 = 0.50
$$

---

## 5. P(X ≥ a)

Use complement:

$$
P(X \ge 1) = 1 - P(X < 1)
$$

$$
= 1 - 0.35 = 0.65
$$

---

# 7. PMF vs CDF comparison

---

## PMF gives:

* exact point probabilities
* local information

---

## CDF gives:

* cumulative probabilities
* interval reasoning
* global structure

---

## Key insight:

| PMF             | CDF               |
| --------------- | ----------------- |
| local           | global            |
| discrete points | full accumulation |
| direct P(X=x)   | P(X ≤ x)          |

---

# 8. Conceptual interpretation

---

This distribution represents:

> a discrete system where outcomes have unequal likelihoods

Possible interpretation:

* scoring system
* discrete measurement device
* categorical weighted model

---

# FINAL SUMMARY

---

We built:

### 1. Probability space

* Ω with 100 equal-weight outcomes

### 2. Random variable

* mapping Ω → {-2,0,1,3,5}

### 3. PMF

* direct probability assignment

### 4. CDF

* cumulative structure

### 5. Key identity

$$
\text{CDF jumps} = \text{PMF values}
$$

---

