
# Problem 4 — Building Complex Statements

---

## 1. Description of the Random Experiment

We roll a die **two times**.

Each result:

$$
i \in {1,2,3,4,5,6}, \quad j \in {1,2,3,4,5,6}
$$

Each outcome is:

$$
(i,j)
$$

---

## 2. Sample Space Size

Each die has 6 outcomes:

$$
6 \times 6 = 36
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

---

# Part A — Basic Events

---

## Event $A$: sum = 7

---

### Step 1 — Definition

$$
i + j = 7
$$

---

### Step 2 — Find all pairs

We check systematically:

* $1 + 6 = 7$
* $2 + 5 = 7$
* $3 + 4 = 7$
* $4 + 3 = 7$
* $5 + 2 = 7$
* $6 + 1 = 7$

---

### Final marking of $A$

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | X |
| **2** | . | . | . | . | X | . |
| **3** | . | . | . | X | . | . |
| **4** | . | . | X | . | . | . |
| **5** | . | X | . | . | . | . |
| **6** | X | . | . | . | . | . |

---

## Event $B$: first die > second die

---

### Step 1 — Definition

$$
i > j
$$

---

### Step 2 — Build row by row

Row 1: no values smaller → all dots

Row 2:

$$
2 > 1
$$

→ mark column 1

Row 3:

$$
3 > 1,\quad 3 > 2
$$

→ mark columns 1,2

Continue same logic.

---

### Final marking of $B$

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | . |
| **2** | X | . | . | . | . | . |
| **3** | X | X | . | . | . | . |
| **4** | X | X | X | . | . | . |
| **5** | X | X | X | X | . | . |
| **6** | X | X | X | X | X | . |

---

## Event $C$: at least one die shows 6

---

### Step 1 — Definition

$$
i = 6 \quad \text{OR} \quad j = 6
$$

---

### Step 2 — Construct

* row 6 → all X
* column 6 → all X

---

### Final marking of $C$

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | X |
| **2** | . | . | . | . | . | X |
| **3** | . | . | . | . | . | X |
| **4** | . | . | . | . | . | X |
| **5** | . | . | . | . | . | X |
| **6** | X | X | X | X | X | X |

---

# Part B — Compound Events

---

## 1. $A \cup C$ (OR)

---

### Step 1 — Meaning

$$
A \cup C = \text{in A OR in C}
$$

So we take:

* all X from A
* all X from C

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | X |
| **2** | . | . | . | . | X | X |
| **3** | . | . | . | X | . | X |
| **4** | . | . | X | . | . | X |
| **5** | . | X | . | . | . | X |
| **6** | X | X | X | X | X | X |

---

## 2. $A \cap C$ (AND)

---

### Step 1 — Meaning

$$
A \cap C = \text{in BOTH A and C}
$$

---

### Step 2 — Find overlap

From A:

* $(1,6)$ → has 6 → yes
* $(6,1)$ → has 6 → yes

Other A points do NOT contain 6.

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | X |
| **2** | . | . | . | . | . | . |
| **3** | . | . | . | . | . | . |
| **4** | . | . | . | . | . | . |
| **5** | . | . | . | . | . | . |
| **6** | X | . | . | . | . | . |

---

## 3. $B \cap C$

---

### Step 1 — Meaning

$$
i > j \quad \text{AND} \quad (i=6 \text{ OR } j=6)
$$

---

### Step 2 — Analyze

Case 1: $i=6$

Then:

$$
6 > j
$$

Valid for:

$$
j = 1,2,3,4,5
$$

---

Case 2: $j=6$

Then:

$$
i > 6
$$

Impossible

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | . |
| **2** | . | . | . | . | . | . |
| **3** | . | . | . | . | . | . |
| **4** | . | . | . | . | . | . |
| **5** | . | . | . | . | . | . |
| **6** | X | X | X | X | X | . |

---

## 4. $A \cap B^c$

---

### Step 1 — Meaning

* $A$: sum = 7
* $B^c$: NOT (first > second)

So:

$$
i \le j
$$

---

### Step 2 — Filter A

From A:

* $(1,6)$ → $1 \le 6$ → keep
* $(2,5)$ → $2 \le 5$ → keep
* $(3,4)$ → $3 \le 4$ → keep
* $(4,3)$ → $4 > 3$ → remove
* $(5,2)$ → remove
* $(6,1)$ → remove

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | X |
| **2** | . | . | . | . | X | . |
| **3** | . | . | . | X | . | . |
| **4** | . | . | . | . | . | . |
| **5** | . | . | . | . | . | . |
| **6** | . | . | . | . | . | . |

---

## 5. $A \cap C^c$

---

### Step 1 — Meaning

$$
\text{sum = 7 AND no 6 appears}
$$

---

### Step 2 — Remove 6 cases from A

Remove:

* $(1,6)$
* $(6,1)$

Keep:

* $(2,5),(3,4),(4,3),(5,2)$

---

### Final marking

|       | 1 | 2 | 3 | 4 | 5 | 6 |
| ----- | - | - | - | - | - | - |
| **1** | . | . | . | . | . | . |
| **2** | . | . | . | . | X | . |
| **3** | . | . | . | X | . | . |
| **4** | . | . | X | . | . | . |
| **5** | . | X | . | . | . | . |
| **6** | . | . | . | . | . | . |

---

# Final Concept (VERY IMPORTANT)

---

## 1. Logic → Set Operations

| Logic | Set        |
| ----- | ---------- |
| AND   | $\cap$     |
| OR    | $\cup$     |
| NOT   | complement |

---

## 2. Visual Understanding

* diagonal → equality
* triangle → inequalities
* cross → unions

---

## 3. Core Idea

You are no longer:

* calculating numbers

You are:

* building **mathematical structure**

---