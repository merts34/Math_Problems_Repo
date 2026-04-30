# Task 4 — Geometric Distribution

---

## 0. Experiment description (core intuition)

---

We consider an experiment where:

* we repeat independent Bernoulli trials
* each trial has:

  * success probability (p)
  * failure probability (1-p)

We continue until the **first success occurs**.

---

## Sample space (\Omega)

An elementary outcome is a sequence like:

$$
\omega = (F, F, F, S)
$$

meaning:

* failure, failure, failure, success

So:

$$
\Omega = {F,S}^{\infty} \quad \text{(but only sequences ending at first S matter)}
$$

---

## Random variable definition

We define:

$$
X(\omega) = \text{trial number of first success}
$$

Example:

* F F S → (X=3)

---

## WHY this definition matters

We are not counting successes anymore.

We are measuring:

> waiting time until first success

---

# 1. PMF and CDF

---

## PMF derivation

We want:

$$
P(X=k)
$$

meaning:

> first success happens exactly at trial k

---

## Step 1 — structure of event

For X = k:

* first (k-1) trials are failures
* k-th trial is success

So sequence is:

$$
(F, F, \dots, F, S)
$$

---

## Step 2 — probability of sequence

Each failure contributes (1-p)

Each success contributes (p)

So:

$$
P(X=k) = (1-p)^{k-1} \cdot p
$$

---

## Final PMF

$$
P(X=k) = (1-p)^{k-1} p
$$

---

# WHY this formula makes sense

---

We require:

* k-1 failures in a row → multiply (1-p)
* then success → multiply p

Independence gives multiplication.

---

# 2. Support of X

---

## Possible values

$$
X \in {1,2,3,\dots}
$$

---

## WHY infinite?

Because:

* success might take arbitrarily long
* there is no fixed upper bound

---

# 3. PMF shape behavior

---

## Key property

Geometric distribution is always:

* highest at k = 1
* decreases exponentially

---

## WHY?

Because:

$$
(1-p)^{k-1}
$$

shrinks as k increases.

---

## Effect of p

### If p large:

* fast decay
* success happens early

### If p small:

* slow decay
* long waiting times possible

---

# 4. CDF of geometric distribution

---

## Definition

$$
F(k) = P(X \le k)
$$

meaning:

> success happens within first k trials

---

## Step 1 — sum of PMF

$$
F(k)=\sum_{i=1}^{k} (1-p)^{i-1}p
$$

---

## Step 2 — geometric series trick

Factor p:

$$
F(k)=p \sum_{i=0}^{k-1} (1-p)^i
$$

---

## Step 3 — sum formula

We use:

$$
\sum_{i=0}^{k-1} r^i = \frac{1-r^k}{1-r}
$$

with (r=1-p)

---

## Step 4 — simplify

$$
F(k)=p \cdot \frac{1-(1-p)^k}{p}
$$

Cancel p:

$$
F(k)=1-(1-p)^k
$$

---

## Final CDF

$$
F(k)=1-(1-p)^k
$$

---

# WHY this is important

---

CDF shows:

* probability of having succeeded by time k
* increases monotonically
* approaches 1 as k → ∞

---

# 5. How graphs change with p

---

## PMF

### Increasing p:

* steeper drop after k=1
* mass concentrated early

### Decreasing p:

* long tail
* slow decay

---

## CDF

### Increasing p:

* rises faster to 1

### Decreasing p:

* slower growth
* longer “waiting zone”

---

# 6. Probability computations

---

## 1. Exact probability

$$
P(X=k) = (1-p)^{k-1}p
$$

---

## 2. Cumulative probability

$$
P(X \le k) = 1-(1-p)^k
$$

---

## 3. Tail probability

$$
P(X > k)
$$

Meaning:

> no success in first k trials

So:

$$
P(X > k) = (1-p)^k
$$

---

## 4. Interval probability

$$
P(a \le X \le b)
$$

We use:

$$
F(b) - F(a-1)
$$

So:

$$
= \left[1-(1-p)^b\right] - \left[1-(1-p)^{a-1}\right]
$$

Simplifies to:

$$
(1-p)^{a-1} - (1-p)^b
$$

---

# 7. Interpretation of tail probabilities

---

## Key meaning:

$$
P(X > k) = (1-p)^k
$$

This means:

> probability of “still no success after k trials”

---

## Real interpretation:

* waiting time risk
* delay probability
* survival-like behavior

---

# 8. Applications

---

## 1. Waiting time models

* time until first success

---

## 2. Quality control

* first defective item appearance

---

## 3. Network systems

* first packet success

---

## 4. Games

* number of attempts until win

---

## Key idea:

Geometric distribution models:

> “how long until something happens”

---

# 9. Relation to binomial

---

## Binomial:

* fixed number of trials
* count successes

---

## Geometric:

* random number of trials
* stop at first success

---

## Key contrast:

| Binomial        | Geometric        |
| --------------- | ---------------- |
| fixed n         | random n         |
| count successes | waiting time     |
| bounded support | infinite support |

---

# FINAL SUMMARY

---

We built:

### 1. Experiment

* repeated independent trials until success

### 2. Random variable

* time of first success

### 3. PMF

$$
(1-p)^{k-1}p
$$

### 4. CDF

$$
1-(1-p)^k
$$

