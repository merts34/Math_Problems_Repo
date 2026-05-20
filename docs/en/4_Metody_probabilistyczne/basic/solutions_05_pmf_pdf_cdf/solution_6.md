# Task 6 — Hypergeometric Distribution

---

## 0. Experiment description: Sampling without replacement

We consider a finite population of size:

$$
N
$$

Inside this population:

* $K$ objects are success-type or distinguished objects.
* $N-K$ objects are failure-type objects.

We draw:

$$
n
$$

objects without replacement.

This means that after an object is selected, it is not returned to the population.

---

## Sample space

An elementary outcome is a subset of the population:

$$
\omega \subseteq \{1,2,\dots,N\}
$$

The size of this subset is:

$$
|\omega|=n
$$

Therefore, the sample space is:

$$
\Omega=\{\text{all subsets of size } n \text{ from } \{1,2,\dots,N\}\}
$$

The number of possible samples is:

$$
|\Omega|=\binom{N}{n}
$$

Using the combination formula:

$$
\binom{N}{n}
=
\frac{N!}{n!(N-n)!}
$$

---

## Elementary outcome

One elementary outcome is one particular sample of size $n$.

For example, let:

$$
N=10
$$

and:

$$
n=3
$$

One possible elementary outcome is:

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

For example, suppose the distinguished objects are:

$$
\{1,2,3,4\}
$$

and the selected sample is:

$$
\omega=\{2,5,9\}
$$

Only object $2$ is distinguished.

Therefore:

$$
X(\omega)=1
$$

---

## Why this is different from the binomial distribution

The key difference is:

* Binomial distribution: independent trials.
* Hypergeometric distribution: dependent draws because sampling is done without replacement.

In the hypergeometric model, probabilities change after each draw.

For example, suppose:

$$
N=10
$$

and:

$$
K=4
$$

At the beginning, the probability of selecting a success is:

$$
\frac{K}{N}
=
\frac{4}{10}
$$

If one success is selected, then the remaining population size becomes:

$$
10-1=9
$$

The remaining number of successes becomes:

$$
4-1=3
$$

So the new success probability becomes:

$$
\frac{3}{9}
$$

Therefore, the probability changed from:

$$
\frac{4}{10}
$$

to:

$$
\frac{3}{9}
$$

This is why the draws are dependent.

---

# 1. PMF of the Hypergeometric Distribution

---

## Goal

We want to compute:

$$
P(X=k)
$$

This means exactly $k$ successes in the sample of size $n$.

---

## Step 1 — Choose success objects

There are:

$$
K
$$

success-type objects in the population.

We want to choose:

$$
k
$$

success-type objects.

The number of ways to do this is:

$$
\binom{K}{k}
$$

Using the combination formula:

$$
\binom{K}{k}
=
\frac{K!}{k!(K-k)!}
$$

---

## Step 2 — Choose failure objects

The sample size is:

$$
n
$$

If we already selected:

$$
k
$$

success-type objects, then we still need:

$$
n-k
$$

failure-type objects.

There are:

$$
N-K
$$

failure-type objects in the population.

So the number of ways to choose the failure objects is:

$$
\binom{N-K}{n-k}
$$

Using the combination formula:

$$
\binom{N-K}{n-k}
=
\frac{(N-K)!}{(n-k)!((N-K)-(n-k))!}
$$

---

## Step 3 — Count all possible samples

The total number of ways to choose $n$ objects from a population of size $N$ is:

$$
\binom{N}{n}
$$

Using the combination formula:

$$
\binom{N}{n}
=
\frac{N!}{n!(N-n)!}
$$

---

## Step 4 — Build the probability

The number of favorable samples is:

$$
\binom{K}{k}\binom{N-K}{n-k}
$$

The total number of possible samples is:

$$
\binom{N}{n}
$$

Therefore:

$$
P(X=k)
=
\frac{\text{favorable samples}}{\text{all possible samples}}
$$

So:

$$
P(X=k)
=
\frac{\binom{K}{k}\binom{N-K}{n-k}}
{\binom{N}{n}}
$$

---

## Explanation of parameters

In the formula:

$$
P(X=k)
=
\frac{\binom{K}{k}\binom{N-K}{n-k}}
{\binom{N}{n}}
$$

