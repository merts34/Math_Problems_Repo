Haklısın — Task 5 eksik kalmış. Şimdi onu da **aynı formatta, çok detaylı, adım adım, LaTeX $$ ile** çözüyorum.

---

# Task 5 — Multinomial Model (Dice Classification)

---

## 1. Description of the Random Experiment

A fair die is rolled:

* 5 times independently

Each roll has 6 equally likely outcomes:

$$
{1,2,3,4,5,6}
$$

We group outcomes into 3 categories:

* Small: ${1,2}$
* Medium: ${3,4}$
* Large: ${5,6}$

---

## 2. Convert to Probabilities

Since the die is fair:

Each number has probability:

$$
\frac{1}{6}
$$

---

### Small numbers (1,2)

There are 2 outcomes:

$$
P(S) = \frac{2}{6} = \frac{1}{3}
$$

---

### Medium numbers (3,4)

$$
P(M) = \frac{2}{6} = \frac{1}{3}
$$

---

### Large numbers (5,6)

$$
P(L) = \frac{2}{6} = \frac{1}{3}
$$

---

## 3. Random Variables

Let:

$$
X_1 = \text{number of small results}
$$
$$
X_2 = \text{number of medium results}
$$
$$
X_3 = \text{number of large results}
$$

Total rolls:

$$
n = 5
$$

So:

$$
X_1 + X_2 + X_3 = 5
$$

---

## 4. Multinomial Distribution Model

This is a multinomial case because:

* more than 2 outcomes per trial
* fixed number of trials
* independent rolls

---

## 5. Multinomial Formula

$$
P(X_1=x_1, X_2=x_2, X_3=x_3)
============================

\frac{n!}{x_1!x_2!x_3!}
\cdot p_1^{x_1} p_2^{x_2} p_3^{x_3}
$$

---

## 6. Substitute Values

We are NOT solving a numeric subcase here, only defining model:

* $n = 5$
* $p_1 = p_2 = p_3 = \frac{1}{3}$

So:

$$
P(X_1, X_2, X_3)
================

\frac{5!}{x_1!x_2!x_3!}
\cdot \left(\frac{1}{3}\right)^{x_1}
\left(\frac{1}{3}\right)^{x_2}
\left(\frac{1}{3}\right)^{x_3}
$$

---

## 7. Simplify Probability Term

Since exponents add:

$$
x_1 + x_2 + x_3 = 5
$$

So:

$$
\left(\frac{1}{3}\right)^{x_1}
\left(\frac{1}{3}\right)^{x_2}
\left(\frac{1}{3}\right)^{x_3}
==============================

\left(\frac{1}{3}\right)^5
$$

---

## 8. Final Distribution Form

$$
P(X_1, X_2, X_3)
================

\frac{5!}{x_1!x_2!x_3!}
\cdot \left(\frac{1}{3}\right)^5
$$

---

## 9. Compute Constant Terms

### Compute $5!$

$$
5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120
$$

So final structure:

$$
P(X_1, X_2, X_3)
================

\frac{120}{x_1!x_2!x_3!}
\cdot \frac{1}{3^5}
$$

---

## 10. Interpretation

Each outcome:

* 5 dice rolls
* grouped into 3 categories
* probability depends on:

  * how many ways to arrange outcomes
  * category probabilities

---

## 11. Key Insight

This is a **symmetric multinomial case**, because:

$$
p_1 = p_2 = p_3 = \frac{1}{3}
$$

So all categories are equally likely.

---

## 12. Final Answer

$$
P(X_1=x_1, X_2=x_2, X_3=x_3)
============================

\frac{5!}{x_1!x_2!x_3!}
\left(\frac{1}{3}\right)^5
$$

---


