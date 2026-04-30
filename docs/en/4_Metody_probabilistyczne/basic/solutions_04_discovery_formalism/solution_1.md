

# Problem 1 — Coin × Coin

---

## 1. Description of the Random Experiment

We toss a coin **two times**.

Each toss has two possible outcomes:

* $H = \text{Head}$
* $T = \text{Tail}$

Each toss is independent.

---

## 2. Sample Space $\Omega$

Each toss has 2 possible outcomes, so:

$$
2 \times 2 = 4
$$

Thus:

$$
\Omega = {HH, HT, TH, TT}
$$

---

## 3. Graphical Representation

We represent outcomes as a table:

|       | H | T |
| ----- | - | - |
| **H** | . | . |
| **T** | . | . |

Each cell corresponds to:

* $(H,H)$
* $(H,T)$
* $(T,H)$
* $(T,T)$

---

# Part A — Marking Events

---

## 1. Exactly one head

We analyze each outcome:

### $HH$

$$
1 + 1 = 2
$$

Not valid

---

### $HT$

$$
1 + 0 = 1
$$

Valid

---

### $TH$

$$
0 + 1 = 1
$$

Valid

---

### $TT$

$$
0 + 0 = 0
$$

Not valid

---

### Final marking

|       | H | T |
| ----- | - | - |
| **H** | . | X |
| **T** | X | . |

---

## 2. Both tosses are the same

We require:

$$
\text{first toss} = \text{second toss}
$$

---

### $HH$

$$
H = H
$$

Valid

---

### $HT$

$$
H \ne T
$$

Not valid

---

### $TH$

$$
T \ne H
$$

Not valid

---

### $TT$

$$
T = T
$$

Valid

---

### Final marking

|       | H | T |
| ----- | - | - |
| **H** | X | . |
| **T** | . | X |

---

## 3. At least one head

We require:

$$
\geq 1 \text{ head}
$$

---

### $HH$

$$
1 + 1 = 2 \geq 1
$$

Valid

---

### $HT$

$$
1 + 0 = 1 \geq 1
$$

Valid

---

### $TH$

$$
0 + 1 = 1 \geq 1
$$

Valid

---

### $TT$

$$
0 + 0 = 0
$$

Not valid

---

### Final marking

|       | H | T |
| ----- | - | - |
| **H** | X | X |
| **T** | X | . |

---

## 4. First toss is tails

We require:

$$
\text{first toss} = T
$$

---

Valid outcomes:

* $TH$
* $TT$

---

### Final marking

|       | H | T |
| ----- | - | - |
| **H** | . | . |
| **T** | X | X |

---

## 5. Second toss is heads

We require:

$$
\text{second toss} = H
$$

---

Valid outcomes:

* $HH$
* $TH$

---

### Final marking

|       | H | T |
| ----- | - | - |
| **H** | X | . |
| **T** | X | . |

---

# Part B — Interpretation

---

## Case 1

|       | H | T |
| ----- | - | - |
| **H** | X | X |
| **T** | . | . |

---

### Step-by-step reasoning

Marked outcomes:

$$
HH, HT
$$

In both cases:

$$
\text{first toss} = H
$$

---

### Final interpretation

$$
\text{the first toss is heads}
$$

---

## Case 2

|       | H | T |
| ----- | - | - |
| **H** | . | X |
| **T** | X | . |

---

### Step-by-step reasoning

Marked outcomes:

$$
HT, TH
$$

Number of heads:

* $HT$:

$$
1 + 0 = 1
$$

* $TH$:

$$
0 + 1 = 1
$$

---

### Final interpretation

$$
\text{exactly one head occurs}
$$