we have:

* $N$: total population size.
* $K$: number of distinguished or success-type objects in the population.
* $N-K$: number of failure-type objects in the population.
* $n$: sample size.
* $k$: number of success-type objects in the sample.
* $X$: random variable counting the number of successes.

---

# 2. Support of the Random Variable

---

The random variable $X$ can take values from the smallest possible number of successes to the largest possible number of successes.

The support is:

$$
X \in \{\max(0,n-(N-K)), \dots, \min(n,K)\}
$$

---

## Lower bound

The number of successes cannot be negative.

So:

$$
X \ge 0
$$

However, if the sample size is large, we may be forced to pick some successes.

There are:

$$
N-K
$$

failure-type objects.

If we draw:

$$
n
$$

objects and there are not enough failures, then we must draw successes.

The minimum number of successes is:

$$
n-(N-K)
$$

So the real lower bound is:

$$
\max(0,n-(N-K))
$$

---

## Upper bound

We cannot pick more successes than the sample size.

So:

$$
X \le n
$$

We also cannot pick more successes than the number of successes in the population.

So:

$$
X \le K
$$

Therefore, the upper bound is:

$$
\min(n,K)
$$

---

# 3. CDF of the Hypergeometric Distribution

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

## Why summation is used

Because the hypergeometric distribution is discrete.

So:

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

# 4. Shape Behavior of the PMF

---

The hypergeometric distribution is similar to the binomial distribution, but it does not assume independence.

The reason is that the sampling is done without replacement.

When the population is large compared to the sample size, the hypergeometric distribution becomes close to the binomial distribution.

In words:

Hypergeometric with parameters $N$, $K$, and $n$ is approximately binomial with sample size $n$ and success probability:

$$
p=\frac{K}{N}
$$

This approximation works when $N$ is large compared to $n$.

For example, if:

$$
N=100000
$$

then removing one object gives:

$$
100000-1=99999
$$

The population size barely changes.

So the success probability is almost constant.

Therefore, the hypergeometric distribution becomes close to the binomial distribution.

---

# 5. Effect of Parameters

---

## Increasing the sample size

The expected value of a hypergeometric random variable is:

$$
E(X)=n\frac{K}{N}
$$

If $n$ increases, then:

$$
n\frac{K}{N}
$$

also increases.

Therefore:

* the expected number of successes increases,
* the distribution shifts to the right,
* the possible range of values becomes larger.

---

## Increasing the number of distinguished objects

The expected value is:

$$
E(X)=n\frac{K}{N}
$$

If $K$ increases, then:

$$
\frac{K}{N}
$$

increases.

Therefore:

$$
n\frac{K}{N}
$$

also increases.

So:

* the distribution shifts to the right,
* the probability of getting more successes increases,
* the expected number of successes increases.

---

## Changing population size

When $N$ is large compared to $n$, removing one object does not change the probabilities very much.

So the hypergeometric distribution becomes close to the binomial distribution with:

$$
p=\frac{K}{N}
$$

When $N$ is small, removing one object changes the population a lot.

So the dependence effect becomes stronger.

---

# 6. Detailed Probability Computations

We use this example:

$$
N=50
$$

$$
K=10
$$

$$
n=5
$$

So:

$$
N-K=50-10
$$

$$
N-K=40
$$

The denominator is:

$$
\binom{50}{5}
$$

Now compute it step by step:

$$
\binom{50}{5}
=
\frac{50!}{5!(50-5)!}
$$

$$
50-5=45
$$

So:

$$
\binom{50}{5}
=
\frac{50!}{5!45!}
$$

Cancel $45!$:

$$
\binom{50}{5}
=
\frac{50\cdot49\cdot48\cdot47\cdot46}{5\cdot4\cdot3\cdot2\cdot1}
$$

Compute the numerator:

$$
50\cdot49=2450
$$

$$
2450\cdot48=117600
$$

$$
117600\cdot47=5527200
$$

$$
5527200\cdot46=254251200
$$

Compute the denominator:

$$
5\cdot4=20
$$

$$
20\cdot3=60
$$

$$
60\cdot2=120
$$

$$
120\cdot1=120
$$

