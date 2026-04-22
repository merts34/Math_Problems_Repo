# Task 10 — Multinomial Model

---

## 1. Problem Description

We are given a box of candies with 3 flavors:

* Strawberry: $0.40$
* Lemon: $0.35$
* Mint: $0.25$

We randomly select 6 candies **independently**.

Let:

$$
X_1 = \text{number of strawberry candies}
$$
$$
X_2 = \text{number of lemon candies}
$$
$$
X_3 = \text{number of mint candies}
$$

We want:

$$
(X_1, X_2, X_3) = (3, 2, 1)
$$

---

## 2. Model Type

This is a **Multinomial distribution** because:

* each trial has more than 2 outcomes
* probabilities are constant
* trials are independent
* total number of trials is fixed ($n=6$)

---

## 3. Multinomial Formula

$$
P(X_1=x_1, X_2=x_2, X_3=x_3)
============================

\frac{n!}{x_1!x_2!x_3!}
\cdot
p_1^{x_1} p_2^{x_2} p_3^{x_3}
$$

---

## 4. Substitute Given Values

We have:

* $n = 6$
* $x_1 = 3$, $x_2 = 2$, $x_3 = 1$
* $p_1 = 0.40$, $p_2 = 0.35$, $p_3 = 0.25$

So:

$$
P = \frac{6!}{3!2!1!}
\cdot (0.40)^3 \cdot (0.35)^2 \cdot (0.25)^1
$$

---

# 5. Step 1 — Compute factorial part

## Compute $6!$

$$
6! = 6 \cdot 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 720
$$

---

## Compute denominator

$$
3! = 3 \cdot 2 \cdot 1 = 6
$$

$$
2! = 2 \cdot 1 = 2
$$

$$
1! = 1
$$

Multiply:

$$
3! \cdot 2! \cdot 1! = 6 \cdot 2 \cdot 1 = 12
$$

---

## Fraction result

$$
\frac{6!}{3!2!1!} = \frac{720}{12} = 60
$$

---

# 6. Step 2 — Compute probability powers

---

## (1) Compute $(0.40)^3$

Step-by-step:

$$
0.40 \cdot 0.40 = 0.16
$$

$$
0.16 \cdot 0.40 = 0.064
$$

So:

$$
(0.40)^3 = 0.064
$$

---

## (2) Compute $(0.35)^2$

$$
0.35 \cdot 0.35 = 0.1225
$$

---

## (3) Compute $(0.25)^1$

$$
(0.25)^1 = 0.25
$$

---

# 7. Step 3 — Multiply probability terms

First multiply:

$$
0.064 \cdot 0.1225
$$

Step-by-step:

* $0.064 \cdot 0.1 = 0.0064$
* $0.064 \cdot 0.0225 = 0.00144$

Sum:

$$
0.0064 + 0.00144 = 0.00784
$$

Now multiply:

$$
0.00784 \cdot 0.25
$$

$$
= 0.00196
$$

---

# 8. Step 4 — Multiply with multinomial coefficient

Now:

$$
P = 60 \cdot 0.00196
$$

Step-by-step:

$$
60 \cdot 0.001 = 0.06
$$

$$
60 \cdot 0.00096 = 0.0576
$$

Add:

$$
0.06 + 0.0576 = 0.1176
$$

---

# 9. Final Answer

$$
P(X_1=3, X_2=2, X_3=1) \approx 0.1176
$$

---

# 10. Interpretation

This means:

If we randomly pick 6 candies many times, about:

$$
11.76%
$$

of the time we will get:

* 3 strawberry
* 2 lemon
* 1 mint

---

