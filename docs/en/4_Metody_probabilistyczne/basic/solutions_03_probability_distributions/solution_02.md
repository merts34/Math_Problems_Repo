# Task 2 — Hypergeometric Model (Sampling from a Batch)

---

## 1. Description of the Random Experiment

We have a warehouse containing:

* 20 components in total
* 5 defective components
* 15 functional components

We randomly select 4 components **without replacement**.

This means:

* After selecting one component, it is NOT put back
* So probabilities change after each draw

---

## 2. Sample Space and Random Variable

Instead of listing all individual outcomes, we define a random variable:

$$
X = \text{number of defective components in the sample of 4}
$$

---

## 3. Possible Values of $X$

We are selecting 4 components.

* Minimum defective: 0
* Maximum defective: 4

So:

$$
X \in {0,1,2,3,4}
$$

---

## 4. Hypergeometric Distribution Formula

The probability of selecting exactly $k$ defective components is:

$$
P(X = k) = \frac{\binom{5}{k}\binom{15}{4-k}}{\binom{20}{4}}
$$

---

## 5. Step-by-step Interpretation of the Formula

We now break it down completely:

### Step 1: Choose defective components

We choose $k$ defective components from 5:

$$
\binom{5}{k}
$$

---

### Step 2: Choose non-defective components

We choose $(4-k)$ good components from 15:

$$
\binom{15}{4-k}
$$

---

### Step 3: Total possible selections

We choose any 4 components from 20:

$$
\binom{20}{4}
$$

---

## 6. Final Probability Structure

So the full probability is:

$$
P(X = k) = \frac{\binom{5}{k}\binom{15}{4-k}}{\binom{20}{4}}
$$

---

## 7. Expanded Denominator

Let’s compute:

$$
\binom{20}{4} = \frac{20 \cdot 19 \cdot 18 \cdot 17}{4 \cdot 3 \cdot 2 \cdot 1}
$$

Now compute step by step:

Numerator:

$$
20 \cdot 19 = 380
$$

$$
380 \cdot 18 = 6840
$$

$$
6840 \cdot 17 = 116280
$$

Denominator:

$$
4 \cdot 3 \cdot 2 \cdot 1 = 24
$$

Now divide:

$$
\binom{20}{4} = \frac{116280}{24} = 4845
$$

---

## 8. Final Simplified Distribution

Now we can write:

$$
P(X = k) = \frac{\binom{5}{k}\binom{15}{4-k}}{4845}
$$

---

## 9. Meaning of Success

A success is defined as:

$$
\text{Success} = \text{selecting a defective component}
$$

---

## 10. Interpretation of the Model

This is NOT binomial because:

* Sampling is without replacement
* Probabilities change after each draw
* Population is finite

So independence does NOT hold.

---

## 11. Key Intuition

Instead of:

* “each trial has fixed probability”

We have:

* “we are selecting from a fixed pool of objects”

So the correct model is:

$$
\text{Hypergeometric distribution}
$$

