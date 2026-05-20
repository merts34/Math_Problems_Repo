# Task 6 — Hypergeometric Distribution

---

## 0. Experiment description: Sampling without replacement

We consider a finite population of size:

$$
N
$$

Inside this population:

* $K$ objects are “success type” or distinguished objects
* $N-K$ objects are “failure type” objects

We draw:

$$
n
$$

objects **without replacement**.

This means that after an object is selected, it is not returned to the population.

---

## Sample space $\Omega$

An elementary outcome is a subset:

$$
\omega \subseteq \{1,2,\dots,N\}, \quad \lvert \omega \rvert = n
$$

So:

$$
\Omega = \{\text{all subsets of size } n \text{ from } \{1,2,\dots,N\}\}
$$

The number of possible samples is:

$$
|\Omega|=\binom{N}{n}
$$

---

## Elementary outcome $\omega$

One elementary outcome is one particular sample of size $n$.

For example, if:

$$
N=10, \quad n=3
$$

then one possible elementary outcome is:

$$
\omega=\{2,5,9\}
$$

This means that objects numbered $2$, $5$, and $9$ were selected.

---

## Random variable

We define:

$$
X(\omega)=\text{number of distinguished objects in the sample}
$$

So $X$ counts how many success-type objects appear in the selected sample.

---

## WHY this is different from the binomial distribution

The key difference is:

* Binomial distribution: independent trials
* Hypergeometric distribution: dependent draws because sampling is done without replacement

In the hypergeometric model, probabilities change after each draw.

For example, if one success object is selected, then the number of remaining success objects decreases.

---

# 1. PMF of the Hypergeometric Distribution

---

## Goal

We want to compute:

$$
P(X=k)
$$

This means:

> exactly $k$ successes in the sample of size $n$

---

## Step 1 — Choose success objects

There are $K$ success-type objects in the population.

We choose $k$ of them.

The number of ways is:

$$
\binom{K}{k}
$$

---

## Step 2 — Choose failure objects

The sample size is $n$.

If we already selected $k$ success objects, then we still need:

$$
n-k
$$

failure objects.

There are:

$$
N-K
$$

failure objects in the population.

So the number of ways to choose the failures is:

$$
\binom{N-K}{n-k}
$$

---

## Step 3 — Count all possible samples

The total number of ways to choose $n$ objects from a population of size $N$ is:

$$
\binom{N}{n}
$$

---

## Final PMF formula

Therefore:

$$
P(X=k)=
\frac{\binom{K}{k}\binom{N-K}{n-k}}
{\binom{N}{n}}
$$

---

## Explanation of parameters

In the formula:

$$
P(X=k)=
\frac{\binom{K}{k}\binom{N-K}{n-k}}
{\binom{N}{n}}
$$

we have:

* $N$: total population size
* $K$: number of distinguished or success-type objects in the population
* $N-K$: number of failure-type objects in the population
* $n$: sample size
* $k$: number of success-type objects in the sample
* $X$: random variable counting the number of successes

---

## WHY this formula works

The numerator:

$$
\binom{K}{k}\binom{N-K}{n-k}
$$

counts favorable samples.

The denominator:

$$
\binom{N}{n}
$$

counts all possible samples.

So the probability is:

$$
\frac{\text{favorable samples}}{\text{all possible samples}}
$$

This is classical combinatorial probability.

---

# 2. Support of $X$

---

## Possible values

The random variable $X$ can take values:

$$
X \in \{\max(0,n-(N-K)), \dots, \min(n,K)\}
$$

---

## WHY restricted?

The value of $X$ cannot be any number automatically.

It is restricted because:

* we cannot pick more successes than actually exist, so $X \le K$
* we cannot pick more successes than the sample size, so $X \le n$
* if the sample is large, we may be forced to pick at least some successes

Therefore, the smallest possible value is:

$$
\max(0,n-(N-K))
$$

and the largest possible value is:

$$
\min(n,K)
$$

