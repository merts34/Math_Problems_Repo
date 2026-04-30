# Task 6 — Hypergeometric Distribution

---

## 0. Experiment description (sampling without replacement)

---

We consider a finite population of size:

$$
N
$$

Inside this population:

* (K) objects are “success type” (distinguished)
* (N-K) objects are “failure type”

We draw:

$$
n
$$

objects **without replacement**.

---

## Sample space (\Omega)

An elementary outcome is a subset:

$$
\omega \subseteq {1,2,\dots,N}, \quad |\omega|=n
$$

So:

$$
\Omega = {\text{all subsets of size } n}
$$

---

## Random variable

We define:

$$
X(\omega) = \text{number of success-type objects in the sample}
$$

---

## WHY this is different from binomial

Key difference:

* binomial → independent trials
* hypergeometric → dependent draws (no replacement)

So probabilities change after each draw.

---

# 1. PMF of Hypergeometric distribution

---

## Goal

Compute:

$$
P(X=k)
$$

meaning:

> exactly k successes in the sample of size n

---

## Step 1 — choose success objects

We choose:

$$
\binom{K}{k}
$$

ways to pick k successes from K available.

---

## Step 2 — choose failure objects

We choose:

$$
\binom{N-K}{n-k}
$$

ways to pick remaining failures.

---

## Step 3 — total ways to choose sample

All subsets of size n:

$$
\binom{N}{n}
$$

---

## Final PMF formula

$$
P(X=k)=\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

---

## WHY this formula works

Because:

* numerator = favorable combinations
* denominator = all possible samples

So it is:

> classical combinatorial probability

---

# 2. Support of X

---

## Possible values:

$$
X \in \left{\max(0, n-(N-K)), \dots, \min(n,K)\right}
$$

---

## WHY restricted?

Because:

* you cannot pick more successes than exist (K)
* you cannot pick more successes than sample size (n)

---

# 3. Shape behavior (PMF)

---

## Key property

Hypergeometric is:

> similar to binomial but without independence

---

## When population is large:

If (N) is large:

$$
Hypergeometric \approx Binomial
$$

---

## WHY?

Because removing one object barely changes probabilities.

---

## Shape intuition

* symmetric-ish when K ≈ N/2
* skewed when K small or large
* narrower than binomial (less variance)

---

# 4. CDF of hypergeometric

---

## Definition

$$
F(k)=P(X \le k)
$$

---

## Formula

$$
F(k)=\sum_{i=0}^{k}
\frac{\binom{K}{i}\binom{N-K}{n-i}}{\binom{N}{n}}
$$

---

## WHY summation?

Because:

> discrete distribution → CDF = accumulation of PMF

---

# 5. Effect of parameters

---

## 1. Increasing sample size (n)

* distribution shifts right
* variance increases
* more spread

---

## 2. Increasing K (more successes in population)

* distribution shifts right
* higher expected successes

---

## 3. Changing N

* larger N → closer to binomial
* smaller N → stronger dependence effects

---

# 6. Probability computations

---

## 1. Exact probability

$$
P(X=k)=\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

---

## 2. Cumulative probability

$$
P(X \le k)=F(k)
$$

---

## 3. Tail probability

$$
P(X \ge k)=1-F(k-1)
$$

---

## 4. Interval probability

$$
P(a \le X \le b)=F(b)-F(a-1)
$$

---

# 7. Hypergeometric vs Binomial

---

## Binomial

* independent trials
* with replacement (conceptually)

$$
P(X=k)=\binom{n}{k}p^k(1-p)^{n-k}
$$

---

## Hypergeometric

* dependent sampling
* without replacement

$$
P(X=k)=\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

---

## Key difference

| Binomial                       | Hypergeometric       |
| ------------------------------ | -------------------- |
| independence                   | dependence           |
| constant probability           | changing probability |
| infinite population assumption | finite population    |

---

# 8. Real-world applications

---

## 1. Quality inspection

* defective items in batch

---

## 2. Card games

* drawing cards without replacement

---

## 3. Election sampling

* selecting voters from population

---

## 4. Biology

* sampling genes from population

---

## Core idea:

Hypergeometric models:

> sampling without replacement from finite populations

---

# FINAL SUMMARY

---

We built:

### 1. Experiment

* sampling without replacement

### 2. Random variable

* count of successes in sample

### 3. PMF

$$
\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

### 4. CDF

* cumulative sum of PMF

