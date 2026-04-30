# Task 8 — Beta Distribution

---

## 0. Experiment setup (continuous probability space)

---

We consider a continuous random experiment on:

$$
\Omega = [0,1]
$$

An elementary outcome is:

$$
\omega \in [0,1]
$$

---

## Random variable definition

We define:

$$
X(\omega)=\omega
$$

---

## WHY this setup?

Because beta distribution models:

> uncertainty about a probability itself

So instead of counting events, we model a value in ([0,1]).

---

# 1. Beta distribution PDF

---

## Parameters

We define:

$$
\alpha > 0,\quad \beta > 0
$$

---

## PDF formula

$$
f(x)=\frac{1}{B(\alpha,\beta)} x^{\alpha-1}(1-x)^{\beta-1}, \quad 0 \le x \le 1
$$

---

## Normalization constant

$$
B(\alpha,\beta)=\int_0^1 x^{\alpha-1}(1-x)^{\beta-1} dx
$$

---

## WHY this is needed

We need:

$$
\int_0^1 f(x),dx = 1
$$

So (B(\alpha,\beta)) ensures total probability = 1.

---

# 2. Support

---

$$
X \in [0,1]
$$

---

## WHY this interval?

Because beta distribution models:

> proportions, probabilities, percentages

---

# 3. Shape analysis of PDF

---

## Key idea

Shape depends on:

* (x^{\alpha-1}) → controls behavior near 0
* ((1-x)^{\beta-1}) → controls behavior near 1

---

## Case 1 — symmetric

$$
\alpha = \beta
$$

Result:

* symmetric around 0.5

Example:

* (\alpha=\beta=2)

---

## Case 2 — skewed right

$$
\alpha < \beta
$$

Result:

* mass near 0
* tail toward 1

---

## Case 3 — skewed left

$$
\alpha > \beta
$$

Result:

* mass near 1
* tail toward 0

---

## Case 4 — U-shaped

$$
\alpha < 1,\ \beta < 1
$$

Result:

* high probability near 0 and 1
* low in middle

---

## Case 5 — bell-shaped

$$
\alpha > 1,\ \beta > 1
$$

Result:

* peak inside (0,1)

---

# 4. CDF of Beta distribution

---

## Definition

$$
F(x)=P(X \le x)=\int_0^x f(t),dt
$$

---

## Explicit form

$$
F(x)=\frac{1}{B(\alpha,\beta)}\int_0^x t^{\alpha-1}(1-t)^{\beta-1} dt
$$

---

## WHY no closed simple form?

Because:

* integral is not elementary in general
* depends on incomplete beta function

---

# 5. Role of parameters in CDF

---

## Increasing α

* faster growth near 1
* shifts distribution right

---

## Increasing β

* slower growth near 1
* shifts distribution left

---

## Intuition

CDF always:

* starts at 0
* ends at 1
* smooth increasing curve

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

## WHY subtraction works

Because:

$$
F(b) = \int_0^b f(x),dx
$$

so:

$$
F(b)-F(a)=\int_a^b f(x),dx
$$

---

# 7. Why probabilities = areas

---

## Key principle

In continuous distributions:

$$
P(X=a)=0
$$

---

## WHY?

Because:

* single points have zero width
* integral over a point = 0

---

## So probability is:

> area under curve, not height

---

# 8. Applications of Beta distribution

---

## 1. Bayesian statistics

* models prior belief about probabilities

Example:

* probability of success of a model

---

## 2. Machine learning

* uncertainty in classification accuracy

---

## 3. A/B testing

* click-through rates

---

## 4. Reliability engineering

* failure probabilities

---

## Core idea:

Beta models:

> uncertainty about probabilities themselves

---

# FINAL SUMMARY

---

We built:

### 1. Experiment

* continuous variable on [0,1]

### 2. Random variable

* identity mapping X(ω)=ω

### 3. PDF

$$
f(x)=\frac{1}{B(\alpha,\beta)}x^{\alpha-1}(1-x)^{\beta-1}
$$

### 4. CDF

* integral of PDF (incomplete beta function)

