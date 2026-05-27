# Problem 7 — Conditional Probability with Three Categories

A company classifies customers into three activity levels:

- high activity,
- medium activity,
- low activity.

It records whether they renewed their subscription.

Let

$$
H=\text{the customer has high activity}
$$

$$
M=\text{the customer has medium activity}
$$

$$
L=\text{the customer has low activity}
$$

and

$$
R=\text{the customer renewed the subscription}.
$$

The total number of customers is

$$
400.
$$

From the table, we have:

$$
|H|=100,
$$

$$
|M|=150,
$$

$$
|L|=150,
$$

$$
|R|=200.
$$

Also,

$$
|H\cap R|=80,
$$

$$
|M\cap R|=90,
$$

and

$$
|L\cap R|=30.
$$

## 1. Why do \(H\), \(M\), and \(L\) form a partition of the sample space?

The events

$$
H,\quad M,\quad L
$$

form a partition of the sample space because every customer belongs to exactly one activity level.

A customer cannot be in two activity levels at the same time.

So the events are mutually exclusive:

$$
H\cap M=\varnothing,
$$

$$
H\cap L=\varnothing,
$$

and

$$
M\cap L=\varnothing.
$$

Also, together they cover the whole sample space:

$$
H\cup M\cup L=\Omega.
$$

Therefore,

$$
H,\ M,\ \text{and } L
$$

form a partition of the sample space.

## 2. Computing \(P(H)\), \(P(M)\), and \(P(L)\)

The probability that a customer has high activity is

$$
P(H)=\frac{|H|}{400}.
$$

Substituting the value:

$$
P(H)=\frac{100}{400}.
$$

Simplifying:

$$
P(H)=\frac{1}{4}.
$$

Therefore,

$$
P(H)=0.25.
$$

---

The probability that a customer has medium activity is

$$
P(M)=\frac{|M|}{400}.
$$

Substituting the value:

$$
P(M)=\frac{150}{400}.
$$

Simplifying:

$$
P(M)=\frac{3}{8}.
$$

Therefore,

$$
P(M)=0.375.
$$

---

The probability that a customer has low activity is

$$
P(L)=\frac{|L|}{400}.
$$

Substituting the value:

$$
P(L)=\frac{150}{400}.
$$

Simplifying:

$$
P(L)=\frac{3}{8}.
$$

Therefore,

$$
P(L)=0.375.
$$

We can check that

$$
P(H)+P(M)+P(L)=0.25+0.375+0.375.
$$

Thus,

$$
P(H)+P(M)+P(L)=1.
$$

## 3. Computing \(P(R\mid H)\), \(P(R\mid M)\), and \(P(R\mid L)\)

First, compute

$$
P(R\mid H).
$$

The conditional probability formula is

$$
P(R\mid H)=\frac{P(H\cap R)}{P(H)}.
$$

Using the original counts, this is

$$
P(R\mid H)=\frac{80}{100}.
$$

Simplifying:

$$
P(R\mid H)=\frac{4}{5}.
$$

Therefore,

$$
P(R\mid H)=0.80.
$$

This means that among high activity customers,

$$
80\%
$$

renewed their subscription.

---

Now compute

$$
P(R\mid M).
$$

Using the original counts:

$$
P(R\mid M)=\frac{90}{150}.
$$

Simplifying:

$$
P(R\mid M)=\frac{3}{5}.
$$

Therefore,

$$
P(R\mid M)=0.60.
$$

This means that among medium activity customers,

$$
60\%
$$

renewed their subscription.

---

Now compute

$$
P(R\mid L).
$$

Using the original counts:

$$
P(R\mid L)=\frac{30}{150}.
$$

Simplifying:

$$
P(R\mid L)=\frac{1}{5}.
$$

Therefore,

$$
P(R\mid L)=0.20.
$$

This means that among low activity customers,

$$
20\%
$$

renewed their subscription.

## 4. Using the law of total probability to compute \(P(R)\)

Since

$$
H,\quad M,\quad L
$$

form a partition of the sample space, we can use the law of total probability:

$$
P(R)=P(R\mid H)P(H)+P(R\mid M)P(M)+P(R\mid L)P(L).
$$