So:

$$
\binom{50}{5}
=
\frac{254251200}{120}
$$

$$
\binom{50}{5}
=
2118760
$$

Therefore:

$$
\binom{50}{5}=2118760
$$

---

## Exact probability example

We compute the probability of getting exactly $2$ successes.

That is:

$$
P(X=2)
$$

Using the PMF formula:

$$
P(X=2)
=
\frac{\binom{10}{2}\binom{40}{5-2}}
{\binom{50}{5}}
$$

First compute:

$$
5-2=3
$$

So:

$$
P(X=2)
=
\frac{\binom{10}{2}\binom{40}{3}}
{\binom{50}{5}}
$$

Now compute:

$$
\binom{10}{2}
=
\frac{10!}{2!(10-2)!}
$$

$$
10-2=8
$$

So:

$$
\binom{10}{2}
=
\frac{10!}{2!8!}
$$

Cancel $8!$:

$$
\binom{10}{2}
=
\frac{10\cdot9}{2\cdot1}
$$

Compute:

$$
10\cdot9=90
$$

$$
2\cdot1=2
$$

So:

$$
\binom{10}{2}
=
\frac{90}{2}
$$

$$
\binom{10}{2}=45
$$

Now compute:

$$
\binom{40}{3}
=
\frac{40!}{3!(40-3)!}
$$

$$
40-3=37
$$

So:

$$
\binom{40}{3}
=
\frac{40!}{3!37!}
$$

Cancel $37!$:

$$
\binom{40}{3}
=
\frac{40\cdot39\cdot38}{3\cdot2\cdot1}
$$

Compute the numerator:

$$
40\cdot39=1560
$$

$$
1560\cdot38=59280
$$

Compute the denominator:

$$
3\cdot2\cdot1=6
$$

So:

$$
\binom{40}{3}
=
\frac{59280}{6}
$$

$$
\binom{40}{3}=9880
$$

Now substitute everything:

$$
P(X=2)
=
\frac{45\cdot9880}{2118760}
$$

Compute the numerator:

$$
45\cdot9880=444600
$$

So:

$$
P(X=2)
=
\frac{444600}{2118760}
$$

Divide:

$$
P(X=2)\approx0.2098
$$

---

## Cumulative probability example

We compute:

$$
P(X \le 2)
$$

This means:

$$
P(X \le 2)=P(X=0)+P(X=1)+P(X=2)
$$

---

### Calculate P of X equals 0

$$
P(X=0)
=
\frac{\binom{10}{0}\binom{40}{5}}
{\binom{50}{5}}
$$

$$
\binom{10}{0}=1
$$

$$
\binom{40}{5}=658008
$$

So:

$$
P(X=0)
=
\frac{1\cdot658008}{2118760}
$$

$$
P(X=0)
=
\frac{658008}{2118760}
$$

$$
P(X=0)\approx0.3106
$$

---

### Calculate P of X equals 1

$$
P(X=1)
=
\frac{\binom{10}{1}\binom{40}{4}}
{\binom{50}{5}}
$$

$$
\binom{10}{1}=10
$$

$$
\binom{40}{4}=91390
$$

Compute:

$$
10\cdot91390=913900
$$

So:

$$
P(X=1)
=
\frac{913900}{2118760}
$$

Divide:

$$
P(X=1)\approx0.4313
$$

---

### Use previous value for P of X equals 2

From the previous calculation:

$$
P(X=2)
=
\frac{444600}{2118760}
$$

---

### Add the probabilities

Now:

$$
P(X \le 2)
=
\frac{658008}{2118760}
+
\frac{913900}{2118760}
+
\frac{444600}{2118760}
$$

Since the denominators are the same, we add the numerators.

First:

$$
658008+913900=1571908
$$

Then:

$$
1571908+444600=2016508
$$

So:

$$
P(X \le 2)
=
\frac{2016508}{2118760}
$$

Divide:

$$
P(X \le 2)\approx0.9517
$$

---

## Tail probability example

We compute:

$$
P(X \ge 3)
$$

This is the complement of:

$$
P(X \le 2)
$$

So:

$$
P(X \ge 3)=1-P(X \le 2)
$$

From above:

