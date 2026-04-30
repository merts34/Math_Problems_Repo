# Task 7 — Negative Binomial Distribution

---

## 0. Experiment description (core idea)

---

We perform a sequence of **independent Bernoulli trials**:

* each trial:

  * success with probability (p)
  * failure with probability (1-p)

But now the process is different from geometric:

> we stop when the **r-th success occurs**

---

## Sample space (\Omega)

An elementary outcome is an infinite sequence:

$$
\omega = (x_1, x_2, x_3, \dots)
$$

where:

$$
x_i \in {S, F}
$$

---

## Random variable definition

We define:

$$
X(\omega) = \text{trial number at which the r-th success occurs}
$$

---

## WHY this is meaningful

We are no longer waiting for the first success.

We are now modeling:

> waiting time until repeated success events accumulate

---

# 1. PMF of Negative Binomial distribution

---

## Goal

Compute:

$$
P(X = k)
$$

meaning:

> the r-th success occurs exactly at trial k

---

## Step 1 — structure of the event

If the r-th success occurs at trial k:

* among first (k-1) trials:

  * we must have exactly (r-1) successes
* at trial k:

  * we must have success

---

## Step 2 — choose positions of successes

We choose where the first (r-1) successes occur in first (k-1) trials:

$$
\binom{k-1}{r-1}
$$

---

## Step 3 — probability of a fixed configuration

Each valid sequence has:

* (r) successes → (p^r)
* (k-r) failures → ((1-p)^{k-r})

So:

$$
p^r (1-p)^{k-r}
$$

---

## Final PMF formula

$$
P(X=k)=\binom{k-1}{r-1} p^r (1-p)^{k-r}
$$

---

## WHY this formula works

Because:

* we fix the last success at position k
* we distribute remaining successes among earlier trials
* independence allows multiplication

---

# 2. Support of X

---

## Possible values:

$$
X \in {r, r+1, r+2, \dots}
$$

---

## WHY minimum is r?

Because:

* you need at least r trials to get r successes
* best case: all first r trials are successes

---

## WHY infinite?

Because:

* successes may take arbitrarily long to accumulate

---

# 3. Shape behavior (PMF intuition)

---

## Key property

Negative binomial is:

> a shifted geometric accumulation model

---

## Effect of parameters

### 1. Increasing p

* r-th success happens earlier
* distribution shifts left

---

### 2. Increasing r

* more successes needed
* distribution shifts right
* more spread

---

## Shape intuition

* skewed right
* long tail
* becomes smoother as r increases

---

# 4. CDF of negative binomial

---

## Definition

$$
F(k)=P(X \le k)
$$

meaning:

> r-th success occurs within first k trials

---

## Formula

$$
F(k)=\sum_{i=r}^{k} \binom{i-1}{r-1} p^r (1-p)^{i-r}
$$

---

## WHY summation is necessary

Because:

> we accumulate probabilities over all possible stopping points

---

# 5. Effect of parameters on CDF

---

## Increasing p

* faster growth
* reaches 1 earlier

---

## Increasing r

* slower growth
* delayed accumulation

---

# 6. Probability computations

---

## 1. Exact probability

$$
P(X=k)=\binom{k-1}{r-1} p^r (1-p)^{k-r}
$$

---

## 2. Cumulative probability

$$
P(X \le k)=F(k)
$$

---

## 3. Tail probability

$$
P(X > k)
$$

meaning:

> r successes not yet achieved by time k

So:

$$
P(X > k)=1-F(k)
$$

---

## 4. Interval probability

$$
P(a \le X \le b)=F(b)-F(a-1)
$$

---

# 7. Connection to geometric distribution

---

## Key relationship

If:

$$
r = 1
$$

then:

$$
P(X=k)= (1-p)^{k-1} p
$$

---

## So:

$$
Negative\ Binomial(r=1) = Geometric
$$

---

## Interpretation

* geometric → waiting for first success
* negative binomial → waiting for r successes

---

# 8. Real-world applications

---

## 1. Quality control

* number of items until r defective ones appear

---

## 2. Biology

* number of trials until r mutations occur

---

## 3. Sports

* attempts until r successful shots

---

## 4. Marketing

* number of contacts until r conversions

---

## Core idea:

Negative binomial models:

> accumulation of repeated successes over time

---

# FINAL SUMMARY

---

We built:

### 1. Experiment

* repeated Bernoulli trials

### 2. Random variable

* time until r-th success

### 3. PMF

$$
\binom{k-1}{r-1} p^r (1-p)^{k-r}
$$

### 4. CDF

* cumulative sum of PMF

