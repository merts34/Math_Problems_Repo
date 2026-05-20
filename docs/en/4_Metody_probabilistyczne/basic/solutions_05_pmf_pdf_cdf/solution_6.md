

---

# Task 6 — Hypergeometric Distribution

In this task, we study the hypergeometric distribution using a simple red-ball example.

Assume that we have a box containing 10 balls.

There are:

$$
4 \text{ red balls}
$$

and

$$
6 \text{ white balls}.
$$

We randomly select 3 balls from the box without replacement.

Therefore,

$$
N = 10
$$

is the total number of balls,

$$
K = 4
$$

is the number of red balls,

$$
N-K = 10-4 = 6
$$

is the number of white balls, and

$$
n = 3
$$

is the number of selected balls.

Let

$$
X = \text{the number of red balls in the sample}.
$$

In this example, red balls are the distinguished objects.

---

# 0. Random Experiment, Sample Space, Elementary Outcome, and Random Variable

The random experiment is selecting 3 balls from a box of 10 balls without replacement.

The phrase “without replacement” means that once a ball is selected, it is not put back into the box before the next selection.

For example, if we first select one ball, then the number of balls in the box decreases from 10 to 9. After the second selection, it decreases from 9 to 8.

So the selections are dependent, because the result of one selection changes the contents of the box for the next selection.

The population is:

$$
{1,2,3,4,5,6,7,8,9,10}.
$$

Assume that the red balls are:

$$
{1,2,3,4}
$$

and the white balls are:

$$
{5,6,7,8,9,10}.
$$

The sample space is the set of all possible samples of size 3 from the 10 balls.

So,

$$
\Omega = { \text{all possible groups of 3 balls chosen from 10 balls} }.
$$

Some possible elementary outcomes are:

$$
{1,2,3},
$$

$$
{1,5,9},
$$

$$
{2,6,10},
$$

$$
{5,7,8}.
$$

An elementary outcome is one particular result of the experiment.

For example,

$$
\omega = {2,5,9}
$$

is one elementary outcome.

Now we define the random variable:

$$
X(\omega) = \text{the number of red balls in the selected sample}.
$$

If

$$
\omega = {2,5,9},
$$

then only ball 2 is red. Balls 5 and 9 are white.

Therefore,

$$
X(\omega) = 1.
$$

If

$$
\omega = {1,3,8},
$$

then balls 1 and 3 are red, and ball 8 is white.

Therefore,

$$
X(\omega) = 2.
$$

If

$$
\omega = {5,6,9},
$$

then none of the selected balls are red.

Therefore,

$$
X(\omega) = 0.
$$

If

$$
\omega = {1,2,4},
$$

then all selected balls are red.

Therefore,

$$
X(\omega) = 3.
$$

So, in this experiment, the random variable $X$ can count how many red balls appear in the sample.

---

# 1. PMF of the Hypergeometric Distribution

The PMF means probability mass function.

It gives the probability that the random variable $X$ takes a specific value.

In this problem,

$$
P(X=k)
$$

means the probability that exactly $k$ red balls are selected.

The hypergeometric PMF is:

$$
P(X=k)
=

\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}.
$$

For our example,

$$
N=10,
$$

$$
K=4,
$$

$$
N-K=6,
$$

and

$$
n=3.
$$

Therefore,

$$
P(X=k)
=

\frac{\binom{4}{k}\binom{6}{3-k}}{\binom{10}{3}}.
$$

Now we explain the formula.

The term

$$
\binom{4}{k}
$$

means choosing $k$ red balls from 4 red balls.

The term

$$
\binom{6}{3-k}
$$

means choosing the remaining $3-k$ balls from the 6 white balls.

The denominator

$$
\binom{10}{3}
$$

means choosing any 3 balls from the total 10 balls.

So the formula is based on:

$$
\text{Probability}
=

\frac{\text{Number of favorable outcomes}}{\text{Number of all possible outcomes}}.
$$

---

# 2. Support of the Random Variable

