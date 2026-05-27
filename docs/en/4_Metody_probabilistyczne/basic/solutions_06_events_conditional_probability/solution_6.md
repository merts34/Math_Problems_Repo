# Problem 6 — Dependence from Data

A delivery company records whether a parcel is international and whether it is delayed.

Let

$$
I=\text{the parcel is international}
$$

and

$$
D=\text{the parcel is delayed}.
$$

The total number of parcels is

$$
600.
$$

From the table, we have:

$$
|I|=200,
$$

$$
|I^c|=400,
$$

$$
|D|=60,
$$

$$
|D^c|=540,
$$

and

$$
|I\cap D|=36.
$$

## 1. Computing \(P(I)\), \(P(D)\), and \(P(I\cap D)\)

The probability that a parcel is international is

$$
P(I)=\frac{|I|}{600}.
$$

Substituting the value:

$$
P(I)=\frac{200}{600}.
$$

Simplifying:

$$
P(I)=\frac{1}{3}.
$$

As a decimal,

$$
P(I)\approx 0.3333.
$$

---

The probability that a parcel is delayed is

$$
P(D)=\frac{|D|}{600}.
$$

Substituting the value:

$$
P(D)=\frac{60}{600}.
$$

Simplifying:

$$
P(D)=\frac{1}{10}.
$$

Therefore,

$$
P(D)=0.10.
$$

---

The probability that a parcel is international and delayed is

$$
P(I\cap D)=\frac{|I\cap D|}{600}.
$$

Substituting the value:

$$
P(I\cap D)=\frac{36}{600}.
$$

Simplifying:

$$
P(I\cap D)=\frac{3}{50}.
$$

Therefore,

$$
P(I\cap D)=0.06.
$$

## 2. Computing \(P(D\mid I)\) and \(P(D\mid I^c)\)

First, we compute

$$
P(D\mid I).
$$

The conditional probability formula is

$$
P(D\mid I)=\frac{P(I\cap D)}{P(I)}.
$$

Using the original counts, this is

$$
P(D\mid I)=\frac{36}{200}.
$$

Simplifying:

$$
P(D\mid I)=\frac{9}{50}.
$$

Therefore,

$$
P(D\mid I)=0.18.
$$

This means that among international parcels,

$$
18\%
$$

are delayed.

---

Now, we compute

$$
P(D\mid I^c).
$$

The event

$$
I^c
$$

means that the parcel is not international, so the parcel is domestic.

From the table, the number of domestic parcels that are delayed is

$$
24.
$$

The total number of domestic parcels is

$$
400.
$$

Therefore,

$$
P(D\mid I^c)=\frac{24}{400}.
$$

Simplifying:

$$
P(D\mid I^c)=\frac{3}{50}.
$$

Therefore,

$$
P(D\mid I^c)=0.06.
$$

This means that among domestic parcels,

$$
6\%
$$

are delayed.

## 3. Are \(I\) and \(D\) independent?

Two events are independent if

$$
P(I\cap D)=P(I)P(D).
$$

We know that

$$
P(I)=\frac{1}{3},
$$

$$
P(D)=0.10,
$$

and

$$
P(I\cap D)=0.06.
$$

Now compute

$$
P(I)P(D).
$$

Substituting the values:

$$
P(I)P(D)=\frac{1}{3}\cdot 0.10.
$$

Since

$$
0.10=\frac{1}{10},
$$

we get

$$
P(I)P(D)=\frac{1}{3}\cdot \frac{1}{10}.
$$

Multiplying:

$$
P(I)P(D)=\frac{1}{30}.
$$

As a decimal,

$$
P(I)P(D)\approx 0.0333.
$$

But

$$
P(I\cap D)=0.06.
$$

Since

$$
0.06\neq 0.0333,
$$

the events are not independent.

Therefore,

$$
I \text{ and } D \text{ are not independent.}
$$

We can also check independence using conditional probability.

If \(I\) and \(D\) were independent, then

$$
P(D\mid I)=P(D).
$$

However,

$$
P(D\mid I)=0.18
$$

and

$$
P(D)=0.10.
$$

Since

$$
0.18\neq 0.10,
$$

the events are not independent.

## 4. Does international shipping increase the probability of delay?

Yes, international shipping increases the probability of delay.

For international parcels,

$$
P(D\mid I)=0.18.
$$

For domestic parcels,

$$
P(D\mid I^c)=0.06.
$$

Since

$$
0.18>0.06,
$$

international parcels have a higher probability of being delayed.

The increase is

$$
0.18-0.06=0.12.
$$

So international shipping increases the delay probability by

$$
12
$$

percentage points.

## 5. Computing \(P(I\mid D)\)

Now we compute

$$
P(I\mid D).
$$

The conditional probability formula is

$$
P(I\mid D)=\frac{P(I\cap D)}{P(D)}.
$$

Using the original counts, this is

$$
P(I\mid D)=\frac{36}{60}.
$$

Simplifying:

$$
P(I\mid D)=\frac{3}{5}.
$$

Therefore,

$$
P(I\mid D)=0.60.
$$

This means that among delayed parcels,

$$
60\%
$$

are international.

## 6. Difference between \(P(D\mid I)\) and \(P(I\mid D)\)

The probability

$$
P(D\mid I)
$$

means:

$$
\text{among international parcels, what is the probability that the parcel is delayed?}
$$

We found that

$$
P(D\mid I)=0.18.
$$

So among international parcels,

$$
18\%
$$

are delayed.

---

The probability

$$
P(I\mid D)
$$

means:

$$
\text{among delayed parcels, what is the probability that the parcel is international?}
$$

We found that

$$
P(I\mid D)=0.60.
$$

So among delayed parcels,

$$
60\%
$$

are international.

These two probabilities are different because the condition is different.

In general,

$$
P(D\mid I)\neq P(I\mid D).
$$

## Final Answers

$$
P(I)=\frac{200}{600}=\frac{1}{3}\approx 0.3333
$$

$$
P(D)=\frac{60}{600}=0.10
$$

$$
P(I\cap D)=\frac{36}{600}=0.06
$$

$$
P(D\mid I)=\frac{36}{200}=0.18
$$

$$
P(D\mid I^c)=\frac{24}{400}=0.06
$$

Since

$$
P(D\mid I)\neq P(D),
$$

because

$$
0.18\neq 0.10,
$$

the events are not independent.

Therefore,

$$
I \text{ and } D \text{ are not independent.}
$$

International shipping increases the probability of delay because

$$
P(D\mid I)=0.18>0.06=P(D\mid I^c).
$$

Also,

$$
P(I\mid D)=\frac{36}{60}=0.60.
$$

Finally,

$$
P(D\mid I)
$$

and

$$
P(I\mid D)
$$

are different because they condition on different events.