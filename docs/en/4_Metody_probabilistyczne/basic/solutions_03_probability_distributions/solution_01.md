


# Task 1 — Binomial Model (Quality Control)

---

## 1. Description of the Random Experiment

We inspect 3 screws one after another.

Each screw can be:

* $G = \text{good}$
* $D = \text{defective}$

Let:

$$
P(D) = p, \quad P(G) = 1 - p
$$

Each trial is independent.

---

## 2. Sample Space $\Omega$

Each screw has 2 possible outcomes, so:

$$
2 \times 2 \times 2 = 8
$$

Therefore:

$$
\Omega = { GGG, GGD, GDG, GDD, DGG, DGD, DDG, DDD }
$$

---

## 3. Probability of Each Outcome (Step-by-step expansion)

---

### Case 1: $P(GGG)$

$$
P(GGG) = P(G)\cdot P(G)\cdot P(G)
$$

Substitute:

$$
= (1 - p)(1 - p)(1 - p)
$$

First multiply first two terms:

$$
(1 - p)(1 - p) = 1 - p - p + p^2
$$

$$
= 1 - 2p + p^2
$$

Now multiply with third term:

$$
(1 - 2p + p^2)(1 - p)
$$

Expand:

$$
= 1(1 - p) - 2p(1 - p) + p^2(1 - p)
$$

Now expand each term:

$$
= (1 - p) - (2p - 2p^2) + (p^2 - p^3)
$$

Combine:

$$
= 1 - p - 2p + 2p^2 + p^2 - p^3
$$

Final result:

$$
P(GGG) = 1 - 3p + 3p^2 - p^3
$$

---

### Case 2: $P(GGD)$

$$
P(GGD) = (1 - p)(1 - p)p
$$

First:

$$
(1 - p)(1 - p) = 1 - 2p + p^2
$$

Now multiply:

$$
(1 - 2p + p^2)p
$$

Expand:

$$
= p - 2p^2 + p^3
$$

---

### Case 3: $P(GDG)$

$$
P(GDG) = (1 - p)p(1 - p)
$$

First:

$$
(1 - p)p = p - p^2
$$

Now:

$$
(p - p^2)(1 - p)
$$

Expand:

$$
= p(1 - p) - p^2(1 - p)
$$

$$
= (p - p^2) - (p^2 - p^3)
$$

Final:

$$
P(GDG) = p - 2p^2 + p^3
$$

---

### Case 4: $P(GDD)$

$$
P(GDD) = (1 - p)p p
$$

$$
= (1 - p)p^2
$$

Expand:

$$
= p^2 - p^3
$$

---

### Case 5: $P(DGG)$

$$
P(DGG) = p(1 - p)(1 - p)
$$

First:

$$
(1 - p)(1 - p) = 1 - 2p + p^2
$$

Now:

$$
p(1 - 2p + p^2)
$$

Expand:

$$
= p - 2p^2 + p^3
$$

---

### Case 6: $P(DGD)$

$$
P(DGD) = p(1 - p)p
$$

First:

$$
p(1 - p) = p - p^2
$$

Now:

$$
(p - p^2)p
$$

Expand:

$$
= p^2 - p^3
$$

---

### Case 7: $P(DDG)$

$$
P(DDG) = p p (1 - p)
$$

$$
= p^2(1 - p)
$$

Expand:

$$
= p^2 - p^3
$$

---

### Case 8: $P(DDD)$

$$
P(DDD) = p \cdot p \cdot p = p^3
$$

---

## 4. Definition of Success

A success is defined as:

$$
\text{Success} = D \quad (\text{defective screw})
$$

---

## 5. Random Variable

Let:

$$
X = \text{number of defective screws}
$$

Possible values:

$$
X \in {0,1,2,3}
$$

---

## 6. Grouped Probabilities

---

### $X = 0$

$$
P(X=0) = (1 - p)^3
$$

---

### $X = 1$

$$
P(X=1) = 3(p - 2p^2 + p^3)
$$

---

### $X = 2$

$$
P(X=2) = 3(p^2 - p^3)
$$

---

### $X = 3$

$$
P(X=3) = p^3
$$

---

## 7. Final Binomial Formula

$$
P(X = k) = \binom{3}{k} p^k (1 - p)^{3-k}
$$