The support is the set of all possible values that $X$ can take.

In this problem, we select 3 balls.

So the number of red balls in the sample can be:

$$
0,1,2,3.
$$

It cannot be 4, because we only select 3 balls.

Therefore, the support is:

$$
{0,1,2,3}.
$$

So,

$$
X \in {0,1,2,3}.
$$

---

# 3. PMF Calculations and PMF Graph

We first calculate the denominator:

$$
\binom{10}{3}
=

\frac{10 \cdot 9 \cdot 8}{3 \cdot 2 \cdot 1}.
$$

Now calculate the numerator:

$$
10 \cdot 9 \cdot 8 = 720.
$$

And the denominator:

$$
3 \cdot 2 \cdot 1 = 6.
$$

Therefore,

$$
\binom{10}{3}
=
\frac{720}{6}
=
120.
$$

So there are 120 possible ways to choose 3 balls from 10 balls.

---

## Case 1: $P(X=0)$

This means selecting exactly 0 red balls.

So we need:

$$
0 \text{ red balls}
$$

and

$$
3 \text{ white balls}.
$$

Using the formula:

$$
P(X=0)
=

\frac{\binom{4}{0}\binom{6}{3}}{\binom{10}{3}}.
$$

First,

$$
\binom{4}{0}=1.
$$

This is because there is exactly one way to choose nothing.

Now calculate:

$$
\binom{6}{3}
=

\frac{6 \cdot 5 \cdot 4}{3 \cdot 2 \cdot 1}.
$$

The numerator is:

$$
6 \cdot 5 \cdot 4 = 120.
$$

The denominator is:

$$
3 \cdot 2 \cdot 1 = 6.
$$

Therefore,

$$
\binom{6}{3}
=
\frac{120}{6}
=
20.
$$

Now substitute:

$$
P(X=0)
=

\frac{1 \cdot 20}{120}.
$$

So,

$$
P(X=0)
=

\frac{20}{120}.
$$

Simplify:

$$
P(X=0)
=

\frac{1}{6}.
$$

Decimal form:

$$
P(X=0)
\approx 0.1667.
$$

---

## Case 2: $P(X=1)$

This means selecting exactly 1 red ball.

So we need:

$$
1 \text{ red ball}
$$

and

$$
2 \text{ white balls}.
$$

Using the formula:

$$
P(X=1)
=

\frac{\binom{4}{1}\binom{6}{2}}{\binom{10}{3}}.
$$

First,

$$
\binom{4}{1}=4.
$$

Now calculate:

$$
\binom{6}{2}
=

\frac{6 \cdot 5}{2 \cdot 1}.
$$

The numerator is:

$$
6 \cdot 5 = 30.
$$

The denominator is:

$$
2 \cdot 1 = 2.
$$

Therefore,

$$
\binom{6}{2}
=
\frac{30}{2}
=
15.
$$

Now substitute:

$$
P(X=1)
=

\frac{4 \cdot 15}{120}.
$$

Multiply:

$$
4 \cdot 15 = 60.
$$

Therefore,

$$
P(X=1)
=

\frac{60}{120}.
$$

Simplify:

$$
P(X=1)
=

\frac{1}{2}.
$$

Decimal form:

$$
P(X=1)
=

0.5.
$$

---

## Case 3: $P(X=2)$

This means selecting exactly 2 red balls.

So we need:

$$
2 \text{ red balls}
$$

and

$$
1 \text{ white ball}.
$$

Using the formula:

$$
P(X=2)
=

\frac{\binom{4}{2}\binom{6}{1}}{\binom{10}{3}}.
$$

First calculate:

$$
\binom{4}{2}
=

\frac{4 \cdot 3}{2 \cdot 1}.
$$

The numerator is:

$$
4 \cdot 3 = 12.
$$

The denominator is:

$$
2 \cdot 1 = 2.
$$

Therefore,

$$
\binom{4}{2}
=
\frac{12}{2}
=
6.
$$

Also,

