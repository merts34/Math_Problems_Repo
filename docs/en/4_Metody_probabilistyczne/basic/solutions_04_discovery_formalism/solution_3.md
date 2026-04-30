

# Problem 3 — Weather (7 days × 3 states)

---

## 1. Description of the Random Experiment

We consider a **week** consisting of 7 days:

$$
\text{Mon, Tue, Wed, Thu, Fri, Sat, Sun}
$$

Each day can have exactly **one weather state**:

* $S = \text{sunny}$
* $C = \text{cloudy}$
* $R = \text{rainy}$

---

## 2. Important Concept (VERY IMPORTANT)

This table **does NOT list all outcomes**.

Instead:

* Each column = a **day**
* Each row = a **possible state**
* Marking a cell = **that state is allowed/selected for that day**

So we are **not listing sequences**, we are describing **constraints on sequences**.

---

## 3. Graphical Representation

|       | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| **S** | .   | .   | .   | .   | .   | .   | .   |
| **C** | .   | .   | .   | .   | .   | .   | .   |
| **R** | .   | .   | .   | .   | .   | .   | .   |

---

# Part A — Marking Events

---

## 1. Monday is sunny

---

### Step 1 — Understand the statement

We are told:

$$
\text{Monday is sunny}
$$

This is a **constraint on one day only**.

Important:

* Monday MUST be $S$
* Other days are **not restricted**

---

### Step 2 — Translate to table

We go to column **Mon**:

* mark $S$
* do NOT mark $C$ or $R$

All other columns stay unrestricted → we leave them as dots (no forced selection)

---

### Final marking

|       | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| **S** | X   | .   | .   | .   | .   | .   | .   |
| **C** | .   | .   | .   | .   | .   | .   | .   |
| **R** | .   | .   | .   | .   | .   | .   | .   |

---

## 2. The weekend (Saturday and Sunday) is rainy

---

### Step 1 — Understand the statement

We have TWO constraints:

$$
\text{Saturday} = R
$$

$$
\text{Sunday} = R
$$

---

### Step 2 — Apply constraints

Go to columns:

* Sat → mark $R$
* Sun → mark $R$

Other days unrestricted.

---

### Final marking

|       | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| **S** | .   | .   | .   | .   | .   | .   | .   |
| **C** | .   | .   | .   | .   | .   | .   | .   |
| **R** | .   | .   | .   | .   | .   | X   | X   |

---

## 3. It rains on Wednesday or Friday

---

### Step 1 — Understand logical word “OR”

This means:

$$
\text{Wed = R OR Fri = R}
$$

Important:

* could be only Wed
* could be only Fri
* could be both

---

### Step 2 — Translate

We must allow:

* Wed → R
* Fri → R

We mark both, because both are allowed possibilities.

---

### Final marking

|       | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| **S** | .   | .   | .   | .   | .   | .   | .   |
| **C** | .   | .   | .   | .   | .   | .   | .   |
| **R** | .   | .   | X   | .   | X   | .   | .   |

---

## 4. There is no rainy day during the week

---

### Step 1 — Understand the statement

“No rainy day” means:

$$
R \text{ is impossible for all days}
$$

---

### Step 2 — Translate

We eliminate row $R$ completely.

So:

* no cell in row $R$ is allowed
* only $S$ and $C$ remain possible

---

### Final marking

|       | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| **S** | X   | X   | X   | X   | X   | X   | X   |
| **C** | X   | X   | X   | X   | X   | X   | X   |
| **R** | .   | .   | .   | .   | .   | .   | .   |

---

## 5. Thursday is not sunny

---

### Step 1 — Understand

$$
\text{Thu} \ne S
$$

So Thursday can be:

$$
C \text{ or } R
$$

---

### Step 2 — Translate

At column Thu:

* remove $S$
* allow $C$ and $R$

---

### Final marking

|       | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| **S** | .   | .   | .   | .   | .   | .   | .   |
| **C** | .   | .   | .   | X   | .   | .   | .   |
| **R** | .   | .   | .   | X   | .   | .   | .   |

---

# Part B — Interpretation

---

## Case 1

|       | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| **S** | .   | .   | .   | .   | .   | X   | X   |
| **C** | .   | .   | .   | .   | .   | .   | .   |
| **R** | .   | .   | .   | .   | .   | .   | .   |

---

### Step-by-step reasoning

Only marked cells:

* Sat → S
* Sun → S

This means:

$$
\text{Saturday = sunny}
$$

$$
\text{Sunday = sunny}
$$

No other constraints.

---

### Final interpretation

$$
\text{the weekend is sunny}
$$

---

## Case 2

|       | Mon | Tue | Wed | Thu | Fri | Sat | Sun |
| ----- | --- | --- | --- | --- | --- | --- | --- |
| **S** | X   | X   | X   | X   | X   | X   | X   |
| **C** | X   | X   | X   | X   | X   | X   | X   |
| **R** | .   | .   | .   | .   | .   | .   | .   |

---

### Step-by-step reasoning

We see:

* all $R$ cells are forbidden
* only $S$ and $C$ allowed

So:

$$
\text{no rainy day is allowed}
$$

---

### Final interpretation

$$
\text{there is no rainy day during the week}
$$

---

#  Final Concept (VERY IMPORTANT NOTES TO MYSELF)

This problem teaches:

---

## 1. Events are NOT always simple outcomes

Here:

* we are not listing sequences
* we are defining **conditions on sequences**

---

## 2. Columns = variables

Each day is like a variable:

$$
\text{Day}_i \in {S,C,R}
$$

---

## 3. Marking = constraint

* X → allowed
* . → not allowed

---

## 4. Logic → structure

* “OR” → multiple columns
* “NOT” → removing rows
* “AND” → combining restrictions