So the support is:

$$
\{\max(0,n-(N-K)), \dots, \min(n,K)\}
$$

---

# 3. Shape behavior of the PMF

---

## Key property

The hypergeometric distribution is similar to the binomial distribution, but it does not assume independence.

The reason is that the sampling is done without replacement.

---

## When the population is large

If $N$ is large compared to $n$, then:

$$
\operatorname{Hypergeometric}(N,K,n)
\approx
\operatorname{Binomial}\left(n,\frac{K}{N}\right)
$$

---

## WHY?

Because when the population is very large, removing one object barely changes the success probability.

So the draws become almost independent.

---

## Shape intuition

* The distribution is roughly symmetric when $K \approx \frac{N}{2}$.
* It is skewed when $K$ is very small or very large.
* It is usually narrower than the binomial distribution because sampling without replacement reduces randomness.

---

# 4. CDF of the Hypergeometric Distribution

---

## Definition

The cumulative distribution function is:

$$
F(k)=P(X \le k)
$$

This means the probability of getting at most $k$ successes.

---

## Formula

$$
F(k)
=
\sum_{i=\max(0,n-(N-K))}^{k}
\frac{\binom{K}{i}\binom{N-K}{n-i}}
{\binom{N}{n}}
$$

---

## WHY summation?

Because the hypergeometric distribution is discrete.

So the CDF is obtained by adding PMF values:

$$
P(X \le k)
=
P(X=0)+P(X=1)+\cdots+P(X=k)
$$

More generally:

$$
F(k)=\sum_{i \le k} P(X=i)
$$

---

# 5. Effect of parameters

---

## 1. Increasing sample size $n$

When $n$ increases:

* the expected number of successes increases
* the distribution usually shifts to the right
* the possible range of values becomes larger
* the spread can increase because more objects are sampled

The expected value is:

$$
E(X)=n\frac{K}{N}
$$

So if $n$ increases, then $E(X)$ also increases.

---

## 2. Increasing the number of distinguished objects $K$

When $K$ increases, there are more success-type objects in the population.

Therefore:

* the distribution shifts to the right
* the probability of getting more successes increases
* the expected number of successes increases

The expected value is:

$$
E(X)=n\frac{K}{N}
$$

So if $K$ increases, then $E(X)$ also increases.

---

## 3. Changing population size $N$

When $N$ is large compared to $n$:

$$
\operatorname{Hypergeometric}(N,K,n)
\approx
\operatorname{Binomial}\left(n,\frac{K}{N}\right)
$$

When $N$ is small, dependence between draws becomes stronger.

This makes the hypergeometric distribution different from the binomial distribution.

---

# 6. Probability computations

---

## 1. Exact probability

The probability of getting exactly $k$ successes is:

$$
P(X=k)=
\frac{\binom{K}{k}\binom{N-K}{n-k}}
{\binom{N}{n}}
$$

---

## 2. Cumulative probability

The probability of getting at most $k$ successes is:

$$
P(X \le k)=F(k)
$$

where:

$$
F(k)
=
\sum_{i=\max(0,n-(N-K))}^{k}
\frac{\binom{K}{i}\binom{N-K}{n-i}}
{\binom{N}{n}}
$$

---

## 3. Tail probability

The probability of getting at least $k$ successes is:

$$
P(X \ge k)=1-F(k-1)
$$

This works because:

$$
P(X \ge k)=1-P(X \le k-1)
$$

---

## 4. Interval probability

The probability of getting between $a$ and $b$ successes is:

$$
P(a \le X \le b)=F(b)-F(a-1)
$$

This works because $F(b)$ includes everything up to $b$, and $F(a-1)$ removes everything below $a$.

---

# 7. Hypergeometric vs Binomial

---

## Binomial distribution

The binomial distribution is used when:

* trials are independent
* the probability of success is constant
* sampling is with replacement or the population is effectively infinite

Its PMF is:

