# Task 5 — Multinomial Model (Categories of Outcomes)

---

## 1. Description of the Random Experiment

We roll a fair die **5 times**.

Each roll results in one of 6 outcomes:

$$
{1,2,3,4,5,6}
$$

We group outcomes into 3 categories:

* Small: ( {1,2} )
* Medium: ( {3,4} )
* Large: ( {5,6} )

---

## 2. Define the Probabilities of Each Category

Since the die is fair:

### Small (1–2)

$$
P(S) = \frac{2}{6} = \frac{1}{3}
$$

### Medium (3–4)

$$
P(M) = \frac{2}{6} = \frac{1}{3}
$$

### Large (5–6)

$$
P(L) = \frac{2}{6} = \frac{1}{3}
$$

So:

$$
P(S) = P(M) = P(L) = \frac{1}{3}
$$

---

## 3. Define the Random Variables

Let:

$$
X_1 = \text{number of small outcomes in 5 rolls}
$$

$$
X_2 = \text{number of medium outcomes in 5 rolls}
$$

$$
X_3 = \text{number of large outcomes in 5 rolls}
$$

Constraint:

$$
X_1 + X_2 + X_3 = 5
$$

---

## 4. Sample Space Idea

Each roll has 3 possible categories:

So each sequence is a length-5 sequence like:

* S M L S M
* L L S M S
* etc.

We do NOT list all explicitly because it is large:

$$
3^5 = 243 \text{ outcomes}
$$

---

## 5. Multinomial Distribution Formula

The probability of a specific count combination is:

$$
P(X_1 = x_1, X_2 = x_2, X_3 = x_3)
= \frac{5!}{x_1! x_2! x_3!}
\cdot p_S^{x_1} \cdot p_M^{x_2} \cdot p_L^{x_3}
$$

---

## 6. Interpretation of Each Part

### Step 1: Permutation factor

$$
\frac{5!}{x_1! x_2! x_3!}
$$

This counts how many different sequences produce the same result.

---

### Step 2: Probability part

$$
p_S^{x_1} \cdot p_M^{x_2} \cdot p_L^{x_3}
$$

Each outcome contributes its probability.

---

## 7. Plug in probabilities

Since:

$$
p_S = p_M = p_L = \frac{1}{3}
$$

We get:

$$
P = \frac{5!}{x_1! x_2! x_3!} \left(\frac{1}{3}\right)^{x_1}
\left(\frac{1}{3}\right)^{x_2}
\left(\frac{1}{3}\right)^{x_3}
$$

---

## 8. Simplification

Since:

$$
x_1 + x_2 + x_3 = 5
$$

We combine powers:

$$
\left(\frac{1}{3}\right)^{x_1 + x_2 + x_3}
= \left(\frac{1}{3}\right)^5
$$

So final simplified formula:

$$
P(X_1, X_2, X_3)
= \frac{5!}{x_1! x_2! x_3!}
\cdot \left(\frac{1}{3}\right)^5
$$

---

## 9. Success Interpretation

A “success” depends on category:

* success is not binary anymore
* we have multiple outcomes per trial

So:

* Success = landing in a specific category (S, M, or L)

---

## 10. Key Concept

This is a generalization of binomial:

* Binomial → 2 outcomes
* Multinomial → 3 or more outcomes

---

## 11. Final Model

$$
(X_1, X_2, X_3) \sim \text{Multinomial}(n=5, p_1=\tfrac{1}{3}, p_2=\tfrac{1}{3}, p_3=\tfrac{1}{3})
$$

---

