

# Problem 5 — From recorded frequencies to probability 
---

## 1. Given experiment

A six-sided die is rolled **1000 times**.

We are given the observed counts:

$$
n({1})=168,\quad
n({2})=154,\quad
n({3})=181
$$

$$
n({4})=167,\quad
n({5})=160,\quad
n({6})=170
$$

---

## 2. Sample space

The set of all possible outcomes is:

$$
\Omega = {1,2,3,4,5,6}
$$

---

### WHY this matters

This means:

* every roll MUST end in exactly one element of Ω
* no outcome exists outside this set
* all events are subsets of Ω

So probability is always built on subsets of Ω.

---

## 3. Frequency definition (core formula)

For any event (A \subseteq \Omega), we define:

$$
f(A) = \frac{n(A)}{1000}
$$

---

### WHY this formula exists

We are doing this:

> converting raw counts → relative proportions

So:

* (n(A)) = how many times event happened
* 1000 = total number of experiments

So this is simply:

$$
\text{relative frequency} = \frac{\text{favorable cases}}{\text{total cases}}
$$

This is the empirical approximation of probability.

---

# Part A — Compute frequencies step by step

---

## Key principle used here

For disjoint events:

$$
n({a,b,c}) = n(a) + n(b) + n(c)
$$

WHY?

Because each outcome belongs to exactly one category → no overlap.

---

# 1. Event A = {2,4,6}

---

## Step 1 — compute total occurrences

We combine counts:

$$
n(A)=n(2)+n(4)+n(6)
$$

Now substitute:

$$
n(A)=154 + 167 + 170
$$

### WHY addition is valid

Because:

* outcomes 2,4,6 are disjoint events
* a single roll cannot be both 2 and 4 etc.

So we are using:

$$
n(A \cup B) = n(A) + n(B) \quad \text{(if disjoint)}
$$

---

## Step 2 — compute sum

$$
154 + 167 = 321
$$

$$
321 + 170 = 491
$$

So:

$$
n(A)=491
$$

---

## Step 3 — convert to frequency

$$
f(A)=\frac{491}{1000}=0.491
$$

---

### INTERPRETATION

This means:

> In 1000 trials, event A occurred 49.1% of the time.

---

# 2. Event B = {1,2,3}

---

## Step 1 — sum counts

$$
n(B)=168+154+181
$$

WHY sum?

Same reason: disjoint outcomes.

---

## Step 2 — compute

$$
168 + 154 = 322
$$

$$
322 + 181 = 503
$$

So:

$$
n(B)=503
$$

---

## Step 3 — frequency

$$
f(B)=\frac{503}{1000}=0.503
$$

---

# 3. Event C = {5,6}

---

## Step 1

$$
n(C)=160+170=330
$$

---

## Step 2

$$
f(C)=\frac{330}{1000}=0.330
$$

---

# 4. Event D = {1,3,5}

---

## Step 1

$$
n(D)=168+181+160
$$

---

## Step 2

$$
168 + 181 = 349
$$

$$
349 + 160 = 509
$$

---

## Step 3

$$
f(D)=0.509
$$

---

# 5. Event E = {1,2,3,4}

---

## Step 1

$$
n(E)=168+154+181+167
$$

---

## Step 2

$$
168 + 154 = 322
$$

$$
322 + 181 = 503
$$

$$
503 + 167 = 670
$$

---

## Step 3

$$
f(E)=0.670
$$

---

# Part B — Why these identities work

---

## Key rule used everywhere

### Disjoint additivity:

$$
f(A \cup B) = f(A) + f(B) \quad \text{if } A \cap B = \emptyset
$$

This comes directly from:

$$
n(A \cup B) = n(A) + n(B)
$$

---

## 1.

$$
f({2,4,6}) = f(2)+f(4)+f(6)
$$

WHY valid?

Because:

* {2}, {4}, {6} do not overlap
* each outcome counted once

So we are splitting a union into disjoint pieces.

---

## 2.

$$
f({1,2,3,4}) = f({1,2}) + f({3,4})
$$

### WHY grouping works

We are using **associativity of disjoint unions**:

$$
{1,2,3,4} = {1,2} \cup {3,4}
$$

and:

$$
{1,2} \cap {3,4} = \emptyset
$$

So additivity applies.

---

## 3.

$$
f({1,3,5}) + f({2,4,6}) = 1
$$

WHY?

Because:

* these two sets form a **partition of Ω**
* every outcome belongs to exactly one of them

So:

$$
\Omega = A \cup A^c
$$

and:

$$
f(A) + f(A^c) = 1
$$

---

## 4.

$$
f({5,6}) = 1 - f({1,2,3,4})
$$

WHY?

Because:

* {5,6} is complement of {1,2,3,4}

So we use:

$$
f(A^c) = 1 - f(A)
$$

---

# Part C — When addition works vs fails

---

## Key rule

### If overlap exists:

$$
f(A \cup B) \ne f(A) + f(B)
$$

Instead:

$$
f(A \cup B) = f(A) + f(B) - f(A \cap B)
$$

(This is inclusion-exclusion principle)

---

## 1. Disjoint case

$$
{1,2} \cap {5,6} = \emptyset
$$

So:

$$
f(A \cup B) = f(A) + f(B)
$$

---

## 2. Overlapping case

$$
M={1,2,3},\quad N={3,4,5}
$$

---

### Step 1 — compute overlap

$$
M \cap N = {3}
$$

So outcome 3 is double counted.

---

### Step 2 — why sum breaks

When we compute:

$$
f(M) + f(N)
$$

we are counting:

* 3 in M
* 3 in N

→ counted twice

---

### Correct formula:

$$
f(M \cup N)=f(M)+f(N)-f(M \cap N)
$$

---

# Part D — Partition idea

---

## Key principle

If Ω is partitioned into disjoint sets:

$$
\sum f(A_i) = 1
$$

WHY?

Because:

* every outcome is counted exactly once
* no overlap
* no missing elements

---

## Example:

$$
{1,2}, {3,4}, {5,6}
$$

These are disjoint and cover Ω completely.

So sum must be:

$$
1
$$

---

# Part E — From frequency to probability

---

We observe a pattern:

### 1. bounded values

$$
0 \le f(A) \le 1
$$

### 2. impossible event

$$
f(\emptyset)=0
$$

### 3. full space

$$
f(\Omega)=1
$$

### 4. additivity

$$
f(A \cup B)=f(A)+f(B)
$$

### 5. complement

$$
f(A^c)=1-f(A)
$$

---

## WHY we define probability

Because frequency:

* stabilizes as experiments grow
* becomes a theoretical object

So we define:

$$
P(A)
$$

as an abstract limit of frequency behavior.

---

# Part F — Big picture

---

## 1. Elementary level

* outcomes: 1–6
* structure: Ω

---

## 2. Empirical level

* we count occurrences
* compute frequencies

---

## 3. Theoretical level

* define probability function P
* obeying axioms

---

## FINAL IDEA

> Probability is not invented — it is the mathematical structure that describes stable behavior of frequencies under repeated experiments.

