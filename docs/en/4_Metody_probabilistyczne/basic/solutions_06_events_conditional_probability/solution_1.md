# Problem 1 — Event Algebra from a Two-Way Table

A university collected data about students’ study habits.

Let

$$
A=\text{the student attends lectures regularly}
$$

and

$$
B=\text{the student submits homework on time}.
$$

The total number of students is

$$
100.
$$

## 1. Probabilities of the four disjoint regions

The event

$$
A\cap B
$$

means that the student attends lectures regularly and submits homework on time.

From the table, there are 48 such students. Therefore,

$$
P(A\cap B)=\frac{48}{100}=0.48.
$$

The event

$$
A\cap B^c
$$

means that the student attends lectures regularly but does not submit homework on time.

From the table, there are 12 such students. Therefore,

$$
P(A\cap B^c)=\frac{12}{100}=0.12.
$$

The event

$$
A^c\cap B
$$

means that the student does not attend lectures regularly but submits homework on time.

From the table, there are 22 such students. Therefore,

$$
P(A^c\cap B)=\frac{22}{100}=0.22.
$$

The event

$$
A^c\cap B^c
$$

means that the student does not attend lectures regularly and does not submit homework on time.

From the table, there are 18 such students. Therefore,

$$
P(A^c\cap B^c)=\frac{18}{100}=0.18.
$$

We can check that these four probabilities add up to 1:

$$
0.48+0.12+0.22+0.18=1.
$$

So these four regions form the whole sample space.

## 2. Computing \(P(A)\), \(P(B)\), and \(P(A\cup B)\)

The event

$$
A
$$

contains the regions

$$
A\cap B
$$

and

$$
A\cap B^c.
$$

Therefore,

$$
P(A)=P(A\cap B)+P(A\cap B^c).
$$

Substituting the values:

$$
P(A)=0.48+0.12.
$$

Thus,

$$
P(A)=0.60.
$$

Now, the event

$$
B
$$

contains the regions

$$
A\cap B
$$

and

$$
A^c\cap B.
$$

Therefore,

$$
P(B)=P(A\cap B)+P(A^c\cap B).
$$

Substituting the values:

$$
P(B)=0.48+0.22.
$$

Thus,

$$
P(B)=0.70.
$$

The event

$$
A\cup B
$$

means that the student attends lectures regularly, submits homework on time, or both.

Using the four regions, we have

$$
P(A\cup B)=P(A\cap B)+P(A\cap B^c)+P(A^c\cap B).
$$

Substituting the values:

$$
P(A\cup B)=0.48+0.12+0.22.
$$

Thus,

$$
P(A\cup B)=0.82.
$$

We can also compute it using the inclusion-exclusion formula:

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B).
$$

Substituting the values:

$$
P(A\cup B)=0.60+0.70-0.48.
$$

Therefore,

$$
P(A\cup B)=0.82.
$$

## 3. Computing \(P(A\mid B)\) and \(P(B\mid A)\)

The conditional probability formula is

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}.
$$

Substituting the values:

$$
P(A\mid B)=\frac{0.48}{0.70}.
$$

Since

$$
0.48=\frac{48}{100}
$$

and

$$
0.70=\frac{70}{100},
$$

we get

$$
P(A\mid B)=\frac{48}{70}.
$$

Simplifying the fraction:

$$
P(A\mid B)=\frac{24}{35}.
$$

As a decimal,

$$
P(A\mid B)\approx 0.6857.
$$

So,

$$
P(A\mid B)\approx 0.6857.
$$

Now we compute

$$
P(B\mid A).
$$

Using the conditional probability formula:

$$
P(B\mid A)=\frac{P(A\cap B)}{P(A)}.
$$

Substituting the values:

$$
P(B\mid A)=\frac{0.48}{0.60}.
$$

Since

$$
0.48=\frac{48}{100}
$$

and

$$
0.60=\frac{60}{100},
$$

we get

$$
P(B\mid A)=\frac{48}{60}.
$$

Simplifying:

$$
P(B\mid A)=\frac{4}{5}.
$$

Therefore,

$$
P(B\mid A)=0.80.
$$

## 4. Are \(A\) and \(B\) mutually exclusive?

Two events are mutually exclusive if they cannot happen at the same time.

Mathematically, this means

$$
P(A\cap B)=0.
$$

However, in this problem,

$$
P(A\cap B)=0.48.
$$

Since

$$
0.48\neq 0,
$$

the events are not mutually exclusive.

Therefore,

$$
A \text{ and } B \text{ are not mutually exclusive.}
$$

This is because there are students who both attend lectures regularly and submit homework on time.

## 5. Are \(A\) and \(B\) independent?

Two events are independent if

$$
P(A\cap B)=P(A)P(B).
$$

We know that

$$
P(A\cap B)=0.48,
$$

$$
P(A)=0.60,
$$

and

$$
P(B)=0.70.
$$

Now compute

$$
P(A)P(B).
$$

Substituting the values:

$$
P(A)P(B)=0.60\cdot 0.70.
$$

Multiplying:

$$
P(A)P(B)=0.42.
$$

But

$$
P(A\cap B)=0.48.
$$

Since

$$
0.48\neq 0.42,
$$

the events are not independent.

Therefore,

$$
A \text{ and } B \text{ are not independent.}
$$

## 6. Interpretation of \(P(A\mid B)\) and \(P(B\mid A)\)

We found that

$$
P(A\mid B)\approx 0.6857.
$$

This means that among students who submit homework on time, about

$$
68.57\%
$$

attend lectures regularly.

We also found that

$$
P(B\mid A)=0.80.
$$

This means that among students who attend lectures regularly,

$$
80\%
$$

submit homework on time.

## Final Answers

$$
P(A\cap B)=0.48
$$

$$
P(A\cap B^c)=0.12
$$

$$
P(A^c\cap B)=0.22
$$

$$
P(A^c\cap B^c)=0.18
$$

$$
P(A)=0.60
$$

$$
P(B)=0.70
$$

$$
P(A\cup B)=0.82
$$

$$
P(A\mid B)\approx 0.6857
$$

$$
P(B\mid A)=0.80
$$

$$
A \text{ and } B \text{ are not mutually exclusive.}
$$

$$
A \text{ and } B \text{ are not independent.}
$$