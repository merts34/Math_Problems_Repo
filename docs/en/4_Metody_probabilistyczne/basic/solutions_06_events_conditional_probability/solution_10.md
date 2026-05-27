# Problem 10 — Comprehensive Problem: Event Algebra, Conditioning, Independence, and Bayes

A company studies whether users complete an online onboarding process.

Users are divided into two groups:

- users who received a tutorial,
- users who did not receive a tutorial.

Let

$$
T=\text{the user received the tutorial}
$$

and

$$
C=\text{the user completed onboarding}.
$$

The total number of users is

$$
500.
$$

From the table, we have:

$$
|T|=250,
$$

$$
|T^c|=250,
$$

$$
|C|=300,
$$

$$
|C^c|=200.
$$

Also,

$$
|T\cap C|=180,
$$

$$
|T\cap C^c|=70,
$$

$$
|T^c\cap C|=120,
$$

and

$$
|T^c\cap C^c|=130.
$$

## 1. Probabilities of the four disjoint regions

The event

$$
T\cap C
$$

means that the user received the tutorial and completed onboarding.

From the table, there are

$$
180
$$

such users. Therefore,

$$
P(T\cap C)=\frac{180}{500}.
$$

Simplifying:

$$
P(T\cap C)=\frac{9}{25}.
$$

Therefore,

$$
P(T\cap C)=0.36.
$$

---

The event

$$
T\cap C^c
$$

means that the user received the tutorial but did not complete onboarding.

From the table, there are

$$
70
$$

such users. Therefore,

$$
P(T\cap C^c)=\frac{70}{500}.
$$

Simplifying:

$$
P(T\cap C^c)=\frac{7}{50}.
$$

Therefore,

$$
P(T\cap C^c)=0.14.
$$

---

The event

$$
T^c\cap C
$$

means that the user did not receive the tutorial but completed onboarding.

From the table, there are

$$
120
$$

such users. Therefore,

$$
P(T^c\cap C)=\frac{120}{500}.
$$

Simplifying:

$$
P(T^c\cap C)=\frac{6}{25}.
$$

Therefore,

$$
P(T^c\cap C)=0.24.
$$

---

The event

$$
T^c\cap C^c
$$

means that the user did not receive the tutorial and did not complete onboarding.

From the table, there are

$$
130
$$

such users. Therefore,

$$
P(T^c\cap C^c)=\frac{130}{500}.
$$

Simplifying:

$$
P(T^c\cap C^c)=\frac{13}{50}.
$$

Therefore,

$$
P(T^c\cap C^c)=0.26.
$$

Now check that the four probabilities add up to 1:

$$
0.36+0.14+0.24+0.26=1.
$$

So the four regions cover the whole sample space.

## 2. Computing \(P(T)\), \(P(C)\), and \(P(T\cup C)\)

First, compute

$$
P(T).
$$

The event

$$
T
$$

contains the regions

$$
T\cap C
$$

and

$$
T\cap C^c.
$$

Therefore,

$$
P(T)=P(T\cap C)+P(T\cap C^c).
$$

Substituting the values:

$$
P(T)=0.36+0.14.
$$

Adding:

$$
P(T)=0.50.
$$

So,

$$
P(T)=0.50.
$$

---

Now compute

$$
P(C).
$$

The event

$$
C
$$

contains the regions

$$
T\cap C
$$

and

$$
T^c\cap C.
$$

Therefore,

$$
P(C)=P(T\cap C)+P(T^c\cap C).
$$

Substituting the values:

$$
P(C)=0.36+0.24.
$$

Adding:

$$
P(C)=0.60.
$$

So,

$$
P(C)=0.60.
$$

---

Now compute

$$
P(T\cup C).
$$

The event

$$
T\cup C
$$

means that the user received the tutorial, completed onboarding, or both.

Using the four regions,

$$
P(T\cup C)=P(T\cap C)+P(T\cap C^c)+P(T^c\cap C).
$$

Substituting the values:

$$
P(T\cup C)=0.36+0.14+0.24.
$$

Adding:

$$
P(T\cup C)=0.74.
$$

So,

$$
P(T\cup C)=0.74.
$$

We can also compute this using the inclusion--exclusion formula:

$$
P(T\cup C)=P(T)+P(C)-P(T\cap C).
$$

Substituting the values:

$$
P(T\cup C)=0.50+0.60-0.36.
$$

Therefore,

$$
P(T\cup C)=0.74.
$$

## 3. Computing \(P(C\mid T)\) and \(P(C\mid T^c)\)

First, compute

$$
P(C\mid T).
$$

The conditional probability formula is

$$
P(C\mid T)=\frac{P(T\cap C)}{P(T)}.
$$

Using the original counts:

$$
P(C\mid T)=\frac{180}{250}.
$$

Simplifying:

$$
P(C\mid T)=\frac{18}{25}.
$$

Therefore,

$$
P(C\mid T)=0.72.
$$

This means that among users who received the tutorial,

$$
72\%
$$

completed onboarding.

---

Now compute

$$
P(C\mid T^c).
$$

The event

$$
T^c
$$

means that the user did not receive the tutorial.

Using the original counts:

