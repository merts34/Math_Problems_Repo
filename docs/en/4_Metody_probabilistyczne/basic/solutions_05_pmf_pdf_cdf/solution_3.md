# Task 3 — Binomial Distribution (Bin(n,p))

---

## 0. Experiment model (VERY IMPORTANT STEP)

---

## What is the experiment?

We perform:

> (n) repeated independent Bernoulli trials

Each trial has:

* Success (S)
* Failure (F)

with:

$$
P(S)=p, \quad P(F)=1-p
$$

---

## Sample space construction

Each elementary outcome is a sequence of length (n):

$$
\omega = (x_1, x_2, \dots, x_n)
$$

where:

$$
x_i \in {S, F}
$$

So:

$$
\Omega = {S,F}^n
$$

---

## Random variable definition

We define:

$$
X(\omega) = \text{number of successes in the sequence}
$$

---

## WHY this definition?

Because we are not interested in order, only in:

> how many successes occurred

So X compresses a sequence into a count.

---

# 1. PMF of Binomial distribution

---

## Key idea

We compute:

$$
P(X=k)
$$

meaning:

> exactly k successes in n trials

---

## Step 1 — choose positions of successes

We choose which k trials are success:

$$
\binom{n}{k}
$$

---

## Step 2 — probability of one specific sequence

A specific sequence with k successes:

$$
p^k (1-p)^{n-k}
$$

WHY?

* each success contributes p
* each failure contributes (1-p)
* independence → multiply probabilities

---

## Final PMF formula

$$
P(X=k)=\binom{n}{k} p^k (1-p)^{n-k}
$$

---

# 2. Support of X

---

## What values can X take?

Only counts of successes:

$$
X \in {0,1,2,\dots,n}
$$

---

## WHY?

You cannot have:

* negative successes
* more than n successes

---

# 3. Shape behavior of PMF

---

## Case A — fixed n, change p

### If p small:

* distribution shifts left
* more mass near 0

### If p large:

* distribution shifts right
* more mass near n

---

## Intuition:

p controls:

> "how likely success is per trial"

---

## Case B — fixed p, increase n

### Effect:

* distribution spreads out
* becomes more bell-shaped
* variance increases

---

## Key formula:

$$
\mathbb{E}[X]=np
$$

$$
\mathrm{Var}(X)=np(1-p)
$$

---

# 4. CDF of binomial

---

## Definition

$$
F(k)=P(X \le k)
$$

---

## Expression

$$
F(k)=\sum_{i=0}^{k} \binom{n}{i} p^i (1-p)^{n-i}
$$

---

## WHY summation?

Because binomial is discrete:

> CDF = accumulation of PMF

---

## Shape

* stepwise increasing function
* smoother than PMF visually

---

# 5. How parameters affect CDF

---

## Increase p:

* curve shifts right
* reaches 1 later

---

## Increase n:

* curve becomes smoother
* steps become smaller (more support points)

---

# 6. Probability computations

---

## 1. Exact probability

$$
P(X=k)=\binom{n}{k} p^k (1-p)^{n-k}
$$

---

## 2. Cumulative probability

$$
P(X \le k)=F(k)
$$

---

## 3. Right tail

$$
P(X \ge k)=1 - F(k-1)
$$

---

## 4. Interval probability

$$
P(a \le X \le b)=F(b)-F(a-1)
$$

---

## WHY this works

Because:

$$
F(b)=P(X \le b)
$$

and subtracting removes lower part.

---

# 7. PMF vs CDF usage

---

## PMF is better when:

* exact probability needed
* small n
* combinatorial reasoning

---

## CDF is better when:

* intervals needed
* tail probabilities
* large n

---

# 8. Real-world applications

---

## 1. Quality control

* defective / non-defective items

---

## 2. Medical trials

* success of treatment

---

## 3. Marketing

* click / no click behavior

---

## 4. Finance

* win/loss trades

---

## Core idea:

Binomial =

> counting successes in repeated independent binary events

---

# 9. Relationship with Bernoulli

---

## Bernoulli:

$$
Bin(1,p)
$$

---

## Binomial generalization:

$$
Bin(n,p)
$$

So:

> Binomial = sum of independent Bernoulli variables

---

# FINAL SUMMARY

---

We built:

### 1. Experiment model

* sequences of S/F

### 2. Random variable

* counts successes

### 3. PMF

* combinatorics + probability multiplication

### 4. CDF

* cumulative sum of PMF

---

## Core formula:

$$
P(X=k)=\binom{n}{k} p^k (1-p)^{n-k}
$$
