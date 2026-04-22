# Task 4 — Poisson Model (Arrival of Events)

---

## 1. Description of the Random Experiment

We observe a web service that receives error reports over time.

We are told:

* On average, **3 error reports per hour** occur.

We model:

$$
X = \text{number of error reports in 1 hour}
$$

---

## 2. Key Assumptions of the Model

The Poisson model assumes:

1. Events occur independently
2. Events occur randomly in time
3. Average rate is constant
4. Two events do not occur at exactly the same instant (idealization)

---

## 3. Sample Space $\Omega$

The number of events can be:

$$
\Omega = {0,1,2,3,4,5,\dots}
$$

So:

$$
X \in \mathbb{N}_0
$$

---

## 4. Parameter Interpretation

We are given:

$$
\lambda = 3
$$

Meaning:

* average number of events per hour = 3

So:

$$
\lambda = \text{expected value per interval}
$$

---

## 5. Poisson Distribution Formula

The probability of observing exactly $k$ events is:

$$
P(X = k) = \frac{e^{-\lambda} \lambda^k}{k!}
$$

---

## 6. Step-by-step Meaning of Each Term

### 1. Exponential term

$$
e^{-\lambda}
$$

This represents:

* probability of "no events baseline adjustment"

---

### 2. Rate term

$$
\lambda^k
$$

This increases probability as expected events increase.

---

### 3. Factorial term

$$
k!
$$

This corrects for ordering of events (since order does not matter).

---

## 7. Plugging in Our Value $\lambda = 3$

We substitute:

$$
P(X = k) = \frac{e^{-3} \cdot 3^k}{k!}
$$

---

## 8. Example Expansions (Step-by-step)

---

### Case $k = 0$

$$
P(X=0) = \frac{e^{-3} \cdot 3^0}{0!}
$$

Now compute step-by-step:

$$
3^0 = 1
$$

$$
0! = 1
$$

So:

$$
P(X=0) = e^{-3}
$$

---

### Case $k = 1$

$$
P(X=1) = \frac{e^{-3} \cdot 3^1}{1!}
$$

Compute:

$$
3^1 = 3
$$

$$
1! = 1
$$

So:

$$
P(X=1) = 3e^{-3}
$$

---

### Case $k = 2$

$$
P(X=2) = \frac{e^{-3} \cdot 3^2}{2!}
$$

Compute step-by-step:

$$
3^2 = 9
$$

$$
2! = 2 \cdot 1 = 2
$$

So:

$$
P(X=2) = \frac{9e^{-3}}{2}
$$

---

## 9. Meaning of the Model

Poisson distribution models:

* number of events in fixed time interval
* without tracking individual trials
* only the rate matters

---

## 10. Success Definition

In this context:

$$
\text{Success} = \text{one error report occurring}
$$

---

## 11. Key Intuition

Unlike binomial/geometric:

* no fixed number of trials
* no "success/failure sequence"
* only event rate matters

---

## 12. Final Formula

$$
P(X = k) = \frac{e^{-3} \cdot 3^k}{k!}
$$

---