Substituting the values:

$$
P(R)=0.80\cdot 0.25+0.60\cdot 0.375+0.20\cdot 0.375.
$$

Now compute each term separately:

$$
0.80\cdot 0.25=0.20,
$$

$$
0.60\cdot 0.375=0.225,
$$

and

$$
0.20\cdot 0.375=0.075.
$$

Therefore,

$$
P(R)=0.20+0.225+0.075.
$$

Adding:

$$
P(R)=0.50.
$$

So,

$$
P(R)=0.50.
$$

We can also check this directly from the table:

$$
P(R)=\frac{200}{400}=0.50.
$$

## 5. Computing \(P(H\mid R)\), \(P(M\mid R)\), and \(P(L\mid R)\)

First, compute

$$
P(H\mid R).
$$

The conditional probability formula is

$$
P(H\mid R)=\frac{P(H\cap R)}{P(R)}.
$$

Using the original counts:

$$
P(H\mid R)=\frac{80}{200}.
$$

Simplifying:

$$
P(H\mid R)=\frac{2}{5}.
$$

Therefore,

$$
P(H\mid R)=0.40.
$$

This means that among customers who renewed,

$$
40\%
$$

were high activity customers.

---

Now compute

$$
P(M\mid R).
$$

Using the original counts:

$$
P(M\mid R)=\frac{90}{200}.
$$

Simplifying:

$$
P(M\mid R)=\frac{9}{20}.
$$

Therefore,

$$
P(M\mid R)=0.45.
$$

This means that among customers who renewed,

$$
45\%
$$

were medium activity customers.

---

Now compute

$$
P(L\mid R).
$$

Using the original counts:

$$
P(L\mid R)=\frac{30}{200}.
$$

Simplifying:

$$
P(L\mid R)=\frac{3}{20}.
$$

Therefore,

$$
P(L\mid R)=0.15.
$$

This means that among customers who renewed,

$$
15\%
$$

were low activity customers.

We can check that these probabilities add up to 1:

$$
P(H\mid R)+P(M\mid R)+P(L\mid R)=0.40+0.45+0.15.
$$

Thus,

$$
P(H\mid R)+P(M\mid R)+P(L\mid R)=1.
$$

## 6. Interpreting the difference between \(P(R\mid H)\) and \(P(H\mid R)\)

The probability

$$
P(R\mid H)
$$

means:

$$
\text{among high activity customers, what is the probability that they renewed?}
$$

We found that

$$
P(R\mid H)=0.80.
$$

So among high activity customers,

$$
80\%
$$

renewed their subscription.

---

The probability

$$
P(H\mid R)
$$

means:

$$
\text{among customers who renewed, what is the probability that they were high activity customers?}
$$

We found that

$$
P(H\mid R)=0.40.
$$

So among customers who renewed,

$$
40\%
$$

were high activity customers.

These two probabilities are different because the condition is different.

In general,

$$
P(R\mid H)\neq P(H\mid R).
$$

## Final Answers

$$
P(H)=\frac{100}{400}=0.25
$$

$$
P(M)=\frac{150}{400}=0.375
$$

$$
P(L)=\frac{150}{400}=0.375
$$

$$
P(R\mid H)=\frac{80}{100}=0.80
$$

$$
P(R\mid M)=\frac{90}{150}=0.60
$$

$$
P(R\mid L)=\frac{30}{150}=0.20
$$

Using the law of total probability:

$$
P(R)=P(R\mid H)P(H)+P(R\mid M)P(M)+P(R\mid L)P(L)
$$

$$
P(R)=0.80\cdot 0.25+0.60\cdot 0.375+0.20\cdot 0.375
$$

$$
P(R)=0.20+0.225+0.075=0.50
$$

$$
P(H\mid R)=\frac{80}{200}=0.40
$$

$$
P(M\mid R)=\frac{90}{200}=0.45
$$

$$
P(L\mid R)=\frac{30}{200}=0.15
$$

Finally,

$$
P(R\mid H)=0.80
$$

means the probability of renewal among high activity customers, while

$$
P(H\mid R)=0.40
$$

means the probability of being high activity among customers who renewed.