$$
P(C\mid T^c)=\frac{120}{250}.
$$

Simplifying:

$$
P(C\mid T^c)=\frac{12}{25}.
$$

Therefore,

$$
P(C\mid T^c)=0.48.
$$

This means that among users who did not receive the tutorial,

$$
48\%
$$

completed onboarding.

## 4. Computing \(P(T\mid C)\) and \(P(T\mid C^c)\)

First, compute

$$
P(T\mid C).
$$

The conditional probability formula is

$$
P(T\mid C)=\frac{P(T\cap C)}{P(C)}.
$$

Using the original counts:

$$
P(T\mid C)=\frac{180}{300}.
$$

Simplifying:

$$
P(T\mid C)=\frac{3}{5}.
$$

Therefore,

$$
P(T\mid C)=0.60.
$$

This means that among users who completed onboarding,

$$
60\%
$$

received the tutorial.

---

Now compute

$$
P(T\mid C^c).
$$

The event

$$
C^c
$$

means that the user did not complete onboarding.

Using the original counts:

$$
P(T\mid C^c)=\frac{70}{200}.
$$

Simplifying:

$$
P(T\mid C^c)=\frac{7}{20}.
$$

Therefore,

$$
P(T\mid C^c)=0.35.
$$

This means that among users who did not complete onboarding,

$$
35\%
$$

received the tutorial.

## 5. Are \(T\) and \(C\) independent?

Two events are independent if

$$
P(T\cap C)=P(T)P(C).
$$

We know that

$$
P(T\cap C)=0.36,
$$

$$
P(T)=0.50,
$$

and

$$
P(C)=0.60.
$$

Now compute

$$
P(T)P(C).
$$

Substituting the values:

$$
P(T)P(C)=0.50\cdot 0.60.
$$

Multiplying:

$$
P(T)P(C)=0.30.
$$

But

$$
P(T\cap C)=0.36.
$$

Since

$$
0.36\neq 0.30,
$$

the events are not independent.

Therefore,

$$
T \text{ and } C \text{ are not independent.}
$$

We can also check independence using conditional probability.

If \(T\) and \(C\) were independent, then

$$
P(C\mid T)=P(C).
$$

But

$$
P(C\mid T)=0.72
$$

and

$$
P(C)=0.60.
$$

Since

$$
0.72\neq 0.60,
$$

the events are not independent.

## 6. Does receiving the tutorial appear to change the probability of completing onboarding?

Yes, receiving the tutorial appears to change the probability of completing onboarding.

With tutorial:

$$
P(C\mid T)=0.72.
$$

Without tutorial:

$$
P(C\mid T^c)=0.48.
$$

Since

$$
0.72>0.48,
$$

users who received the tutorial have a higher probability of completing onboarding.

The difference is

$$
0.72-0.48=0.24.
$$

So receiving the tutorial increases the completion probability by

$$
24
$$

percentage points.

## 7. Difference between \(P(C\mid T)\) and \(P(T\mid C)\)

The probability

$$
P(C\mid T)
$$

means:

$$
\text{among users who received the tutorial, what is the probability that they completed onboarding?}
$$

We found that

$$
P(C\mid T)=0.72.
$$

So among users who received the tutorial,

$$
72\%
$$

completed onboarding.

---

The probability

$$
P(T\mid C)
$$

means:

$$
\text{among users who completed onboarding, what is the probability that they received the tutorial?}
$$

We found that

$$
P(T\mid C)=0.60.
$$

So among users who completed onboarding,

$$
60\%
$$

received the tutorial.

These two probabilities are different because the condition is different.

In general,

$$
P(C\mid T)\neq P(T\mid C).
$$

## 8. Short interpretation of the result in words

The data suggest that receiving the tutorial is associated with a higher probability of completing onboarding.

Among users who received the tutorial,

$$
72\%
$$

completed onboarding.

Among users who did not receive the tutorial,

$$
48\%
$$

completed onboarding.

Therefore, the tutorial appears to have a positive effect on onboarding completion.

Also, the events are not independent because receiving the tutorial changes the probability of completing onboarding.

## Final Answers

$$
P(T\cap C)=\frac{180}{500}=0.36
$$

$$
P(T\cap C^c)=\frac{70}{500}=0.14
$$

$$
P(T^c\cap C)=\frac{120}{500}=0.24
$$

$$
P(T^c\cap C^c)=\frac{130}{500}=0.26
$$

$$
P(T)=0.36+0.14=0.50
$$

$$
P(C)=0.36+0.24=0.60
$$

$$
P(T\cup C)=0.36+0.14+0.24=0.74
$$

$$
P(C\mid T)=\frac{180}{250}=0.72
$$

$$
P(C\mid T^c)=\frac{120}{250}=0.48
$$

$$
P(T\mid C)=\frac{180}{300}=0.60
$$

$$
P(T\mid C^c)=\frac{70}{200}=0.35
$$

Since

$$
P(T\cap C)\neq P(T)P(C),
$$

because

$$
0.36\neq 0.50\cdot 0.60,
$$

the events are not independent.

Receiving the tutorial appears to increase the probability of completing onboarding because

$$
P(C\mid T)=0.72>0.48=P(C\mid T^c).
$$