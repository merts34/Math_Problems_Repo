# Task 10 — Normal Distribution (N(\mu,\sigma^2))

---

## 0. Experiment description (measurement model)

---

We consider a continuous measurement process:

* we observe a real-valued quantity
* the value is influenced by many small random effects
* errors are symmetric around a true mean

Examples:

* height of people
* measurement errors
* test scores
* physical quantities (noise in sensors)

---

## Sample space

We define:

$$
\Omega = \mathbb{R}
$$

---

## Random variable

We define:

$$
X(\omega)=\omega
$$

meaning:

> the observed measurement value itself

---

## WHY normal distribution is fundamental

Because many independent small effects combine to form it.

This is the idea behind:

> Central Limit Theorem (CLT)

---

# 1. PDF of Normal distribution

---

## Parameters

* mean: (\mu \in \mathbb{R})
* variance: (\sigma^2 > 0)

---

## PDF formula

$$
f(x)=\frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

---

## WHY this shape appears

Because:

* exponent penalizes distance from mean
* squared term ensures symmetry
* exponential ensures fast decay

---

# 2. Support

---

$$
X \in \mathbb{R}
$$

---

## WHY full real line?

Because:

> measurement noise can theoretically take any real value

---

# 3. Shape of PDF

---

## Key structure

The function:

$$
e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

creates a **bell shape**

---

## Effect of μ (mean)

### Increasing μ:

* shifts graph to the right

### Decreasing μ:

* shifts graph to the left

---

## Effect of σ² (variance)

### Small σ²:

* narrow peak
* high concentration around mean

### Large σ²:

* wider curve
* more spread

---

## Intuition

* μ = center
* σ = spread

---

# 4. CDF of Normal distribution

---

## Definition

$$
F(x)=P(X \le x)=\int_{-\infty}^{x} f(t),dt
$$

---

## Important fact

There is no elementary closed form.

So we use:

* numerical approximation
* error function

---

## Standard form

We define standard normal:

$$
Z \sim N(0,1)
$$

---

## Standardization formula

$$
Z=\frac{X-\mu}{\sigma}
$$

---

## WHY this is useful

Because:

> all normal probabilities reduce to standard normal tables

---

# 5. CDF behavior

---

## Properties

* smooth curve
* strictly increasing
* symmetric around μ

---

## Key points

$$
F(\mu)=0.5
$$

because:

> half probability lies on each side of mean

---

# 6. Probability computations

---

## 1. Left tail

$$
P(X \le a)=F(a)
$$

---

## 2. Right tail

$$
P(X \ge a)=1-F(a)
$$

---

## 3. Interval probability

$$
P(a \le X \le b)=F(b)-F(a)
$$

---

## 4. Using standardization

We convert:

$$
P(X \le a)=P\left(Z \le \frac{a-\mu}{\sigma}\right)
$$

---

## WHY standardization works

Because:

> all normal distributions are scaled versions of standard normal

---

# 7. Why (P(X=a)=0)

---

## Key idea

For continuous distributions:

$$
P(X=a)=0
$$

---

## WHY?

Because:

* probability is area under curve
* a single point has zero width
* integral over a point = 0

---

# 8. Applications of normal distribution

---

## 1. Natural phenomena

* heights
* weights
* biological traits

---

## 2. Measurement errors

* sensor noise
* experimental errors

---

## 3. Statistics

* sampling distributions
* hypothesis testing

---

## 4. Finance

* returns approximation (basic models)

---

## Core idea:

Normal distribution models:

> sum of many small independent effects

---

# FINAL SUMMARY

---

We built:

### 1. Experiment

* real-valued measurements

### 2. Random variable

* continuous outcome in ℝ

### 3. PDF

$$
f(x)=\frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
$$

### 4. CDF

* integral of PDF (no closed form)

---
