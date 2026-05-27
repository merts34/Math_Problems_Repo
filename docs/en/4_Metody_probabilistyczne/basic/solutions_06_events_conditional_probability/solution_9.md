# Problem 9 — Law of Total Probability Without a Full Table

A company receives orders through three channels:

- website,
- mobile app,
- phone.

Let

$$
W=\text{the order came through the website}
$$

$$
A=\text{the order came through the mobile app}
$$

$$
H=\text{the order came by phone}
$$

and

$$
C=\text{the order is cancelled}.
$$

We are given:

$$
P(W)=0.50,
$$

$$
P(A)=0.35,
$$

$$
P(H)=0.15.
$$

Also,

$$
P(C\mid W)=0.04,
$$

$$
P(C\mid A)=0.06,
$$

and

$$
P(C\mid H)=0.10.
$$

## 1. Why do \(W\), \(A\), and \(H\) form a partition of the sample space?

The events

$$
W,\quad A,\quad H
$$

form a partition of the sample space because every order comes from exactly one channel.

An order cannot come from the website, mobile app, and phone at the same time.

So the events are mutually exclusive:

$$
W\cap A=\varnothing,
$$

$$
W\cap H=\varnothing,
$$

and

$$
A\cap H=\varnothing.
$$

Also, together they cover the whole sample space:

$$
W\cup A\cup H=\Omega.
$$

We can check this using the probabilities:

$$
P(W)+P(A)+P(H)=0.50+0.35+0.15.
$$

Adding:

$$
P(W)+P(A)+P(H)=1.
$$

Therefore,

$$
W,\ A,\ \text{and } H
$$

form a partition of the sample space.

## 2. Using the law of total probability to compute \(P(C)\)

Since

$$
W,\quad A,\quad H
$$

form a partition of the sample space, we can use the law of total probability:

$$
P(C)=P(C\mid W)P(W)+P(C\mid A)P(A)+P(C\mid H)P(H).
$$

Substituting the values:

$$
P(C)=0.04\cdot 0.50+0.06\cdot 0.35+0.10\cdot 0.15.
$$

Now compute each term separately:

$$
0.04\cdot 0.50=0.020,
$$

$$
0.06\cdot 0.35=0.021,
$$

and

$$
0.10\cdot 0.15=0.015.
$$

Therefore,

$$
P(C)=0.020+0.021+0.015.
$$

Adding:

$$
P(C)=0.056.
$$

So the overall probability that an order is cancelled is

$$
P(C)=0.056.
$$

As a percentage,

$$
P(C)=5.6\%.
$$

## 3. Computing \(P(W\mid C)\), \(P(A\mid C)\), and \(P(H\mid C)\)

We use Bayes' formula.

First, compute

$$
P(W\mid C).
$$

Bayes' formula gives:

$$
P(W\mid C)=\frac{P(C\mid W)P(W)}{P(C)}.
$$

Substituting the values:

$$
P(W\mid C)=\frac{0.04\cdot 0.50}{0.056}.
$$

First compute the numerator:

$$
0.04\cdot 0.50=0.020.
$$

So,

$$
P(W\mid C)=\frac{0.020}{0.056}.
$$

To simplify, multiply numerator and denominator by 1000:

$$
P(W\mid C)=\frac{20}{56}.
$$

Simplifying:

$$
P(W\mid C)=\frac{5}{14}.
$$

As a decimal,

$$
P(W\mid C)\approx 0.3571.
$$

So, among cancelled orders, about

$$
35.71\%
$$

came through the website.

---

Now compute

$$
P(A\mid C).
$$

Bayes' formula gives:

$$
P(A\mid C)=\frac{P(C\mid A)P(A)}{P(C)}.
$$

Substituting the values:

$$
P(A\mid C)=\frac{0.06\cdot 0.35}{0.056}.
$$

First compute the numerator:

$$
0.06\cdot 0.35=0.021.
$$

So,

$$
P(A\mid C)=\frac{0.021}{0.056}.
$$

To simplify, multiply numerator and denominator by 1000:

