# Problem 8 — Bayes' Formula from a Table

A fraud detection system classifies transactions as suspicious or not suspicious.

Let

$$
F=\text{the transaction is fraudulent}
$$

and

$$
S=\text{the transaction is marked suspicious}.
$$

The total number of transactions is

$$
10000.
$$

From the table, we have:

$$
|F|=100,
$$

$$
|F^c|=9900,
$$

$$
|S|=395,
$$

$$
|S^c|=9605,
$$

$$
|F\cap S|=98,
$$

and

$$
|F^c\cap S|=297.
$$

## 1. Computing \(P(F)\), \(P(S\mid F)\), and \(P(S\mid F^c)\)

First, compute

$$
P(F).
$$

The probability that a transaction is fraudulent is

$$
P(F)=\frac{|F|}{10000}.
$$

Substituting the value:

$$
P(F)=\frac{100}{10000}.
$$

Simplifying:

$$
P(F)=\frac{1}{100}.
$$

Therefore,

$$
P(F)=0.01.
$$

So only

$$
1\%
$$

of all transactions are fraudulent.

---

Now compute

$$
P(S\mid F).
$$

The conditional probability formula is

$$
P(S\mid F)=\frac{P(F\cap S)}{P(F)}.
$$

Using the original counts, this is

$$
P(S\mid F)=\frac{98}{100}.
$$

Simplifying:

$$
P(S\mid F)=\frac{49}{50}.
$$

Therefore,

$$
P(S\mid F)=0.98.
$$

This means that among fraudulent transactions,

$$
98\%
$$

are marked suspicious.

---

Now compute

$$
P(S\mid F^c).
$$

The event

$$
F^c
$$

means that the transaction is not fraudulent, so the transaction is legitimate.

Using the original counts:

$$
P(S\mid F^c)=\frac{297}{9900}.
$$

Simplifying:

$$
P(S\mid F^c)=\frac{3}{100}.
$$

Therefore,

$$
P(S\mid F^c)=0.03.
$$

This means that among legitimate transactions,

$$
3\%
$$

are marked suspicious.

## 2. Using the law of total probability to compute \(P(S)\)

The events

$$
F
$$

and

$$
F^c
$$

form a partition of the sample space.

Therefore, by the law of total probability,

$$
P(S)=P(S\mid F)P(F)+P(S\mid F^c)P(F^c).
$$

We already know that

$$
P(F)=0.01.
$$

So,

$$
P(F^c)=1-P(F).
$$

Substituting:

$$
P(F^c)=1-0.01.
$$

Therefore,

$$
P(F^c)=0.99.
$$

Now substitute all values into the law of total probability:

$$
P(S)=0.98\cdot 0.01+0.03\cdot 0.99.
$$

Compute the first term:

$$
0.98\cdot 0.01=0.0098.
$$

Compute the second term:

$$
0.03\cdot 0.99=0.0297.
$$

Therefore,

$$
P(S)=0.0098+0.0297.
$$

Adding:

$$
P(S)=0.0395.
$$

So,

$$
P(S)=0.0395.
$$

We can also check this directly from the table:

$$
P(S)=\frac{395}{10000}.
$$

Thus,

$$
P(S)=0.0395.
$$

## 3. Using Bayes' formula to compute \(P(F\mid S)\)

Bayes' formula is

$$
P(F\mid S)=\frac{P(S\mid F)P(F)}{P(S)}.
$$

Substituting the values:

$$
P(F\mid S)=\frac{0.98\cdot 0.01}{0.0395}.
$$

First compute the numerator:

$$
0.98\cdot 0.01=0.0098.
$$

So,

$$
P(F\mid S)=\frac{0.0098}{0.0395}.
$$

Using the original counts, this is also

$$
P(F\mid S)=\frac{98}{395}.
$$

Now divide:

$$
P(F\mid S)\approx 0.2481.
$$

Therefore,

$$
P(F\mid S)\approx 0.2481.
$$