$$
\binom{6}{1}=6.
$$

Now substitute:

$$
P(X=2)
=

\frac{6 \cdot 6}{120}.
$$

Multiply:

$$
6 \cdot 6 = 36.
$$

Therefore,

$$
P(X=2)
=

\frac{36}{120}.
$$

Simplify:

$$
P(X=2)
=

\frac{3}{10}.
$$

Decimal form:

$$
P(X=2)
=

0.3.
$$

---

## Case 4: $P(X=3)$

This means selecting exactly 3 red balls.

So we need:

$$
3 \text{ red balls}
$$

and

$$
0 \text{ white balls}.
$$

Using the formula:

$$
P(X=3)
=

\frac{\binom{4}{3}\binom{6}{0}}{\binom{10}{3}}.
$$

First,

$$
\binom{4}{3}=4.
$$

Also,

$$
\binom{6}{0}=1.
$$

Now substitute:

$$
P(X=3)
=

\frac{4 \cdot 1}{120}.
$$

Therefore,

$$
P(X=3)
=

\frac{4}{120}.
$$

Simplify:

$$
P(X=3)
=

\frac{1}{30}.
$$

Decimal form:

$$
P(X=3)
\approx 0.0333.
$$

---

## PMF Table

| $x$ | Meaning             | $P(X=x)$ |
| --: | ------------------- | -------: |
|   0 | No red balls        | $0.1667$ |
|   1 | Exactly 1 red ball  | $0.5000$ |
|   2 | Exactly 2 red balls | $0.3000$ |
|   3 | Exactly 3 red balls | $0.0333$ |

The probabilities add up to 1:

$$
0.1667 + 0.5000 + 0.3000 + 0.0333 = 1.
$$

---

## PMF Graph

The PMF graph has $x$ values on the horizontal axis and probabilities on the vertical axis.

| $x$ | $P(X=x)$ | Bar             |
| --: | -------: | --------------- |
|   0 |   0.1667 | █████           |
|   1 |   0.5000 | ███████████████ |
|   2 |   0.3000 | █████████       |
|   3 |   0.0333 | █               |

The largest probability is at:

$$
X=1.
$$

So, in this example, the most likely result is selecting exactly 1 red ball.

---

# 4. CDF Calculations and CDF Graph

The CDF means cumulative distribution function.

It is defined as:

$$
F(k)=P(X \leq k).
$$

This means the probability that $X$ is less than or equal to $k$.

We already know:

$$
P(X=0)=\frac{20}{120},
$$

$$
P(X=1)=\frac{60}{120},
$$

$$
P(X=2)=\frac{36}{120},
$$

$$
P(X=3)=\frac{4}{120}.
$$

---

## $F(0)=P(X \leq 0)$

This includes only:

$$
X=0.
$$

So,

$$
F(0)=P(X=0).
$$

Therefore,

$$
F(0)=\frac{20}{120}.
$$

So,

$$
F(0)=0.1667.
$$

---

## $F(1)=P(X \leq 1)$

This includes:

$$
X=0
$$

and

$$
X=1.
$$

So,

$$
F(1)=P(X=0)+P(X=1).
$$

Substitute:

$$
F(1)=\frac{20}{120}+\frac{60}{120}.
$$

Add the numerators:

$$
20+60=80.
$$

Therefore,

$$
F(1)=\frac{80}{120}.
$$

Simplify:

$$
F(1)=\frac{2}{3}.
$$

Decimal form:

$$
F(1)\approx 0.6667.
$$

---

## $F(2)=P(X \leq 2)$

This includes:

$$
X=0,
$$

$$
X=1,
$$

and

$$
X=2.
$$

So,

$$
F(2)=P(X=0)+P(X=1)+P(X=2).
$$

Substitute:

$$
F(2)=\frac{20}{120}+\frac{60}{120}+\frac{36}{120}.
$$

Add the numerators:

$$
20+60+36=116.
$$

Therefore,

$$
F(2)=\frac{116}{120}.
$$