$$
P(X=k)=\binom{n}{k}p^k(1-p)^{n-k}
$$

---

## Hypergeometric distribution

The hypergeometric distribution is used when:

* draws are dependent
* sampling is without replacement
* the population is finite

Its PMF is:

$$
P(X=k)=
\frac{\binom{K}{k}\binom{N-K}{n-k}}
{\binom{N}{n}}
$$

---

## Key difference

| Binomial | Hypergeometric |
|---|---|
| independent trials | dependent draws |
| constant probability | changing probability |
| with replacement conceptually | without replacement |
| infinite or very large population | finite population |
| parameter $p$ | parameters $N,K,n$ |

---

# 8. Real-world applications

---

## 1. Quality inspection

A factory produces a batch of products.

Some products are defective and some are not defective.

If we inspect a few products without replacement, then the number of defective products in the sample follows a hypergeometric distribution.

---

## 2. Card games

Cards are drawn from a deck without replacement.

The number of aces, hearts, or special cards in a hand can be modeled by a hypergeometric distribution.

---

## 3. Election sampling

A fixed population contains voters with different preferences.

If we select voters without replacement, the number of voters supporting a candidate can be modeled with a hypergeometric distribution.

---

## 4. Biology

In biology, we may sample genes, organisms, or individuals from a finite population.

The number of individuals with a certain trait can be modeled using a hypergeometric distribution.

---

# 9. PMF graphs for several parameter choices

---

To draw PMF graphs, we can use Python.

The following code draws PMF graphs for different parameter choices.

```python
import math
import numpy as np
import matplotlib.pyplot as plt

def hypergeom_pmf(k, N, K, n):
    if k < max(0, n - (N - K)) or k > min(n, K):
        return 0
    
    return (
        math.comb(K, k) * math.comb(N - K, n - k)
    ) / math.comb(N, n)

parameter_sets = [
    (50, 10, 5),
    (50, 25, 5),
    (50, 25, 15)
]

for N, K, n in parameter_sets:
    x_min = max(0, n - (N - K))
    x_max = min(n, K)
    x_values = np.arange(x_min, x_max + 1)

    pmf_values = [hypergeom_pmf(k, N, K, n) for k in x_values]

    plt.figure()
    plt.bar(x_values, pmf_values)
    plt.title(f"Hypergeometric PMF: N={N}, K={K}, n={n}")
    plt.xlabel("Number of successes k")
    plt.ylabel("P(X = k)")
    plt.grid(True)
    plt.show()
```

---

## Explanation of the PMF graphs

The parameter sets are:

$$
(N,K,n)=(50,10,5)
$$

$$
(N,K,n)=(50,25,5)
$$

$$
(N,K,n)=(50,25,15)
$$

These graphs show how the PMF changes when $K$ and $n$ change.

When $K$ increases, the distribution shifts to the right because there are more success-type objects in the population.

When $n$ increases, the possible range of $X$ becomes wider because we draw more objects.

---

# 10. CDF graphs for the same parameter choices

---

The CDF is the cumulative sum of the PMF values.

The following code draws the corresponding CDF graphs.

```python
import math
import numpy as np
import matplotlib.pyplot as plt

def hypergeom_pmf(k, N, K, n):
    if k < max(0, n - (N - K)) or k > min(n, K):
        return 0
    
    return (
        math.comb(K, k) * math.comb(N - K, n - k)
    ) / math.comb(N, n)

parameter_sets = [
    (50, 10, 5),
    (50, 25, 5),
    (50, 25, 15)
]

for N, K, n in parameter_sets:
    x_min = max(0, n - (N - K))
    x_max = min(n, K)
    x_values = np.arange(x_min, x_max + 1)

    pmf_values = [hypergeom_pmf(k, N, K, n) for k in x_values]
    cdf_values = np.cumsum(pmf_values)

    plt.figure()
    plt.step(x_values, cdf_values, where="post")
    plt.title(f"Hypergeometric CDF: N={N}, K={K}, n={n}")
    plt.xlabel("Number of successes k")
    plt.ylabel("F(k) = P(X <= k)")
    plt.grid(True)
    plt.show()
```

