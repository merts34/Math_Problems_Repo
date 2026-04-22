# Task 3 — Geometric Model (Waiting for the First Event)

---

## 1. Description of the Random Experiment

We observe a sequence of printed pages in a printing house.

Each page can:

* contain an error (success event)
* contain no error (failure event)

Let:

$$
P(\text{error}) = p
$$

$$
P(\text{no error}) = 1 - p
$$

We keep observing pages **until the first error appears**.

---

## 2. Key Idea of the Experiment

We are not fixing the number of trials.

Instead:

* we stop at the first success (error)

So the random variable is:

$$
X = \text{number of pages until first error occurs}
$$

---

## 3. Sample Space $\Omega$

Possible outcomes are sequences ending with the first error:

* First page is error → 1
* First error on second page → 2
* First error on third page → 3
* etc.

So:

$$
\Omega = {1,2,3,4,\dots}
$$

---

## 4. Probability Structure (Step-by-step logic)

We compute probabilities by enforcing:

* first $(k-1)$ pages are NOT errors
* the $k$-th page IS an error

---

## 5. General Probability Formula

We derive step-by-step.

---

### Step 1: First page is not error

$$
P(\text{no error}) = 1 - p
$$

---

### Step 2: First two pages are not error

$$
P(\text{no error, no error}) = (1 - p)(1 - p)
$$

Now expand:

$$
(1 - p)(1 - p) = 1 - p - p + p^2
$$

$$
= 1 - 2p + p^2
$$

---

### Step 3: First $k-1$ pages are not error

We multiply $(1-p)$ repeatedly:

$$
(1 - p)^{k-1}
$$

This represents:

$$
(1 - p)(1 - p)(1 - p)\cdots \text{(k-1 times)}
$$

---

### Step 4: The k-th page is an error

$$
P(\text{k-th page is error}) = p
$$

---

## 6. Final Probability Formula

Now combine:

* first $(k-1)$ failures
* then 1 success

$$
P(X = k) = (1 - p)^{k-1} \cdot p
$$

---

## 7. Full Expansion Example (k = 4)

Let’s explicitly expand:

$$
P(X = 4) = (1 - p)^3 \cdot p
$$

Now expand $(1 - p)^3$ step by step:

First:

$$
(1 - p)(1 - p) = 1 - 2p + p^2
$$

Now multiply again:

$$
(1 - 2p + p^2)(1 - p)
$$

Expand:

$$
= 1 - p - 2p + 2p^2 + p^2 - p^3
$$

$$
= 1 - 3p + 3p^2 - p^3
$$

Now multiply by $p$:

$$
(1 - 3p + 3p^2 - p^3)p
$$

$$
= p - 3p^2 + 3p^3 - p^4
$$

So:

$$
P(X=4) = p - 3p^2 + 3p^3 - p^4
$$

---

## 8. Special Case: First Page is Error

If $k = 1$:

$$
P(X = 1) = p
$$

(no failures before)

---

## 9. Success Definition

A success is defined as:

$$
\text{Success} = \text{error on a page}
$$

---

## 10. Key Property

This model assumes:

* independent trials
* constant probability $p$
* infinite sequence of trials

---

## 11. Final Summary

The geometric distribution is:

$$
P(X = k) = (1 - p)^{k-1} p
$$

where:

* $(1 - p)^{k-1}$ = all failures before first success
* $p$ = success at step $k$

---