Simplify:

$$
F(2)=\frac{29}{30}.
$$

Decimal form:

$$
F(2)\approx 0.9667.
$$

---

## $F(3)=P(X \leq 3)$

This includes all possible values of $X$:

$$
X=0,1,2,3.
$$

Therefore,

$$
F(3)=1.
$$

---

## CDF Table

| $k$ | $F(k)=P(X \leq k)$ |
| --: | -----------------: |
|   0 |           $0.1667$ |
|   1 |           $0.6667$ |
|   2 |           $0.9667$ |
|   3 |           $1.0000$ |

---

## CDF Graph

The CDF graph is a step graph.

| $k$ | $F(k)$ | Bar                            |
| --: | -----: | ------------------------------ |
|   0 | 0.1667 | █████                          |
|   1 | 0.6667 | ████████████████████           |
|   2 | 0.9667 | █████████████████████████████  |
|   3 | 1.0000 | ██████████████████████████████ |

The CDF always increases or stays the same. It never decreases.

---

# 5. Effect of Parameter Changes

Now we explain how the distribution changes when parameters change.

---

## 5.1. Effect of Changing the Sample Size

In the original example,

$$
N=10,
$$

$$
K=4,
$$

and

$$
n=3.
$$

Now suppose we still have 10 balls and 4 red balls, but we select 5 balls instead of 3.

So now:

$$
N=10,
$$

$$
K=4,
$$

$$
n=5.
$$

The random variable is still:

$$
X = \text{the number of red balls in the sample}.
$$

The total number of possible samples is:

$$
\binom{10}{5}.
$$

Calculate:

$$
\binom{10}{5}
=

\frac{10 \cdot 9 \cdot 8 \cdot 7 \cdot 6}{5 \cdot 4 \cdot 3 \cdot 2 \cdot 1}.
$$

The numerator is:

$$
10 \cdot 9 \cdot 8 \cdot 7 \cdot 6 = 30240.
$$

The denominator is:

$$
5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120.
$$

Therefore,

$$
\binom{10}{5}
=
\frac{30240}{120}
=
252.
$$

The PMF is:

$$
P(X=k)
=

\frac{\binom{4}{k}\binom{6}{5-k}}{\binom{10}{5}}.
$$

The possible values are:

$$
X=0,1,2,3,4.
$$

---

## PMF for $n=5$

### $P(X=0)$

$$
P(X=0)
=

\frac{\binom{4}{0}\binom{6}{5}}{\binom{10}{5}}.
$$

$$
\binom{4}{0}=1.
$$

$$
\binom{6}{5}=6.
$$

Therefore,

$$
P(X=0)
=
\frac{1 \cdot 6}{252}
=
\frac{6}{252}
\approx 0.0238.
$$

---

### $P(X=1)$

$$
P(X=1)
=

\frac{\binom{4}{1}\binom{6}{4}}{\binom{10}{5}}.
$$

$$
\binom{4}{1}=4.
$$

$$
\binom{6}{4}=15.
$$

Therefore,

$$
P(X=1)
=
\frac{4 \cdot 15}{252}
=
\frac{60}{252}
\approx 0.2381.
$$

---

### $P(X=2)$

$$
P(X=2)
=

\frac{\binom{4}{2}\binom{6}{3}}{\binom{10}{5}}.
$$

$$
\binom{4}{2}=6.
$$

$$
\binom{6}{3}=20.
$$

Therefore,

$$
P(X=2)
=
\frac{6 \cdot 20}{252}
=
\frac{120}{252}
\approx 0.4762.
$$

---

### $P(X=3)$

$$
P(X=3)
=

\frac{\binom{4}{3}\binom{6}{2}}{\binom{10}{5}}.
$$

$$
\binom{4}{3}=4.
$$

$$
\binom{6}{2}=15.
$$

Therefore,

$$
P(X=3)
=
\frac{4 \cdot 15}{252}
=
\frac{60}{252}
\approx 0.2381.
$$

---

