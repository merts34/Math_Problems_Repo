# Task 9 — Poisson Model

---

## 1. Problem Description

We are given:

* A customer service center receives on average:

$$
\lambda = 5
$$

requests per hour.

We define:

$$
X = \text{number of requests in 1 hour}
$$

We assume a **Poisson process**.

---

## 2. Why Poisson Model?

We use Poisson because:

* events occur randomly in time
* events are independent
* we count number of events in a fixed interval
* we know only the average rate $\lambda$

---

## 3. Random Variable

$$
X \in {0,1,2,3,\dots}
$$

---

## 4. Poisson Distribution Formula

$$
P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!}
$$

Substitute $\lambda = 5$:

$$
P(X = k) = \frac{e^{-5} \cdot 5^k}{k!}
$$

---

# PART A — Exactly 3 requests

We compute:

$$
P(X=3)
$$

---

## Step 1: Apply formula

$$
P(X=3) = \frac{e^{-5} \cdot 5^3}{3!}
$$

---

## Step 2: Compute each part separately

### (1) Compute $5^3$

$$
5^3 = 5 \cdot 5 \cdot 5 = 125
$$

---

### (2) Compute factorial $3!$

$$
3! = 3 \cdot 2 \cdot 1 = 6
$$

---

### (3) Substitute

$$
P(X=3) = \frac{e^{-5} \cdot 125}{6}
$$

---

## Step 3: Simplify fraction

$$
\frac{125}{6} \approx 20.8333
$$

So:

$$
P(X=3) = 20.8333 \cdot e^{-5}
$$

---

## Step 4: Approximate $e^{-5}$

We use:

$$
e^{-5} \approx 0.006737
$$

---

## Step 5: Multiply

$$
20.8333 \cdot 0.006737
$$

Now multiply step-by-step:

* $20 \cdot 0.006737 = 0.13474$
* $0.8333 \cdot 0.006737 \approx 0.00561$

Add:

$$
0.13474 + 0.00561 = 0.14035
$$

---

## Final Answer (Part A)

$$
P(X=3) \approx 0.140
$$

---

# PART B — At least one request

We compute:

$$
P(X \ge 1)
$$

---

## Step 1: Use complement rule

Instead of summing infinite terms:

$$
P(X \ge 1) = 1 - P(X=0)
$$

---

## Step 2: Compute $P(X=0)$

Formula:

$$
P(X=0) = \frac{e^{-5} \cdot 5^0}{0!}
$$

---

## Step 3: Simplify terms

### Powers:

$$
5^0 = 1
$$

### Factorial:

$$
0! = 1
$$

So:

$$
P(X=0) = e^{-5}
$$

---

## Step 4: Substitute approximation

$$
P(X=0) \approx 0.006737
$$

---

## Step 5: Compute complement

$$
P(X \ge 1) = 1 - 0.006737
$$

$$
= 0.993263
$$

---

## Final Answer (Part B)

$$
P(X \ge 1) \approx 0.993
$$

---

# 5. Final Summary

### Exactly 3 requests:

$$
P(X=3) \approx 0.140
$$

### At least 1 request:

$$
P(X \ge 1) \approx 0.993
$$

---
