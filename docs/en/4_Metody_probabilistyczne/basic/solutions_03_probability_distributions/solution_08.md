# Task 8 — Geometric Model

---

## 1. Problem Description

We are given:

* Probability of an error in each program compilation:

$$
p = 0.1
$$

Each compilation is independent.

We run compilations **until the first error occurs**.

---

## 2. Random Variable Definition

Let:

$$
X = \text{number of compilations until the first error occurs}
$$

So:

* $X = 1$ means first compilation has an error
* $X = 2$ means first compilation succeeds, second fails
* etc.

---

## 3. Model Type

This is a **Geometric distribution**, because:

* independent trials
* constant success probability
* we stop at first success (error)

---

## 4. Geometric Distribution Formula

$$
P(X = k) = (1-p)^{k-1} \cdot p
$$

Substitute $p = 0.1$:

$$
P(X = k) = (0.9)^{k-1} \cdot 0.1
$$

---

# PART A — First error appears on the 4th compilation

We compute:

$$
P(X=4)
$$

---

## Step 1: Apply formula

$$
P(X=4) = (0.9)^{4-1} \cdot 0.1
$$

Simplify exponent:

$$
= (0.9)^3 \cdot 0.1
$$

---

## Step 2: Compute $(0.9)^3$ step-by-step

First multiplication:

$$
0.9 \cdot 0.9 = 0.81
$$

Now multiply again:

$$
0.81 \cdot 0.9 = 0.729
$$

So:

$$
(0.9)^3 = 0.729
$$

---

## Step 3: Multiply by 0.1

$$
P(X=4) = 0.729 \cdot 0.1
$$

$$
= 0.0729
$$

---

## Final Answer (Part A)

$$
P(X=4) = 0.0729
$$

---

# PART B — First error occurs no later than the 3rd compilation

We compute:

$$
P(X \le 3)
$$

This means:

* error happens at 1st OR 2nd OR 3rd compilation

So:

$$
P(X \le 3) = P(1) + P(2) + P(3)
$$

---

## Step 1: Compute each term using formula

---

### Case 1: $P(X=1)$

$$
P(X=1) = (0.9)^0 \cdot 0.1
$$

Now:

$$
(0.9)^0 = 1
$$

So:

$$
P(X=1) = 0.1
$$

---

### Case 2: $P(X=2)$

$$
P(X=2) = (0.9)^1 \cdot 0.1
$$

$$
= 0.9 \cdot 0.1
$$

$$
= 0.09
$$

---

### Case 3: $P(X=3)$

$$
P(X=3) = (0.9)^2 \cdot 0.1
$$

First compute:

$$
0.9 \cdot 0.9 = 0.81
$$

So:

$$
P(X=3) = 0.81 \cdot 0.1 = 0.081
$$

---

## Step 2: Sum all probabilities

$$
P(X \le 3) = 0.1 + 0.09 + 0.081
$$

Now add step-by-step:

First:

$$
0.1 + 0.09 = 0.19
$$

Then:

$$
0.19 + 0.081 = 0.271
$$

---

## Final Answer (Part B)

$$
P(X \le 3) = 0.271
$$

---

# 4. Final Summary

### First error on 4th compilation:

$$
P(X=4) = 0.0729
$$

---

### First error no later than 3rd compilation:

$$
P(X \le 3) = 0.271
$$

---