### $P(X=4)$

$$
P(X=4)
=

\frac{\binom{4}{4}\binom{6}{1}}{\binom{10}{5}}.
$$

$$
\binom{4}{4}=1.
$$

$$
\binom{6}{1}=6.
$$

Therefore,

$$
P(X=4)
=
\frac{1 \cdot 6}{252}
=
\frac{6}{252}
\approx 0.0238.
$$

---

## PMF Table for $n=5$

| $x$ | $P(X=x)$ |
| --: | -------: |
|   0 | $0.0238$ |
|   1 | $0.2381$ |
|   2 | $0.4762$ |
|   3 | $0.2381$ |
|   4 | $0.0238$ |

When the sample size increases from 3 to 5, the distribution moves to the right.

This is because selecting more balls increases the expected number of red balls.

For $n=3$:

$$
E(X)
=
n \cdot \frac{K}{N}
=
3 \cdot \frac{4}{10}
=
1.2.
$$

For $n=5$:

$$
E(X)
=
n \cdot \frac{K}{N}
=
5 \cdot \frac{4}{10}
=
\frac{20}{10}
=
2.
$$

So when the sample size increases, the average number of red balls also increases.

---
## 5.2. Effect of Changing the Number of Distinguished Objects

Now we keep the total number of balls and the sample size the same, but we increase the number of red balls.

Suppose:

$$
N=10,
$$

$$
K=7,
$$

and

$$
n=3.
$$

So there are 7 red balls and 3 white balls.

The PMF is:

$$
P(X=k)
=
\frac{\binom{7}{k}\binom{3}{3-k}}{\binom{10}{3}}.
$$

The denominator is still:

$$
\binom{10}{3}=120.
$$

---

## PMF for $K=7$

### $P(X=0)$

$$
P(X=0)
=
\frac{\binom{7}{0}\binom{3}{3}}{\binom{10}{3}}.
$$

$$
\binom{7}{0}=1.
$$

$$
\binom{3}{3}=1.
$$

Therefore,

$$
P(X=0)
=
\frac{1 \cdot 1}{120}
=
\frac{1}{120}
\approx 0.0083.
$$

---

### $P(X=1)$

$$
P(X=1)
=
\frac{\binom{7}{1}\binom{3}{2}}{\binom{10}{3}}.
$$

$$
\binom{7}{1}=7.
$$

$$
\binom{3}{2}=3.
$$

Therefore,

$$
P(X=1)
=
\frac{7 \cdot 3}{120}
=
\frac{21}{120}
=
0.175.
$$

---

### $P(X=2)$

$$
P(X=2)
=
\frac{\binom{7}{2}\binom{3}{1}}{\binom{10}{3}}.
$$

Calculate:

$$
\binom{7}{2}
=
\frac{7 \cdot 6}{2 \cdot 1}
=
\frac{42}{2}
=
21.
$$

Also,

$$
\binom{3}{1}=3.
$$

Therefore,

$$
P(X=2)
=
\frac{21 \cdot 3}{120}
=
\frac{63}{120}
=
0.525.
$$

---

### $P(X=3)$

$$
P(X=3)
=
\frac{\binom{7}{3}\binom{3}{0}}{\binom{10}{3}}.
$$

Calculate:

$$
\binom{7}{3}
=
\frac{7 \cdot 6 \cdot 5}{3 \cdot 2 \cdot 1}.
$$

The numerator is:

$$
7 \cdot 6 \cdot 5 = 210.
$$

The denominator is:

$$
3 \cdot 2 \cdot 1 = 6.
$$

Therefore,

$$
\binom{7}{3}
=
\frac{210}{6}
=
35.
$$

Also,

$$
\binom{3}{0}=1.
$$

Therefore,

$$
P(X=3)
=
\frac{35 \cdot 1}{120}
=
\frac{35}{120}
\approx 0.2917.
$$

---

## PMF Table for $K=7$