$$
P(X \le 2)=\frac{2016508}{2118760}
$$

Write $1$ with the same denominator:

$$
1=\frac{2118760}{2118760}
$$

Therefore:

$$
P(X \ge 3)
=
\frac{2118760}{2118760}
-
\frac{2016508}{2118760}
$$

Subtract the numerators:

$$
2118760-2016508=102252
$$

So:

$$
P(X \ge 3)
=
\frac{102252}{2118760}
$$

Divide:

$$
P(X \ge 3)\approx0.0483
$$

---

## Interval probability example

We compute:

$$
P(1 \le X \le 3)
$$

This means:

$$
P(1 \le X \le 3)
=
P(X=1)+P(X=2)+P(X=3)
$$

We already have:

$$
P(X=1)
=
\frac{913900}{2118760}
$$

and:

$$
P(X=2)
=
\frac{444600}{2118760}
$$

Now compute:

$$
P(X=3)
$$

Using the PMF formula:

$$
P(X=3)
=
\frac{\binom{10}{3}\binom{40}{5-3}}
{\binom{50}{5}}
$$

Compute:

$$
5-3=2
$$

So:

$$
P(X=3)
=
\frac{\binom{10}{3}\binom{40}{2}}
{\binom{50}{5}}
$$

Compute:

$$
\binom{10}{3}
=
\frac{10\cdot9\cdot8}{3\cdot2\cdot1}
$$

$$
10\cdot9=90
$$

$$
90\cdot8=720
$$

$$
3\cdot2\cdot1=6
$$

So:

$$
\binom{10}{3}
=
\frac{720}{6}
$$

$$
\binom{10}{3}=120
$$

Compute:

$$
\binom{40}{2}
=
\frac{40\cdot39}{2\cdot1}
$$

$$
40\cdot39=1560
$$

$$
2\cdot1=2
$$

So:

$$
\binom{40}{2}
=
\frac{1560}{2}
$$

$$
\binom{40}{2}=780
$$

Now substitute:

$$
P(X=3)
=
\frac{120\cdot780}{2118760}
$$

Compute:

$$
120\cdot780=93600
$$

So:

$$
P(X=3)
=
\frac{93600}{2118760}
$$

Now add:

$$
P(1 \le X \le 3)
=
\frac{913900}{2118760}
+
\frac{444600}{2118760}
+
\frac{93600}{2118760}
$$

Add the numerators:

$$
913900+444600=1358500
$$

$$
1358500+93600=1452100
$$

So:

$$
P(1 \le X \le 3)
=
\frac{1452100}{2118760}
$$

Divide:

$$
P(1 \le X \le 3)\approx0.6854
$$

---

# 7. Hypergeometric Model vs Binomial Model

---

## Binomial distribution

The binomial distribution is used when:

* trials are independent,
* the probability of success is constant,
* sampling is with replacement or the population is effectively infinite.

Its PMF is:

$$
P(Y=k)=\binom{n}{k}p^k(1-p)^{n-k}
$$

---

## Hypergeometric distribution

The hypergeometric distribution is used when:

* draws are dependent,
* sampling is without replacement,
* the population is finite.

Its PMF is:

$$
P(X=k)
=
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
| parameter $p$ | parameters $N$, $K$, $n$ |

---

# 8. Real-World Applications

---

## Quality inspection

A factory produces a batch of products.

Some products are defective and some are not defective.

If we inspect a few products without replacement, then the number of defective products in the sample follows a hypergeometric distribution.

---

## Card games

Cards are drawn from a deck without replacement.

The number of aces, hearts, or special cards in a hand can be modeled by a hypergeometric distribution.

---

## Election sampling

A fixed population contains voters with different preferences.

If we select voters without replacement, the number of voters supporting a candidate can be modeled with a hypergeometric distribution.

---

## Biology

In biology, we may sample genes, organisms, or individuals from a finite population.

The number of individuals with a certain trait can be modeled using a hypergeometric distribution.

---

# 9. PMF Graphs for Several Parameter Choices

The following graphs are written as Markdown bar charts.

Each bar shows the relative size of the probability.

---

## PMF Graph 1

Parameters:

$$
N=50
$$

$$
K=10
$$

$$
n=5
$$

So:

