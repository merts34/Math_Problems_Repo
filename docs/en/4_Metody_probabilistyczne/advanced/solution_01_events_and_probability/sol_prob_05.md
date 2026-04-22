## Task 5 – Detailed Explanation

We analyze the **volume of water (in dm³ per second)** that a concrete culvert can conduct.

We are given the following probabilities:

- \(P(A) = 0.6\)
- \(P(B) = 0.7\)
- \(P(A \cup B) = 0.8\)

### Event definitions

Event **A**:  
The water volume is between **125 and 250**

$$
125 \le x \le 250
$$

Event **B**:  
The water volume is between **200 and 300**

$$
200 < x \le 300
$$

---

# Step 1 – Understanding the intervals

If we draw the intervals on a number line:


125 -----------200----------250----------300



- Event **A** covers the interval **125–250**
- Event **B** covers the interval **200–300**

The **overlap of these intervals** is:


200 -----------250


This overlap is called the **intersection**:

$$
A \cap B
$$

---

# 1. Complementary probability \(P(A')\)

The complement of an event means **the event does not happen**.

So:

- \(A\) → water is between **125 and 250**
- \(A'\) → water is **not between 125 and 250**

The complement rule is:

$$
P(A') = 1 - P(A)
$$

Substitute the value:

$$
P(A') = 1 - 0.6
$$

$$
P(A') = 0.4
$$

**Result**

$$
P(A') = 0.4
$$

Meaning there is a **40% probability** that the water volume is **outside the interval 125–250**.

---

# 2. Intersection probability \(P(A \cap B)\)

The symbol

$$
\cap
$$

means **intersection**, which means **both events happen at the same time**.

Here it means the water volume is in **both intervals simultaneously**.

That happens in the interval:


200 – 250


To calculate it we use the **union formula**:

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

Why do we subtract the intersection?

Because if we simply add:

$$
P(A) + P(B)
$$

the overlapping part would be **counted twice**, so we subtract it once.

Now substitute the values:

$$
0.8 = 0.6 + 0.7 - P(A \cap B)
$$

First compute the sum:

$$
0.6 + 0.7 = 1.3
$$

So we get:

$$
0.8 = 1.3 - P(A \cap B)
$$

Rearrange the equation:

$$
P(A \cap B) = 1.3 - 0.8
$$

$$
P(A \cap B) = 0.5
$$

**Result**

$$
P(A \cap B) = 0.5
$$

This means there is a **50% probability** that the water volume is **between 200 and 250**.

---

# 3. Probability \(P(A' \cap B')\)

This expression means:

- \(A'\) → not in A
- \(B'\) → not in B

So:

$$
A' \cap B'
$$

means the water volume is **in neither interval**.

In other words, the water volume is **outside both A and B**.

We use the rule:

$$
P(A' \cap B') = 1 - P(A \cup B)
$$

Substitute the value:

$$
P(A' \cap B') = 1 - 0.8
$$

$$
P(A' \cap B') = 0.2
$$

**Result**

$$
P(A' \cap B') = 0.2
$$

This means there is a **20% probability** that the water volume is **outside both intervals**.

---

# Final Results

| Probability | Result |
|-------------|--------|
| \(P(A')\) | 0.4 |
| \(P(A \cap B)\) | 0.5 |
| \(P(A' \cap B')\) | 0.2 |

---

# Key Probability Rules Used

Complement rule:

$$
P(A') = 1 - P(A)
$$

Union formula:

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

De Morgan’s rule:

$$
P(A' \cap B') = 1 - P(A \cup B)
$$