| $x$ | $P(X=x)$ |
|---:|---:|
| 0 | $0.0083$ |
| 1 | $0.1750$ |
| 2 | $0.5250$ |
| 3 | $0.2917$ |

When the number of red balls increases from 4 to 7, the distribution shifts to the right.

This is because red balls become more common in the population.

For $K=4$:

$$
E(X)
=
3 \cdot \frac{4}{10}
=
\frac{12}{10}
=
1.2.
$$

For $K=7$:

$$
E(X)
=
3 \cdot \frac{7}{10}
=
\frac{21}{10}
=
2.1.
$$

So increasing the number of distinguished objects increases the expected value of $X$.

---

# 6. Computing Probabilities

Now we compute probabilities such as:

$$
P(X=k),
$$

$$
P(X \leq k),
$$

$$
P(X \geq k),
$$

and

$$
P(a \leq X \leq b).
$$

We use the original example:

$$
N=10,
$$

$$
K=4,
$$

$$
n=3.
$$

The PMF values are:

$$
P(X=0)=\frac{20}{120}=0.1667,
$$

$$
P(X=1)=\frac{60}{120}=0.5000,
$$

$$
P(X=2)=\frac{36}{120}=0.3000,
$$

$$
P(X=3)=\frac{4}{120}=0.0333.
$$

---

## 6.1. Computing $P(X=k)$

Example:

$$
P(X=2).
$$

This means selecting exactly 2 red balls.

We need:

$$
2 \text{ red balls}
$$

and

$$
1 \text{ white ball}.
$$

So,

$$
P(X=2)
=
\frac{\binom{4}{2}\binom{6}{1}}{\binom{10}{3}}.
$$

Now calculate:

$$
\binom{4}{2}=6,
$$

$$
\binom{6}{1}=6,
$$

and

$$
\binom{10}{3}=120.
$$

Therefore,

$$
P(X=2)
=
\frac{6 \cdot 6}{120}
=
\frac{36}{120}
=
0.3.
$$

So,

$$
P(X=2)=0.3.
$$

---

## 6.2. Computing $P(X \leq k)$

Example:

$$
P(X \leq 1).
$$

This means selecting at most 1 red ball.

So the possible values are:

$$
X=0
$$

or

$$
X=1.
$$

Therefore,

$$
P(X \leq 1)
=
P(X=0)+P(X=1).
$$

Substitute:

$$
P(X \leq 1)
=
\frac{20}{120}
+
\frac{60}{120}.
$$

Add:

$$
P(X \leq 1)
=
\frac{80}{120}.
$$

Simplify:

$$
P(X \leq 1)
=
\frac{2}{3}.
$$

Decimal form:

$$
P(X \leq 1)
\approx 0.6667.
$$

---

## 6.3. Computing $P(X \geq k)$

Example:

$$
P(X \geq 2).
$$

This means selecting at least 2 red balls.

So the possible values are:

$$
X=2
$$

or

$$
X=3.
$$

Therefore,

$$
P(X \geq 2)
=
P(X=2)+P(X=3).
$$

Substitute:

$$
P(X \geq 2)
=
\frac{36}{120}
+
\frac{4}{120}.
$$

Add:

$$
P(X \geq 2)
=
\frac{40}{120}.
$$

Simplify:

$$
P(X \geq 2)
=
\frac{1}{3}.
$$

Decimal form:

$$
P(X \geq 2)
\approx 0.3333.
$$

---

## 6.4. Computing $P(a \leq X \leq b)$

Example:

$$
P(1 \leq X \leq 2).
$$

This means selecting either 1 red ball or 2 red balls.

So,

$$
P(1 \leq X \leq 2)
=
P(X=1)+P(X=2).
$$

Substitute:

$$
P(1 \leq X \leq 2)
=
\frac{60}{120}
+
\frac{36}{120}.
$$

Add:

$$
P(1 \leq X \leq 2)
=
\frac{96}{120}.
$$

Simplify:

$$
P(1 \leq X \leq 2)
=
0.8.
$$

Therefore,