$$
N-K=50-10=40
$$

The denominator is:

$$
\binom{50}{5}=2118760
$$

The PMF formula becomes:

$$
P(X=k)
=
\frac{\binom{10}{k}\binom{40}{5-k}}
{2118760}
$$

| k | P(X = k) | PMF graph |
|---:|---:|---|
| 0 | 0.3106 | ██████████████ |
| 1 | 0.4313 | ████████████████████ |
| 2 | 0.2098 | ██████████ |
| 3 | 0.0442 | ██ |
| 4 | 0.0040 | █ |
| 5 | 0.0001 | █ |

This distribution is skewed because the number of success-type objects is relatively small compared to the full population.

---

## PMF Graph 2

Parameters:

$$
N=50
$$

$$
K=25
$$

$$
n=5
$$

So:

$$
N-K=50-25=25
$$

The denominator is:

$$
\binom{50}{5}=2118760
$$

The PMF formula becomes:

$$
P(X=k)
=
\frac{\binom{25}{k}\binom{25}{5-k}}
{2118760}
$$

| k | Calculation | Numerator | P(X = k) | PMF graph |
|---:|---|---:|---:|---|
| 0 | C(25,0) C(25,5) = 1 x 53130 | 53130 | 0.0251 | ██ |
| 1 | C(25,1) C(25,4) = 25 x 12650 | 316250 | 0.1493 | █████████ |
| 2 | C(25,2) C(25,3) = 300 x 2300 | 690000 | 0.3257 | ████████████████████ |
| 3 | C(25,3) C(25,2) = 2300 x 300 | 690000 | 0.3257 | ████████████████████ |
| 4 | C(25,4) C(25,1) = 12650 x 25 | 316250 | 0.1493 | █████████ |
| 5 | C(25,5) C(25,0) = 53130 x 1 | 53130 | 0.0251 | ██ |

This distribution is almost symmetric because half of the population consists of success-type objects.

---

## PMF Graph 3

Parameters:

$$
N=50
$$

$$
K=25
$$

$$
n=15
$$

So:

$$
N-K=50-25=25
$$

The denominator is:

$$
\binom{50}{15}=2250829575120
$$

The PMF formula becomes:

$$
P(X=k)
=
\frac{\binom{25}{k}\binom{25}{15-k}}
{2250829575120}
$$

| k | Numerator | P(X = k) | PMF graph |
|---:|---:|---:|---|
| 0 | 3268760 | 0.000001 |  |
| 1 | 111435000 | 0.000050 |  |
| 2 | 1560090000 | 0.0007 | █ |
| 3 | 11960690000 | 0.0053 | █ |
| 4 | 56386110000 | 0.0251 | ██ |
| 5 | 173669218800 | 0.0772 | ███████ |
| 6 | 361810872500 | 0.1607 | ██████████████ |
| 7 | 519913102500 | 0.2310 | ████████████████████ |
| 8 | 519913102500 | 0.2310 | ████████████████████ |
| 9 | 361810872500 | 0.1607 | ██████████████ |
| 10 | 173669218800 | 0.0772 | ███████ |
| 11 | 56386110000 | 0.0251 | ██ |
| 12 | 11960690000 | 0.0053 | █ |
| 13 | 1560090000 | 0.0007 | █ |
| 14 | 111435000 | 0.000050 |  |
| 15 | 3268760 | 0.000001 |  |

This distribution has a wider range because the sample size is larger.

---

# 10. CDF Graphs for the Same Parameter Choices

The CDF is the cumulative sum of PMF values.

So:

$$
F(k)=P(X \le k)
$$

and:

$$
F(k)=P(X=0)+P(X=1)+\cdots+P(X=k)
$$

---

## CDF Graph 1

Parameters:

$$
N=50
$$

$$
K=10
$$

$$
n=5
$$

Using the PMF values from Graph 1:

$$
P(X=0)=0.3106
$$

$$
P(X=1)=0.4313
$$

$$
P(X=2)=0.2098
$$

$$
P(X=3)=0.0442
$$

$$
P(X=4)=0.0040
$$

$$
P(X=5)=0.0001
$$

Now compute the CDF step by step.

For $k=0$:

$$
F(0)=P(X=0)
$$

