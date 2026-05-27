# Problem 5 — Independence from Data

A streaming platform records whether users have a premium account and whether they watched a movie during the last weekend.

Let

$$
A=\text{the user has a premium account}
$$

and

$$
M=\text{the user watched a movie during the weekend}.
$$

The total number of users is

$$
200.
$$

From the table, we have:

$$
|A|=120,
$$

$$
|A^c|=80,
$$

$$
|M|=140,
$$

$$
|M^c|=60,
$$

and

$$
|A\cap M|=84.
$$

## 1. Computing \(P(A)\), \(P(M)\), and \(P(A\cap M)\)

The probability that a user has a premium account is

$$
P(A)=\frac{|A|}{200}.
$$

Substituting the value:

$$
P(A)=\frac{120}{200}.
$$

Simplifying:

$$
P(A)=\frac{3}{5}.
$$

Therefore,

$$
P(A)=0.60.
$$

---

The probability that a user watched a movie during the weekend is

$$
P(M)=\frac{|M|}{200}.
$$

Substituting the value:

$$
P(M)=\frac{140}{200}.
$$

Simplifying:

$$
P(M)=\frac{7}{10}.
$$

Therefore,

$$
P(M)=0.70.
$$

---

The probability that a user has a premium account and watched a movie during the weekend is

$$
P(A\cap M)=\frac{|A\cap M|}{200}.
$$

Substituting the value:

$$
P(A\cap M)=\frac{84}{200}.
$$

Simplifying:

$$
P(A\cap M)=\frac{21}{50}.
$$

Therefore,

$$
P(A\cap M)=0.42.
$$

## 2. Computing \(P(M\mid A)\) and \(P(M\mid A^c)\)

First, we compute

$$
P(M\mid A).
$$

The conditional probability formula is

$$
P(M\mid A)=\frac{P(A\cap M)}{P(A)}.
$$

Using the original counts, this is

$$
P(M\mid A)=\frac{84}{120}.
$$

Simplifying:

$$
P(M\mid A)=\frac{7}{10}.
$$

Therefore,

$$
P(M\mid A)=0.70.
$$

This means that among premium users,

$$
70\%
$$

watched a movie during the weekend.

---

Now, we compute

$$
P(M\mid A^c).
$$

The event

$$
A^c
$$

means that the user does not have a premium account, so the user is a free user.

From the table, the number of free users who watched a movie is

$$
56.
$$

The total number of free users is

$$
80.
$$

Therefore,

$$
P(M\mid A^c)=\frac{56}{80}.
$$

Simplifying:

$$
P(M\mid A^c)=\frac{7}{10}.
$$

Therefore,

$$
P(M\mid A^c)=0.70.
$$

This means that among free users,

$$
70\%
$$

watched a movie during the weekend.

## 3. Deciding whether \(A\) and \(M\) are independent

Two events are independent if

$$
P(A\cap M)=P(A)P(M).
$$

We know that

$$
P(A)=0.60,
$$

$$
P(M)=0.70,
$$

and

$$
P(A\cap M)=0.42.
$$

Now compute

$$
P(A)P(M).
$$

Substituting the values:

$$
P(A)P(M)=0.60\cdot 0.70.
$$

Multiplying:

$$
P(A)P(M)=0.42.
$$

Since

$$
P(A\cap M)=0.42
$$

and

$$
P(A)P(M)=0.42,
$$

we have

$$
P(A\cap M)=P(A)P(M).
$$

Therefore,

$$
A \text{ and } M \text{ are independent.}
$$

We can also check independence by conditional probability.

If \(A\) and \(M\) are independent, then

$$
P(M\mid A)=P(M).
$$

We found that

$$
P(M\mid A)=0.70
$$

and

$$
P(M)=0.70.
$$

Since

$$
P(M\mid A)=P(M),
$$

this also shows that the events are independent.

Also,

$$
P(M\mid A^c)=0.70
$$

which is the same as

$$
P(M)=0.70.
$$

So having a premium account does not change the probability of watching a movie.

## 4. Explanation of independence in words

Independence means that knowing whether a user has a premium account does not change the probability that the user watched a movie during the weekend.

In this problem, premium users and free users have the same probability of watching a movie:

$$
P(M\mid A)=0.70
$$

and

$$
P(M\mid A^c)=0.70.
$$

Since both probabilities are equal, account type does not affect the probability of watching a movie during the weekend.

Therefore,

$$
A \text{ and } M \text{ are independent events.}
$$

## Final Answers

$$
P(A)=\frac{120}{200}=0.60
$$

$$
P(M)=\frac{140}{200}=0.70
$$

$$
P(A\cap M)=\frac{84}{200}=0.42
$$

$$
P(M\mid A)=\frac{84}{120}=0.70
$$

$$
P(M\mid A^c)=\frac{56}{80}=0.70
$$

Since

$$
P(A\cap M)=P(A)P(M),
$$

because

$$
0.42=0.60\cdot 0.70,
$$

the events are independent.

Therefore,

$$
A \text{ and } M \text{ are independent.}
$$