As a percentage,

$$
P(F\mid S)\approx 24.81\%.
$$

This means that among transactions marked suspicious, about

$$
24.81\%
$$

are actually fraudulent.

## 4. Among suspicious transactions, are most transactions fraudulent or legitimate?

From the table, among suspicious transactions:

$$
|F\cap S|=98
$$

and

$$
|F^c\cap S|=297.
$$

So suspicious fraudulent transactions are

$$
98,
$$

while suspicious legitimate transactions are

$$
297.
$$

Since

$$
297>98,
$$

most suspicious transactions are legitimate, not fraudulent.

Another way to see this is:

$$
P(F\mid S)\approx 0.2481
$$

and

$$
P(F^c\mid S)=1-P(F\mid S).
$$

Substituting:

$$
P(F^c\mid S)=1-0.2481.
$$

Therefore,

$$
P(F^c\mid S)\approx 0.7519.
$$

So about

$$
75.19\%
$$

of suspicious transactions are legitimate.

## 5. Why can this happen even if the system detects fraudulent transactions very well?

This can happen because fraudulent transactions are very rare.

The system detects fraudulent transactions very well because

$$
P(S\mid F)=0.98.
$$

This means that if a transaction is fraudulent, the system marks it suspicious with probability

$$
98\%.
$$

However, fraud is rare because

$$
P(F)=0.01.
$$

This means only

$$
1\%
$$

of all transactions are fraudulent.

Even though the false positive rate for legitimate transactions is only

$$
P(S\mid F^c)=0.03,
$$

there are many more legitimate transactions than fraudulent transactions.

There are

$$
9900
$$

legitimate transactions, and

$$
3\%
$$

of them are marked suspicious:

$$
0.03\cdot 9900=297.
$$

There are only

$$
100
$$

fraudulent transactions, and

$$
98\%
$$

of them are marked suspicious:

$$
0.98\cdot 100=98.
$$

Therefore, the suspicious group contains more legitimate transactions than fraudulent transactions:

$$
297>98.
$$

## 6. Explaining the role of the base rate \(P(F)\)

The base rate

$$
P(F)
$$

is the original probability that a transaction is fraudulent before knowing whether it was marked suspicious.

In this problem,

$$
P(F)=0.01.
$$

This means fraud is very rare.

Because the base rate is very low, even a good detection system can produce many suspicious transactions that are actually legitimate.

So the base rate is important because it affects the posterior probability

$$
P(F\mid S).
$$

Even though

$$
P(S\mid F)=0.98
$$

is very high, the final probability

$$
P(F\mid S)
$$

is only about

$$
0.2481.
$$

Therefore, a suspicious mark increases the probability of fraud, but it does not mean that the transaction is most likely fraudulent.

## Final Answers

$$
P(F)=\frac{100}{10000}=0.01
$$

$$
P(S\mid F)=\frac{98}{100}=0.98
$$

$$
P(S\mid F^c)=\frac{297}{9900}=0.03
$$

Using the law of total probability:

$$
P(S)=P(S\mid F)P(F)+P(S\mid F^c)P(F^c)
$$

$$
P(S)=0.98\cdot 0.01+0.03\cdot 0.99
$$

$$
P(S)=0.0098+0.0297
$$

$$
P(S)=0.0395
$$

Using Bayes' formula:

$$
P(F\mid S)=\frac{P(S\mid F)P(F)}{P(S)}
$$

$$
P(F\mid S)=\frac{0.98\cdot 0.01}{0.0395}
$$

$$
P(F\mid S)=\frac{0.0098}{0.0395}
$$

$$
P(F\mid S)=\frac{98}{395}
$$

$$
P(F\mid S)\approx 0.2481
$$

So among suspicious transactions, about

$$
24.81\%
$$

are fraudulent, and about

$$
75.19\%
$$

are legitimate.

Therefore, most suspicious transactions are legitimate.

This happens because the base rate of fraud is very low:

$$
P(F)=0.01.
$$