$$
F(0)=0.3106
$$

For $k=1$:

$$
F(1)=P(X=0)+P(X=1)
$$

$$
F(1)=0.3106+0.4313
$$

$$
F(1)=0.7419
$$

For $k=2$:

$$
F(2)=P(X=0)+P(X=1)+P(X=2)
$$

$$
F(2)=0.3106+0.4313+0.2098
$$

First:

$$
0.3106+0.4313=0.7419
$$

Then:

$$
0.7419+0.2098=0.9517
$$

So:

$$
F(2)=0.9517
$$

For $k=3$:

$$
F(3)=F(2)+P(X=3)
$$

$$
F(3)=0.9517+0.0442
$$

$$
F(3)=0.9959
$$

For $k=4$:

$$
F(4)=F(3)+P(X=4)
$$

$$
F(4)=0.9959+0.0040
$$

$$
F(4)=0.9999
$$

For $k=5$:

$$
F(5)=F(4)+P(X=5)
$$

$$
F(5)=0.9999+0.0001
$$

$$
F(5)=1.0000
$$

| k | F(k) = P(X <= k) | CDF graph |
|---:|---:|---|
| 0 | 0.3106 | ██████ |
| 1 | 0.7419 | ███████████████ |
| 2 | 0.9517 | ███████████████████ |
| 3 | 0.9959 | ████████████████████ |
| 4 | 0.9999 | ████████████████████ |
| 5 | 1.0000 | ████████████████████ |

---

## CDF Graph 2

Parameters:

$$
N=50
$$

$$
K=25
$$

$$
n=5
$$

The CDF is computed by adding PMF values step by step.

| k | CDF calculation | F(k) | CDF graph |
|---:|---|---:|---|
| 0 | 0.0251 | 0.0251 | █ |
| 1 | 0.0251 + 0.1493 | 0.1743 | ███ |
| 2 | 0.1743 + 0.3257 | 0.5000 | ██████████ |
| 3 | 0.5000 + 0.3257 | 0.8257 | █████████████████ |
| 4 | 0.8257 + 0.1493 | 0.9749 | ███████████████████ |
| 5 | 0.9749 + 0.0251 | 1.0000 | ████████████████████ |

---

## CDF Graph 3

Parameters:

$$
N=50
$$

$$
K=25
$$

$$
n=15
$$

The CDF is again computed by cumulative addition.

| k | F(k) = P(X <= k) | CDF graph |
|---:|---:|---|
| 0 | 0.000001 |  |
| 1 | 0.000051 |  |
| 2 | 0.000744 |  |
| 3 | 0.006058 | █ |
| 4 | 0.031109 | █ |
| 5 | 0.108267 | ██ |
| 6 | 0.269013 | █████ |
| 7 | 0.500000 | ██████████ |
| 8 | 0.730987 | ███████████████ |
| 9 | 0.891733 | ██████████████████ |
| 10 | 0.968891 | ███████████████████ |
| 11 | 0.993942 | ████████████████████ |
| 12 | 0.999256 | ████████████████████ |
| 13 | 0.999949 | ████████████████████ |
| 14 | 0.999999 | ████████████████████ |
| 15 | 1.000000 | ████████████████████ |

---

# 11. Application with Binomial Comparison

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

Then $X$ follows a hypergeometric distribution with parameters:

$$
N=100
$$

$$
K=20
$$

$$
n=10
$$

The corresponding binomial approximation uses:

$$
p=\frac{K}{N}
$$

Substitute:

$$
p=\frac{20}{100}
$$

Divide numerator and denominator by $20$:

$$
\frac{20}{100}=\frac{1}{5}
$$

So:

$$
p=0.2
$$

Therefore, the binomial approximation has parameters:

$$
n=10
$$

and:

$$
p=0.2
$$

---

## Detailed hypergeometric calculation for k equals 2

For the hypergeometric model:

$$
P(X=2)
=
\frac{\binom{20}{2}\binom{80}{8}}
{\binom{100}{10}}
$$

Compute:

$$
\binom{20}{2}
=
\frac{20\cdot19}{2\cdot1}
$$

$$
20\cdot19=380
$$

$$
2\cdot1=2
$$

