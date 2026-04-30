# Task 5 — Poisson Distribution

---

## 0. Experiment description (what is being modeled?)

---

We consider a situation where:

* events occur randomly over time or space
* events happen independently
* average rate is constant

Examples:

* number of emails per hour
* number of phone calls per minute
* number of accidents per day

---

## Sample space (\Omega)

We define:

$$
\Omega = {0,1,2,3,\dots}
$$

---

## WHY this sample space?

Because:

> we are counting how many events occur in a fixed interval

So outcomes are counts, not sequences.

---

## Random variable

We define:

$$
X(\omega) = \text{number of events in a fixed interval}
$$

---

# 1. Poisson PMF

---

## Key parameter

We introduce:

$$
\lambda > 0
$$

meaning:

> average number of events per interval

---

## PMF formula

$$
P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

---

## WHY this formula appears

It comes from:

* limiting case of binomial distribution
* when:

  * (n \to \infty)
  * (p \to 0)
  * (np = \lambda)

So Poisson models:

> rare events in large populations

---

# 2. Support

---

$$
X \in {0,1,2,3,\dots}
$$

---

## WHY infinite?

Because:

* there is no theoretical upper bound on event count
* rare bursts are possible

---

# 3. PMF shape behavior

---

## Effect of (\lambda)

### Small (\lambda)

* mass concentrated near 0
* rare events dominate

### Large (\lambda)

* distribution shifts right
* becomes more symmetric

---

## Key insight

As (\lambda) increases:

> Poisson starts resembling a normal distribution

---

# 4. CDF of Poisson

---

## Definition

$$
F(k) = P(X \le k)
$$

---

## Formula

$$
F(k)=\sum_{i=0}^{k} \frac{\lambda^i e^{-\lambda}}{i!}
$$

---

## WHY summation?

Because Poisson is discrete:

> CDF = cumulative sum of PMF

---

# 5. Shape of CDF

---

## Properties

* starts at 0
* increases step-by-step
* approaches 1 as k → ∞

---

## Effect of λ

### Small λ:

* fast rise near 0

### Large λ:

* slower rise
* wider spread

---

# 6. Probability computations

---

## 1. Exact probability

$$
P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

---

## 2. Cumulative probability

$$
P(X \le k) = F(k)
$$

---

## 3. Right tail

$$
P(X \ge k)
$$

We use complement:

$$
P(X \ge k)=1-P(X \le k-1)
$$

---

## 4. Interval probability

$$
P(a \le X \le b)=F(b)-F(a-1)
$$

---

# 7. Why Poisson is special

---

## Key property: additivity of rates

If:

* (X_1 \sim Poisson(\lambda_1))
* (X_2 \sim Poisson(\lambda_2))

then:

$$
X_1 + X_2 \sim Poisson(\lambda_1 + \lambda_2)
$$

---

## WHY important?

Because:

> independent event sources combine naturally

Example:

* calls from two different systems

---

# 8. Comparison with binomial

---

## Binomial:

* fixed number of trials (n)
* success probability (p)

---

## Poisson:

* no fixed trials
* only rate (\lambda)

---

## Connection:

$$
Bin(n,p) \approx Poisson(\lambda)
$$

when:

$$
n \to \infty,\quad p \to 0,\quad np=\lambda
$$

---

# 9. Applications

---

## 1. Queue systems

* customers arriving

---

## 2. Biology

* mutation occurrences

---

## 3. Network traffic

* packet arrivals

---

## 4. Insurance

* claim counts

---

## Core idea:

Poisson models:

> random count of rare independent events over time

---

# FINAL SUMMARY

---

We built:

### 1. Experiment

* counting events in fixed interval

### 2. Random variable

* number of occurrences

### 3. PMF

$$
P(X=k)=\frac{\lambda^k e^{-\lambda}}{k!}
$$

### 4. CDF

* cumulative sum of PMF

