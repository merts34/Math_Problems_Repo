# Task 6 — Binomial Model (Defective Parts) — Full Step-by-Step Solution

---

## Method Used

We use the **Binomial Distribution model** because:

* Fixed number of trials: $n = 10$
* Each trial has two outcomes:

  * defective (success)
  * non-defective (failure)
* Constant probability:
  $$
  p = 0.04
  $$
* Trials are independent

So:

$$
X \sim \text{Binomial}(n=10, p=0.04)
$$

---

## Binomial Formula

$$
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
$$

Here:

* $n = 10$
* $p = 0.04$
* $1-p = 0.96$

So:

$$
P(X = k) = \binom{10}{k}(0.04)^k(0.96)^{10-k}
$$

---

# PART A — Probability of exactly 2 defective parts

We compute:

$$
P(X=2)
$$

---

## Step 1 — Write the formula

$$
P(X=2) = \binom{10}{2}(0.04)^2(0.96)^8
$$

---

## Step 2 — Compute combination term (VERY detailed)

### Definition of combination

By definition:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

---

### Now substitute:

* $n = 10$
* $k = 2$

So:

$$
\binom{10}{2} = \frac{10!}{2!(10-2)!}
$$

---

### Simplify inside:

$$
= \frac{10!}{2! \cdot 8!}
$$

---

### Expand factorials explicitly

We write:

$$
10! = 10 \cdot 9 \cdot 8!
$$

So:

$$
\binom{10}{2} = \frac{10 \cdot 9 \cdot 8!}{2! \cdot 8!}
$$

---

### Cancel common term

$$
= \frac{10 \cdot 9 \cdot \cancel{8!}}{2! \cdot \cancel{8!}}
$$

So:

$$
= \frac{10 \cdot 9}{2!}
$$

---

### Compute factorial

$$
2! = 2 \cdot 1 = 2
$$

So:

$$
\binom{10}{2} = \frac{10 \cdot 9}{2}
$$

---

### Final computation

$$
10 \cdot 9 = 90
$$

$$
90 \div 2 = 45
$$

So:

$$
\binom{10}{2} = 45
$$

---

## Step 3 — Compute probability powers

### (1) Compute $(0.04)^2$

$$
0.04 \cdot 0.04 = 0.0016
$$

So:

$$
(0.04)^2 = 0.0016
$$

---

### (2) Compute $(0.96)^8$

We compute step-by-step:

$$
0.96^2 = 0.9216
$$

$$
0.96^4 = 0.9216 \cdot 0.9216 = 0.84934656
$$

$$
0.96^8 = 0.84934656 \cdot 0.84934656 \approx 0.721389
$$

---

## Step 4 — Multiply everything

We now substitute all results:

$$
P(X=2) = 45 \cdot 0.0016 \cdot 0.721389
$$

---

### First multiplication

$$
45 \cdot 0.0016 = 0.072
$$

---

### Second multiplication

$$
0.072 \cdot 0.721389
$$

Break it down:

* $0.072 \cdot 0.7 = 0.0504$
* $0.072 \cdot 0.021389 \approx 0.00154$

Add:

$$
0.0504 + 0.00154 = 0.05194
$$

---

## Final Answer (Part A)

$$
P(X=2) \approx 0.0519
$$

---

# PART B — At least one defective part

We compute:

$$
P(X \ge 1)
$$

---

## Step 1 — Use complement rule

Instead of summing all cases:

$$
P(X \ge 1) = 1 - P(X=0)
$$

---

## Step 2 — Compute $P(X=0)$

$$
P(X=0) = \binom{10}{0}(0.04)^0(0.96)^{10}
$$

---

## Step 3 — Simplify terms

### Combination:

$$
\binom{10}{0} = 1
$$

### Power:

$$
(0.04)^0 = 1
$$

So:

$$
P(X=0) = (0.96)^{10}
$$

---

## Step 4 — Compute $(0.96)^{10}$ step-by-step

We already know:

$$
0.96^8 \approx 0.721389
$$

Now:

$$
0.96^{10} = 0.96^8 \cdot 0.96^2
$$

We know:

$$
0.96^2 = 0.9216
$$

So:

$$
0.96^{10} = 0.721389 \cdot 0.9216
$$

Compute:

* $0.721389 \cdot 0.9 = 0.6492501$
* $0.721389 \cdot 0.0216 \approx 0.01557$

Sum:

$$
0.66482
$$

So:

$$
P(X=0) \approx 0.6648
$$

---

## Step 5 — Final probability

$$
P(X \ge 1) = 1 - 0.6648
$$

$$
= 0.3352
$$

---

## Final Answers

### Exactly 2 defective parts:

$$
P(X=2) \approx 0.0519
$$

### At least 1 defective part:

$$
P(X \ge 1) \approx 0.335
$$