---

## Explanation of the CDF graphs

The CDF graphs are increasing step functions.

This is because $X$ is a discrete random variable.

Each jump in the CDF corresponds to one PMF value.

In other words:

$$
F(k)=P(X \le k)
$$

increases whenever a new possible value of $X$ is added.

---

# 11. Application with binomial comparison

---

## Practical example: Quality inspection

Suppose a factory has a batch of:

$$
N=100
$$

products.

Among them:

$$
K=20
$$

products are defective.

We randomly inspect:

$$
n=10
$$

products without replacement.

Let:

$$
X=\text{number of defective products in the sample}
$$

Then:

$$
X \sim \operatorname{Hypergeometric}(N=100,K=20,n=10)
$$

The corresponding binomial approximation uses:

$$
p=\frac{K}{N}=\frac{20}{100}=0.2
$$

So:

$$
Y \sim \operatorname{Binomial}(n=10,p=0.2)
$$

---

## Why compare with binomial?

The binomial model assumes independent trials and constant success probability.

The hypergeometric model does not assume independence because the products are sampled without replacement.

However, when $N$ is large and $n$ is small compared to $N$, the binomial distribution can approximate the hypergeometric distribution.

---

## Graph comparing hypergeometric and binomial PMFs

```python
import math
import numpy as np
import matplotlib.pyplot as plt

def hypergeom_pmf(k, N, K, n):
    if k < max(0, n - (N - K)) or k > min(n, K):
        return 0
    
    return (
        math.comb(K, k) * math.comb(N - K, n - k)
    ) / math.comb(N, n)

def binomial_pmf(k, n, p):
    return math.comb(n, k) * (p ** k) * ((1 - p) ** (n - k))

N = 100
K = 20
n = 10
p = K / N

x_values = np.arange(0, n + 1)

hypergeom_values = [hypergeom_pmf(k, N, K, n) for k in x_values]
binomial_values = [binomial_pmf(k, n, p) for k in x_values]

plt.figure()
plt.plot(x_values, hypergeom_values, marker="o", label="Hypergeometric")
plt.plot(x_values, binomial_values, marker="s", label="Binomial approximation")
plt.title("Hypergeometric vs Binomial PMF")
plt.xlabel("Number of successes k")
plt.ylabel("Probability")
plt.legend()
plt.grid(True)
plt.show()
```

---

## Interpretation of the comparison

The hypergeometric distribution is the correct model because the products are sampled without replacement.

The binomial distribution is only an approximation.

The two distributions become close when:

$$
N \text{ is large compared to } n
$$

because removing one object from a large population does not change the probabilities very much.

---

# Final Summary

---

We built the hypergeometric model step by step.

## 1. Experiment

The experiment is sampling without replacement from a finite population.

---

## 2. Sample space

The sample space is:

$$
\Omega = \{\text{all subsets of size } n \text{ from } \{1,2,\dots,N\}\}
$$

---

## 3. Random variable

The random variable is:

$$
X(\omega)=\text{number of distinguished objects in the sample}
$$

---

## 4. PMF

The probability mass function is:

$$
P(X=k)=
\frac{\binom{K}{k}\binom{N-K}{n-k}}
{\binom{N}{n}}
$$

---

## 5. Support

The support is:

$$
X \in \{\max(0,n-(N-K)), \dots, \min(n,K)\}
$$

---

## 6. CDF

The cumulative distribution function is:

$$
F(k)
=
\sum_{i=\max(0,n-(N-K))}^{k}
\frac{\binom{K}{i}\binom{N-K}{n-i}}
{\binom{N}{n}}
$$

---

## 7. Core idea

The hypergeometric distribution models:

> the number of successes when sampling without replacement from a finite population.

It is different from the binomial distribution because the draws are dependent and the probability of success changes after each draw.