$$
P(1 \leq X \leq 2)=0.8.
$$

---

# 7. Comparison with the Binomial Model

The hypergeometric model and the binomial model are similar because both count the number of successes in a sample.

However, the main difference is replacement.

The hypergeometric distribution is used when sampling is done without replacement.

The binomial distribution is used when trials are independent and the probability of success is constant.

---

## Hypergeometric Model

In the hypergeometric model:

* We sample without replacement.
* The population is finite.
* The probability changes after each selection.
* The trials are dependent.

For example, if we select a red ball first and do not put it back, then the number of red balls decreases from 4 to 3.

So the probability of getting a red ball on the next draw changes.

---

## Binomial Model

In the binomial model:

* Trials are independent.
* The probability of success stays constant.
* It is like sampling with replacement.

In our example, the probability of selecting a red ball at the beginning is:

$$
p=\frac{4}{10}=0.4.
$$

If we used a binomial approximation, we would assume that this probability stays constant for all 3 selections.

Let

$$
Y = \text{the number of red balls in 3 independent trials}.
$$

Then,

$$
Y \sim \text{Binomial}(3,0.4).
$$

The binomial PMF is:

$$
P(Y=k)
=
\binom{3}{k}(0.4)^k(0.6)^{3-k}.
$$

---

## Binomial Calculations

### $P(Y=0)$

$$
P(Y=0)
=
\binom{3}{0}(0.4)^0(0.6)^3.
$$

Now,

$$
\binom{3}{0}=1,
$$

$$
(0.4)^0=1,
$$

and

$$
(0.6)^3=0.6 \cdot 0.6 \cdot 0.6=0.216.
$$

Therefore,

$$
P(Y=0)=1 \cdot 1 \cdot 0.216=0.216.
$$

---

### $P(Y=1)$

$$
P(Y=1)
=
\binom{3}{1}(0.4)^1(0.6)^2.
$$

Now,

$$
\binom{3}{1}=3,
$$

$$
(0.4)^1=0.4,
$$

and

$$
(0.6)^2=0.36.
$$

Therefore,

$$
P(Y=1)=3 \cdot 0.4 \cdot 0.36.
$$

First,

$$
3 \cdot 0.4=1.2.
$$

Then,

$$
1.2 \cdot 0.36=0.432.
$$

So,

$$
P(Y=1)=0.432.
$$

---

### $P(Y=2)$

$$
P(Y=2)
=
\binom{3}{2}(0.4)^2(0.6)^1.
$$

Now,

$$
\binom{3}{2}=3,
$$

$$
(0.4)^2=0.16,
$$

and

$$
(0.6)^1=0.6.
$$

Therefore,

$$
P(Y=2)=3 \cdot 0.16 \cdot 0.6.
$$

First,

$$
3 \cdot 0.16=0.48.
$$

Then,

$$
0.48 \cdot 0.6=0.288.
$$

So,

$$
P(Y=2)=0.288.
$$

---

### $P(Y=3)$

$$
P(Y=3)
=
\binom{3}{3}(0.4)^3(0.6)^0.
$$

Now,

$$
\binom{3}{3}=1,
$$

$$
(0.4)^3=0.4 \cdot 0.4 \cdot 0.4=0.064,
$$

and

$$
(0.6)^0=1.
$$

Therefore,

$$
P(Y=3)=1 \cdot 0.064 \cdot 1=0.064.
$$

---

## Comparison Table

| Number of red balls | Hypergeometric | Binomial |
|---:|---:|---:|
| 0 | $0.1667$ | $0.2160$ |
| 1 | $0.5000$ | $0.4320$ |
| 2 | $0.3000$ | $0.2880$ |
| 3 | $0.0333$ | $0.0640$ |

The results are similar, but they are not exactly the same.

The hypergeometric model is more accurate here because the balls are selected without replacement.

The binomial model assumes a constant probability of red on each draw, but in the real experiment the probability changes after every draw.

---

# 8. Practical Applications of the Hypergeometric Model

