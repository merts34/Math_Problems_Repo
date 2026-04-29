# Task 7 — Hypergeometric Model

---

## Problem

A box contains:

* 12 working light bulbs
* 3 defective light bulbs

We draw 5 bulbs **without replacement**.

We want the probability that the sample contains **exactly 2 defective bulbs**.

---

# 1. Method Used

We use the **hypergeometric distribution** because:

* the population is finite
* we draw **without replacement**
* the probability changes after each draw
* we are counting how many defective bulbs appear in the sample

So this is **not** binomial.

---

# 2. Define the Random Variable

Let:

$$
X = \text{number of defective bulbs in the sample of 5}
$$

We want:

$$
P(X=2)
$$

---

# 3. Identify the Parameters

Total number of bulbs:

$$
N = 15
$$

Number of defective bulbs:

$$
K = 3
$$

Number of working bulbs:

$$
15 - 3 = 12
$$

Sample size:

$$
n = 5
$$

We want exactly:

$$
k = 2
$$

---

# 4. Hypergeometric Formula

The hypergeometric probability formula is:

$$
P(X=k) = \frac{\binom{K}{k}\binom{N-K}{n-k}}{\binom{N}{n}}
$$

Now substitute the values:

$$
P(X=2) = \frac{\binom{3}{2}\binom{12}{5-2}}{\binom{15}{5}}
$$

Since:

$$
5 - 2 = 3
$$

we get:

$$
P(X=2) = \frac{\binom{3}{2}\binom{12}{3}}{\binom{15}{5}}
$$

---

# 5. Meaning of Each Part

We now explain each term carefully.

## First term: choosing the defective bulbs

We need exactly 2 defective bulbs from the 3 defective bulbs available.

That is:

$$
\binom{3}{2}
$$

---

## Second term: choosing the working bulbs

Since we draw 5 bulbs total and 2 are defective, the remaining bulbs must be working:

$$
5 - 2 = 3
$$

So we need to choose 3 working bulbs from 12 working bulbs:

$$
\binom{12}{3}
$$

---

## Third term: total possible samples

We choose any 5 bulbs from the 15 total bulbs:

$$
\binom{15}{5}
$$

---

# 6. Compute Each Combination Step by Step

---

## 6.1 Compute $\binom{3}{2}$

By definition:

$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

So:

$$
\binom{3}{2} = \frac{3!}{2!(3-2)!}
$$

First simplify inside:

$$
3 - 2 = 1
$$

So:

$$
\binom{3}{2} = \frac{3!}{2!1!}
$$

Now expand factorials:

$$
3! = 3 \cdot 2 \cdot 1 = 6
$$

$$
2! = 2 \cdot 1 = 2
$$

$$
1! = 1
$$

So:

$$
\binom{3}{2} = \frac{6}{2 \cdot 1}
$$

$$
= \frac{6}{2}
$$

$$
= 3
$$

---

## 6.2 Compute $\binom{12}{3}$

By definition:

$$
\binom{12}{3} = \frac{12!}{3!(12-3)!}
$$

First simplify:

$$
12 - 3 = 9
$$

So:

$$
\binom{12}{3} = \frac{12!}{3!9!}
$$

Now expand the factorial so we can cancel $9!$:

$$
12! = 12 \cdot 11 \cdot 10 \cdot 9!
$$

So:

$$
\binom{12}{3} = \frac{12 \cdot 11 \cdot 10 \cdot 9!}{3! \cdot 9!}
$$

Cancel $9!$:

$$
= \frac{12 \cdot 11 \cdot 10}{3!}
$$

Now compute $3!$:

$$
3! = 3 \cdot 2 \cdot 1 = 6
$$

So:

$$
\binom{12}{3} = \frac{12 \cdot 11 \cdot 10}{6}
$$

Now compute the numerator:

$$
12 \cdot 11 = 132
$$

$$
132 \cdot 10 = 1320
$$

Now divide:

$$
\frac{1320}{6} = 220
$$

So:

$$
\binom{12}{3} = 220
$$

---

## 6.3 Compute $\binom{15}{5}$

By definition:

$$
\binom{15}{5} = \frac{15!}{5!(15-5)!}
$$

First simplify:

$$
15 - 5 = 10
$$

So:

$$
\binom{15}{5} = \frac{15!}{5!10!}
$$

Now expand $15!$ in a way that cancels $10!$:

$$
15! = 15 \cdot 14 \cdot 13 \cdot 12 \cdot 11 \cdot 10!
$$

So:

$$
\binom{15}{5} = \frac{15 \cdot 14 \cdot 13 \cdot 12 \cdot 11 \cdot 10!}{5! \cdot 10!}
$$

Cancel $10!$:

$$
= \frac{15 \cdot 14 \cdot 13 \cdot 12 \cdot 11}{5!}
$$

Now compute $5!$:

$$
5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120
$$

So:

$$
\binom{15}{5} = \frac{15 \cdot 14 \cdot 13 \cdot 12 \cdot 11}{120}
$$

Now compute the numerator step by step:

$$
15 \cdot 14 = 210
$$

$$
210 \cdot 13 = 2730
$$

$$
2730 \cdot 12 = 32760
$$

$$
32760 \cdot 11 = 360360
$$

So:

$$
\binom{15}{5} = \frac{360360}{120}
$$

Now divide:

$$
360360 \div 120 = 3003
$$

So:

$$
\binom{15}{5} = 3003
$$

---

# 7. Substitute into the Formula

We had:

$$
P(X=2) = \frac{\binom{3}{2}\binom{12}{3}}{\binom{15}{5}}
$$

Now substitute the computed values:

$$
P(X=2) = \frac{3 \cdot 220}{3003}
$$

Multiply the numerator:

$$
3 \cdot 220 = 660
$$

So:

$$
P(X=2) = \frac{660}{3003}
$$

---

# 8. Simplify the Fraction

We can divide numerator and denominator by 3:

$$
\frac{660}{3003} = \frac{220}{1001}
$$

So:

$$
P(X=2) = \frac{220}{1001}
$$

Now approximate:

$$
\frac{220}{1001} \approx 0.2198
$$

So:

$$
P(X=2) \approx 0.220
$$

---

# 9. Final Answer

The probability that the sample contains exactly 2 defective bulbs is:

$$
P(X=2) = \frac{\binom{3}{2}\binom{12}{3}}{\binom{15}{5}}
$$

and numerically:

$$
P(X=2) \approx 0.2198
$$

---

# 10. Interpretation

This means that if we repeatedly draw 5 bulbs from the box without replacement, about:

$$
21.98%
$$

of the samples will contain exactly 2 defective bulbs.

