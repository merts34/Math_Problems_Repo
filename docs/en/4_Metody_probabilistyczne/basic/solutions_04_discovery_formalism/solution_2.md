

# Problem 2 — Die × Die

---

## 1. Description of the Random Experiment

We roll a fair die **two times**.

Each die has possible outcomes:

$$
{1,2,3,4,5,6}
$$

Each roll is independent.

---

## 2. Sample Space $\Omega$

Each die has 6 outcomes, so:

$$
6 \times 6 = 36
$$

Thus:

$$
\Omega = {(i,j) \mid i \in {1,\dots,6},; j \in {1,\dots,6}}
$$

---

## 3. Graphical Representation

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | . |
| **2** | . | . | . | . | . | . |
| **3** | . | . | . | . | . | . |
| **4** | . | . | . | . | . | . |
| **5** | . | . | . | . | . | . |
| **6** | . | . | . | . | . | . |

* rows = first die
* columns = second die

---

# Part A — Marking Events

---

## 1. The sum is equal to 8

We require:

$$
i + j = 8
$$

---

### Find all solutions

* $2 + 6 = 8$
* $3 + 5 = 8$
* $4 + 4 = 8$
* $5 + 3 = 8$
* $6 + 2 = 8$

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | . |
| **2** | . | . | . | . | . | X |
| **3** | . | . | . | . | X | . |
| **4** | . | . | . | X | . | . |
| **5** | . | . | X | . | . | . |
| **6** | . | X | . | . | . | . |

---

## 2. First die is greater than the second

We require:

$$
i > j
$$

---

### Step-by-step idea

* row 1 → nothing (1 is smallest)
* row 2 → only column 1
* row 3 → columns 1,2
* row 4 → columns 1,2,3
* row 5 → columns 1,2,3,4
* row 6 → columns 1,2,3,4,5

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | . |
| **2** | X | . | . | . | . | . |
| **3** | X | X | . | . | . | . |
| **4** | X | X | X | . | . | . |
| **5** | X | X | X | X | . | . |
| **6** | X | X | X | X | X | . |

---

## 3. Both dice show even numbers

Even numbers:

$$
{2,4,6}
$$

---

We require:

$$
i \in {2,4,6}, \quad j \in {2,4,6}
$$

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | . |
| **2** | . | X | . | X | . | X |
| **3** | . | . | . | . | . | . |
| **4** | . | X | . | X | . | X |
| **5** | . | . | . | . | . | . |
| **6** | . | X | . | X | . | X |

---

## 4. At least one die shows 6

We require:

$$
i = 6 \quad \text{or} \quad j = 6
$$

---

### Step-by-step

* entire row 6
* entire column 6

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | X |
| **2** | . | . | . | . | . | X |
| **3** | . | . | . | . | . | X |
| **4** | . | . | . | . | . | X |
| **5** | . | . | . | . | . | X |
| **6** | X | X | X | X | X | X |

---

## 5. Exactly one die shows 1

We require:

* one die = 1
* the other ≠ 1

---

### Valid cases

* $(1,2),(1,3),(1,4),(1,5),(1,6)$
* $(2,1),(3,1),(4,1),(5,1),(6,1)$

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | X | X | X | X | X |
| **2** | X | . | . | . | . | . |
| **3** | X | . | . | . | . | . |
| **4** | X | . | . | . | . | . |
| **5** | X | . | . | . | . | . |
| **6** | X | . | . | . | . | . |

---

# Part B — Interpretation

---

## Case 1

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | . |
| **2** | . | . | . | . | . | . |
| **3** | . | . | X | X | X | X |
| **4** | . | . | X | X | X | X |
| **5** | . | . | X | X | X | X |
| **6** | . | . | X | X | X | X |

---

### Step-by-step reasoning

Marked columns:

$$
3,4,5,6
$$

This means:

$$
\text{second die} \geq 3
$$

Rows allowed:

$$
3,4,5,6
$$

This means:

$$
\text{first die} \geq 3
$$

---

### Final interpretation

$$
\text{both dice show numbers greater than or equal to 3}
$$

---

## Case 2

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | X | . | . | . | . | . |
| **2** | . | X | . | . | . | . |
| **3** | . | . | X | . | . | . |
| **4** | . | . | . | X | . | . |
| **5** | . | . | . | . | X | . |
| **6** | . | . | . | . | . | X |

---

### Step-by-step reasoning

Marked cells:

$$
(1,1),(2,2),(3,3),(4,4),(5,5),(6,6)
$$

So:

$$
i = j
$$

---

### Final interpretation

$$
\text{both dice show the same number}
$$

---

# Final Concept

This problem shows:

* events are geometric regions in the table
* inequalities → triangular regions
* equalities → diagonal
* unions → combined regions