$$
\binom{20}{2}
=
\frac{380}{2}
$$

$$
\binom{20}{2}=190
$$

Also:

$$
\binom{80}{8}=28987537150
$$

and:

$$
\binom{100}{10}=17310309456440
$$

Now substitute:

$$
P(X=2)
=
\frac{190\cdot28987537150}
{17310309456440}
$$

Compute the numerator:

$$
190\cdot28987537150=5507632058500
$$

So:

$$
P(X=2)
=
\frac{5507632058500}{17310309456440}
$$

Divide:

$$
P(X=2)\approx0.3182
$$

---

## Detailed binomial calculation for k equals 2

For the binomial model:

$$
P(Y=2)
=
\binom{10}{2}(0.2)^2(1-0.2)^{10-2}
$$

First:

$$
1-0.2=0.8
$$

and:

$$
10-2=8
$$

So:

$$
P(Y=2)
=
\binom{10}{2}(0.2)^2(0.8)^8
$$

Compute:

$$
\binom{10}{2}=45
$$

Compute:

$$
(0.2)^2=0.2\cdot0.2
$$

$$
(0.2)^2=0.04
$$

Compute:

$$
(0.8)^8=0.16777216
$$

Now multiply step by step:

$$
45\cdot0.04=1.8
$$

Then:

$$
1.8\cdot0.16777216=0.301989888
$$

Therefore:

$$
P(Y=2)\approx0.3020
$$

---

## Hypergeometric vs Binomial PMF comparison

| k | Hypergeometric P(X = k) | Hypergeometric graph | Binomial P(Y = k) | Binomial graph |
|---:|---:|---|---:|---|
| 0 | 0.0951 | ██████ | 0.1074 | ███████ |
| 1 | 0.2679 | █████████████████ | 0.2684 | █████████████████ |
| 2 | 0.3182 | ████████████████████ | 0.3020 | ███████████████████ |
| 3 | 0.2092 | █████████████ | 0.2013 | █████████████ |
| 4 | 0.0841 | █████ | 0.0881 | ██████ |
| 5 | 0.0215 | █ | 0.0264 | ██ |
| 6 | 0.0035 | █ | 0.0055 | █ |
| 7 | 0.0004 | █ | 0.0008 | █ |
| 8 | 0.000023 |  | 0.000074 |  |
| 9 | 0.0000008 |  | 0.000004 |  |
| 10 | 0.00000001 |  | 0.0000001 |  |

---

## Interpretation of the comparison

The hypergeometric distribution is the correct model because the products are sampled without replacement.

The binomial distribution is only an approximation.

The two distributions are close in this example because the population size is:

$$
N=100
$$

and the sample size is:

$$
n=10
$$

Since $N$ is large compared to $n$, removing one object from the population does not change the probabilities very much.

Therefore, the hypergeometric distribution can be approximated by a binomial distribution with:

$$
p=\frac{K}{N}
$$

---

# Final Summary

---

We built the hypergeometric model step by step.

## Experiment

The experiment is sampling without replacement from a finite population.

---

## Sample space

The sample space is:

$$
\Omega
=
\{\text{all subsets of size } n \text{ from } \{1,2,\dots,N\}\}
$$

---

## Elementary outcome

An elementary outcome is:

$$
\omega \subseteq \{1,2,\dots,N\}
$$

with:

$$
|\omega|=n
$$

---

## Random variable

The random variable is:

$$
X(\omega)=\text{number of distinguished objects in the sample}
$$

---

## PMF

The probability mass function is:

$$
P(X=k)
=
\frac{\binom{K}{k}\binom{N-K}{n-k}}
{\binom{N}{n}}
$$

---

## Support

The support is:

$$
X \in \{\max(0,n-(N-K)), \dots, \min(n,K)\}
$$

---

## CDF

The cumulative distribution function is:

$$
F(k)
=
\sum_{i=\max(0,n-(N-K))}^{k}
\frac{\binom{K}{i}\binom{N-K}{n-i}}
{\binom{N}{n}}
$$

---

## Core idea

The hypergeometric distribution models the number of successes when sampling without replacement from a finite population.

It is different from the binomial distribution because the draws are dependent and the probability of success changes after each draw.