$$
P(A\mid C)=\frac{21}{56}.
$$

As a decimal,

$$
P(A\mid C)=0.375.
$$

So, among cancelled orders,

$$
37.5\%
$$

came through the mobile app.

---

Now compute

$$
P(H\mid C).
$$

Bayes' formula gives:

$$
P(H\mid C)=\frac{P(C\mid H)P(H)}{P(C)}.
$$

Substituting the values:

$$
P(H\mid C)=\frac{0.10\cdot 0.15}{0.056}.
$$

First compute the numerator:

$$
0.10\cdot 0.15=0.015.
$$

So,

$$
P(H\mid C)=\frac{0.015}{0.056}.
$$

To simplify, multiply numerator and denominator by 1000:

$$
P(H\mid C)=\frac{15}{56}.
$$

As a decimal,

$$
P(H\mid C)\approx 0.2679.
$$

So, among cancelled orders, about

$$
26.79\%
$$

came by phone.

We can check that these conditional probabilities add up to 1:

$$
P(W\mid C)+P(A\mid C)+P(H\mid C)
$$

$$
=\frac{20}{56}+\frac{21}{56}+\frac{15}{56}
$$

$$
=\frac{56}{56}
$$

$$
=1.
$$

## 4. Which channel is most likely among cancelled orders?

We compare:

$$
P(W\mid C)\approx 0.3571,
$$

$$
P(A\mid C)=0.375,
$$

and

$$
P(H\mid C)\approx 0.2679.
$$

The largest probability is

$$
P(A\mid C)=0.375.
$$

Therefore, among cancelled orders, the most likely channel is the mobile app.

## 5. Is this necessarily the channel with the highest cancellation rate?

No, this is not necessarily the channel with the highest cancellation rate.

The cancellation rates are:

$$
P(C\mid W)=0.04,
$$

$$
P(C\mid A)=0.06,
$$

and

$$
P(C\mid H)=0.10.
$$

The highest cancellation rate is for phone orders:

$$
P(C\mid H)=0.10.
$$

However, phone orders make up only

$$
P(H)=0.15
$$

of all orders.

Mobile app orders have a lower cancellation rate:

$$
P(C\mid A)=0.06,
$$

but they make up a larger part of all orders:

$$
P(A)=0.35.
$$

Therefore, among cancelled orders, the most likely channel can be mobile app even though phone has the highest cancellation rate.

This happens because

$$
P(\text{channel}\mid C)
$$

depends on both:

$$
P(C\mid \text{channel})
$$

and

$$
P(\text{channel}).
$$

So the channel with the highest cancellation rate is not necessarily the most common channel among cancelled orders.

## Final Answers

$$
P(C)=P(C\mid W)P(W)+P(C\mid A)P(A)+P(C\mid H)P(H)
$$

$$
P(C)=0.04\cdot 0.50+0.06\cdot 0.35+0.10\cdot 0.15
$$

$$
P(C)=0.020+0.021+0.015
$$

$$
P(C)=0.056
$$

$$
P(W\mid C)=\frac{0.04\cdot 0.50}{0.056}
$$

$$
P(W\mid C)=\frac{0.020}{0.056}
$$

$$
P(W\mid C)=\frac{20}{56}=\frac{5}{14}\approx 0.3571
$$

$$
P(A\mid C)=\frac{0.06\cdot 0.35}{0.056}
$$

$$
P(A\mid C)=\frac{0.021}{0.056}
$$

$$
P(A\mid C)=\frac{21}{56}=0.375
$$

$$
P(H\mid C)=\frac{0.10\cdot 0.15}{0.056}
$$

$$
P(H\mid C)=\frac{0.015}{0.056}
$$

$$
P(H\mid C)=\frac{15}{56}\approx 0.2679
$$

Therefore, among cancelled orders, the most likely channel is

$$
A,
$$

which means the mobile app.

The channel with the highest cancellation rate is phone because

$$
P(C\mid H)=0.10.
$$

However, phone is not the most likely channel among cancelled orders because phone orders are only

$$
P(H)=0.15
$$

of all orders.