The hypergeometric distribution is useful when we select a sample from a finite population without replacement.

---

## Application 1: Quality Control

Suppose a factory produces 100 items.

Some of these items are defective.

A quality inspector randomly selects 10 items without replacement.

Let

$$
X = \text{the number of defective items in the sample}.
$$

This is a hypergeometric situation because the selected items are not returned to the population.

---

## Application 2: Card Drawing

Suppose a standard deck has 52 cards.

There are 13 hearts.

We draw 5 cards without replacement.

Let

$$
X = \text{the number of hearts among the 5 selected cards}.
$$

This follows a hypergeometric distribution.

---

## Application 3: Student Selection

Suppose a class has 30 students.

8 students passed an exam.

We randomly select 5 students without replacement.

Let

$$
X = \text{the number of students who passed among the selected students}.
$$

This can be modeled using a hypergeometric distribution.

---

## Application 4: Survey Sampling

Suppose a city has a fixed number of voters.

Some voters support a certain candidate.

A sample of voters is selected without replacement.

Let

$$
X = \text{the number of supporters in the sample}.
$$

This is also a hypergeometric model.

---

# 9. Application and Comparison with a Similar Binomial Model

Now we use the red-ball example as a quality control application.

Suppose the box contains 10 products.

Among them, 4 products are defective.

The defective products correspond to red balls.

The non-defective products correspond to white balls.

We randomly select 3 products for inspection without replacement.

Let

$$
X = \text{the number of defective products in the sample}.
$$

Then,

$$
X \sim \text{Hypergeometric}(N=10,K=4,n=3).
$$

The hypergeometric probabilities are:

| $x$ | $P(X=x)$ |
|---:|---:|
| 0 | $0.1667$ |
| 1 | $0.5000$ |
| 2 | $0.3000$ |
| 3 | $0.0333$ |

This is the correct model because the selected products are not returned to the population.

Now compare it with a binomial model.

The probability that one randomly selected product is defective is:

$$
p=\frac{4}{10}=0.4.
$$

If we incorrectly assume that each selection is independent, then we can use:

$$
Y \sim \text{Binomial}(3,0.4).
$$

The binomial probabilities are:

| $y$ | $P(Y=y)$ |
|---:|---:|
| 0 | $0.2160$ |
| 1 | $0.4320$ |
| 2 | $0.2880$ |
| 3 | $0.0640$ |

The binomial model is only an approximation here.

The hypergeometric model is better because the sample is selected without replacement.

If the population were very large and the sample size were very small, then the binomial model would be a good approximation.

For example, selecting 3 products from 10 products changes the population noticeably.

But selecting 3 products from 10,000 products does not change the population much.

Therefore, for large populations and small samples, the binomial approximation becomes more accurate.

---

# Final Summary

The hypergeometric distribution is used when we sample without replacement from a finite population.

In our example, we have:

$$
N=10,
$$

$$
K=4,
$$

$$
n=3.
$$

There are 10 balls in total, 4 of them are red, and we select 3 balls without replacement.

The random variable is:

$$
X = \text{the number of red balls in the sample}.
$$

The PMF is:

$$
P(X=k)
=
\frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}.
$$

For our example:

$$
P(X=k)
=
\frac{\binom{4}{k}\binom{6}{3-k}}{\binom{10}{3}}.
$$

The support is:

$$
X \in \{0,1,2,3\}.
$$

The PMF values are:

$$
P(X=0)=0.1667,
$$

$$
P(X=1)=0.5000,
$$

$$
P(X=2)=0.3000,
$$

$$
P(X=3)=0.0333.
$$

The CDF values are:

$$
P(X \leq 0)=0.1667,
$$

$$
P(X \leq 1)=0.6667,
$$

$$
P(X \leq 2)=0.9667,
$$

$$
P(X \leq 3)=1.
$$

The hypergeometric model differs from the binomial model because hypergeometric sampling is without replacement, while binomial sampling assumes independent trials with a constant probability.