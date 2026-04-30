
# Problem 6 — Axiomatic point of view (Kolmogorov framework)

---

## 1. Goal of probability theory

In previous problems we worked with:

* finite outcomes
* frequencies
* empirical ratios

Now we switch perspective:

> We no longer describe experiments — we define a mathematical system that *models them*.

---

# 2. Probability space

We define a probability model as:

$$
(\Omega, \mathcal{F}, P)
$$

---

## Meaning of each component

### 1. Sample space

$$
\Omega
$$

This is the set of all possible outcomes.

Example:

$$
\Omega = {1,2,3,4,5,6}
$$

---

### 2. Event space (sigma-algebra)

$$
\mathcal{F}
$$

This is not “all subsets automatically”.

It is a **structured collection of events**.

---

### WHY do we need 𝓕?

Because in advanced probability:

* not every subset must be measurable
* we need closure rules to avoid contradictions

So we require:

### Properties of 𝓕:

1. ( \Omega \in \mathcal{F} )
2. If (A \in \mathcal{F}), then (A^c \in \mathcal{F})
3. If (A_1, A_2, ... \in \mathcal{F}), then
   ( \bigcup_{i} A_i \in \mathcal{F} )

---

### Intuition

𝓕 = “allowed events we can assign probability to”

---

### 3. Probability function

$$
P : \mathcal{F} \to [0,1]
$$

This assigns a number to each event.

---

# 3. Kolmogorov axioms

---

## Axiom 1 — Non-negativity

$$
P(A) \ge 0
$$

### WHY?

Because probability comes from frequency:

$$
\frac{n(A)}{N} \ge 0
$$

Counts can never be negative.

---

## Axiom 2 — Normalization

$$
P(\Omega) = 1
$$

### WHY?

Because:

* Ω contains every possible outcome
* something must happen in every trial

So total probability = 100%

---

## Axiom 3 — Countable additivity

If:

$$
A_i \cap A_j = \emptyset \quad (i \ne j)
$$

then:

$$
P\left(\bigcup_{i=1}^{\infty} A_i\right)
========================================

\sum_{i=1}^{\infty} P(A_i)
$$

---

# 4. Why this axiom is the deepest one

This is the key conceptual jump.

---

## Finite version (what we already saw)

$$
P(A \cup B) = P(A) + P(B)
$$

works when sets are disjoint.

---

## But Kolmogorov extends it to:

* infinitely many sets
* infinite decompositions

---

## WHY this is non-trivial

Because:

* experiments are always finite
* we never observe infinite unions directly
* limits are required

So this axiom is a **theoretical extension**, not empirical fact.

---

# 5. Why these axioms naturally appear

---

## (1) From frequencies

We observed:

* values always between 0 and 1
* total always sums to 1
* disjoint events add up correctly

So:

| Empirical fact          | Axiom          |
| ----------------------- | -------------- |
| relative frequency ≥ 0  | non-negativity |
| total outcomes = 1      | normalization  |
| no overlap → add counts | additivity     |

---

## 6. Complement rule (derived, not axiomatic)

From axioms we get:

$$
P(A^c) = 1 - P(A)
$$

### Proof idea:

We know:

$$
A \cup A^c = \Omega
$$

and:

$$
A \cap A^c = \emptyset
$$

So:

$$
P(A) + P(A^c) = P(\Omega) = 1
$$

---

# 7. What is fundamentally new compared to finite problems?

---

## In earlier problems:

* Ω was finite
* everything was counting
* additivity was finite only

---

## Now:

We introduce:

### 1. Infinite structures

Example:

* real-valued outcomes
* continuous distributions

---

### 2. σ-algebra restriction

Not all subsets are allowed

WHY?

Because:

* some sets are too “wild” to assign consistent probability
* measure theory avoids contradictions

---

### 3. Countable additivity

This is essential for:

* limits
* convergence
* continuous probability (normal distribution etc.)

---

# 8. Conceptual bridge

---

## Step 1 — Finite world (your earlier problems)

* count outcomes
* compute frequencies
* simple addition works

---

## Step 2 — Empirical abstraction

* frequency stabilizes
* we define probability function P

---

## Step 3 — Axiomatic system

We no longer compute — we DEFINE:

$$
(\Omega, \mathcal{F}, P)
$$

---

## FINAL STRUCTURE

Probability theory becomes:

> a consistent extension of finite counting to infinite mathematical structures

---

# 9. Final summary (core insight)

---

* Non-negativity → comes from counts
* Normalization → comes from “something must happen”
* Finite additivity → comes from disjoint counting
* Countable additivity → is the leap to infinite mathematics
