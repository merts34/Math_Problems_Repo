# Task 9 — Gamma Distribution

---

## 0. Experiment description (waiting time model)

---

We consider a continuous-time process where:

* events happen randomly over time
* the process has a constant average rate
* events are independent in time

Typical examples:

* arrival of customers
* radioactive decay
* time until system failures

---

## Sample space

We define:

$$
\Omega = [0,\infty)
$$

---

## Random variable

We define:

$$
X(\omega)=\omega
$$

meaning:

> waiting time until a certain event occurs

---

## WHY this model exists

Gamma distribution generalizes:

* exponential distribution (waiting time for 1 event)
* Poisson process timing structure

---

# 1. Gamma PDF

---

## Parameters

We define:

* shape: (\alpha > 0)
* rate: (\beta > 0)

---

## PDF formula

$$
f(x)=\frac{\beta^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\beta x}, \quad x \ge 0
$$

---

## Special function

$$
\Gamma(\alpha)=\int_0^\infty x^{\alpha-1} e^{-x} dx
$$

---

## WHY Gamma function appears

Because it generalizes factorial:

$$
\Gamma(n)=(n-1)! \quad \text{for integers}
$$

---

# 2. Support

---

$$
X \in [0,\infty)
$$

---

## WHY infinite?

Because:

> waiting time can grow arbitrarily large

---

# 3. Shape behavior (PDF intuition)

---

## Key structure

Gamma PDF is:

$$
x^{\alpha-1} e^{-\beta x}
$$

So two forces act:

* (x^{\alpha-1}) → increases near 0 (if α>1)
* (e^{-\beta x}) → decreases for large x

---

## Case 1 — α = 1

$$
f(x)=\beta e^{-\beta x}
$$

This is:

> exponential distribution

---

## Case 2 — α > 1

* distribution starts at 0
* rises to a peak
* then decays

---

## Case 3 — large α

* more symmetric shape
* approaches normal distribution

---

# 4. CDF of Gamma distribution

---

## Definition

$$
F(x)=P(X \le x)=\int_0^x f(t),dt
$$

---

## Explicit form

$$
F(x)=\frac{1}{\Gamma(\alpha)}\int_0^x \beta^\alpha t^{\alpha-1} e^{-\beta t} dt
$$

---

## WHY no simple closed form?

Because:

* integral defines incomplete gamma function

---

# 5. Shape of CDF

---

## General properties

* starts at 0
* increases smoothly
* approaches 1 as x → ∞

---

## Effect of parameters

### Increasing α

* slower initial growth
* more delayed accumulation

---

### Increasing β

* faster decay of PDF
* CDF reaches 1 faster

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

## WHY this works

Because:

$$
F(b)-F(a)=\int_a^b f(x),dx
$$

---

# 7. Connection to exponential distribution

---

## Key fact

If:

$$
\alpha = 1
$$

then:

$$
Gamma(\alpha,\beta) = Exponential(\beta)
$$

---

## Interpretation

* exponential → waiting for 1 event
* gamma → waiting for α events

---

# 8. Connection to Poisson process

---

If events follow a Poisson process:

* number of events in time interval → Poisson
* waiting time between events → Exponential
* waiting time until r-th event → Gamma

---

## Key link:

| Concept              | Distribution |
| -------------------- | ------------ |
| event count          | Poisson      |
| waiting for 1 event  | Exponential  |
| waiting for r events | Gamma        |

---

# 9. Applications

---

## 1. Queueing systems

* waiting time for service completion

---

## 2. Reliability engineering

* lifetime of systems

---

## 3. Biology

* time until multiple reactions occur

---

## 4. Finance

* aggregated time-to-event modeling

---

## Core idea:

Gamma models:

> accumulated waiting time for multiple random events

---

# FINAL SUMMARY

---

We built:

### 1. Experiment

* continuous waiting time process

### 2. Random variable

* time until event accumulation

### 3. PDF

$$
f(x)=\frac{\beta^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\beta x}
$$

### 4. CDF

* integral of PDF (incomplete gamma function)

