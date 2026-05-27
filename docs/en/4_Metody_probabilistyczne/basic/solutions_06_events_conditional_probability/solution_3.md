# Problem 3 — Conditional Probabilities Are Not Symmetric

An online course platform records whether users watched a lecture and whether they passed a quiz.

Let

$$
W=\text{the user watched the lecture}
$$

and

$$
Q=\text{the user passed the quiz}.
$$

The total number of users is

$$
150.
$$

From the table, we have:

$$
W\cap Q=72
$$

$$
W\cap Q^c=18
$$

$$
W^c\cap Q=28
$$

$$
W^c\cap Q^c=32
$$

Also,

$$
W=90
$$

$$
W^c=60
$$

$$
Q=100
$$

$$
Q^c=50.
$$

## 1. Computing \(P(Q\mid W)\) and \(P(W\mid Q)\)

First, we compute

$$
P(Q\mid W).
$$

The conditional probability formula is

$$
P(Q\mid W)=\frac{P(W\cap Q)}{P(W)}.
$$

From the table,

$$
P(W\cap Q)=\frac{72}{150}
$$

and

$$
P(W)=\frac{90}{150}.
$$

Therefore,

$$
P(Q\mid W)=\frac{\frac{72}{150}}{\frac{90}{150}}.
$$

The denominators cancel:

$$
P(Q\mid W)=\frac{72}{90}.
$$

Simplifying:

$$
P(Q\mid W)=\frac{4}{5}.
$$

Thus,

$$
P(Q\mid W)=0.80.
$$

So, among users who watched the lecture, the probability of passing the quiz is

$$
0.80.
$$

---

Now, we compute

$$
P(W\mid Q).
$$

The conditional probability formula is

$$
P(W\mid Q)=\frac{P(W\cap Q)}{P(Q)}.
$$

From the table,

$$
P(W\cap Q)=\frac{72}{150}
$$

and

$$
P(Q)=\frac{100}{150}.
$$

Therefore,

$$
P(W\mid Q)=\frac{\frac{72}{150}}{\frac{100}{150}}.
$$

The denominators cancel:

$$
P(W\mid Q)=\frac{72}{100}.
$$

Simplifying:

$$
P(W\mid Q)=\frac{18}{25}.
$$

Thus,

$$
P(W\mid Q)=0.72.
$$

So, among users who passed the quiz, the probability that they watched the lecture is

$$
0.72.
$$

## 2. Computing \(P(Q\mid W^c)\) and \(P(W\mid Q^c)\)

First, we compute

$$
P(Q\mid W^c).
$$

The conditional probability formula is

$$
P(Q\mid W^c)=\frac{P(W^c\cap Q)}{P(W^c)}.
$$

From the table,

$$
P(W^c\cap Q)=\frac{28}{150}
$$

and

$$
P(W^c)=\frac{60}{150}.
$$

Therefore,

$$
P(Q\mid W^c)=\frac{\frac{28}{150}}{\frac{60}{150}}.
$$

The denominators cancel:

$$
P(Q\mid W^c)=\frac{28}{60}.
$$

Simplifying:

$$
P(Q\mid W^c)=\frac{7}{15}.
$$

As a decimal,

$$
P(Q\mid W^c)\approx 0.4667.
$$

So, among users who did not watch the lecture, the probability of passing the quiz is approximately

$$
0.4667.
$$

---

Now, we compute

$$
P(W\mid Q^c).
$$

The conditional probability formula is

$$
P(W\mid Q^c)=\frac{P(W\cap Q^c)}{P(Q^c)}.
$$

From the table,

$$
P(W\cap Q^c)=\frac{18}{150}
$$

and

$$
P(Q^c)=\frac{50}{150}.
$$

Therefore,

$$
P(W\mid Q^c)=\frac{\frac{18}{150}}{\frac{50}{150}}.
$$

The denominators cancel:

$$
P(W\mid Q^c)=\frac{18}{50}.
$$

Simplifying:

$$
P(W\mid Q^c)=\frac{9}{25}.
$$

Thus,

$$
P(W\mid Q^c)=0.36.
$$

So, among users who did not pass the quiz, the probability that they watched the lecture is

$$
0.36.
$$

## 3. Why do \(P(Q\mid W)\) and \(P(W\mid Q)\) answer different questions?

The probability

$$
P(Q\mid W)
$$

means:

$$
\text{among users who watched the lecture, what is the probability that they passed the quiz?}
$$

This probability focuses on the users who watched the lecture.

On the other hand,

$$
P(W\mid Q)
$$

means:

$$
\text{among users who passed the quiz, what is the probability that they watched the lecture?}
$$

This probability focuses on the users who passed the quiz.

Therefore, these two probabilities are different because their conditions are different.

In general,

$$
P(Q\mid W)\neq P(W\mid Q).
$$

## 4. Which probability is more useful if we want to know whether watching the lecture helps?

If we want to know whether watching the lecture helps, we should compare the probability of passing for users who watched the lecture with the probability of passing for users who did not watch the lecture.

So we compare:

$$
P(Q\mid W)
$$

and

$$
P(Q\mid W^c).
$$

We found that

$$
P(Q\mid W)=0.80
$$

and

$$
P(Q\mid W^c)\approx 0.4667.
$$

Since

$$
0.80>0.4667,
$$

users who watched the lecture had a higher probability of passing the quiz.

Therefore, the most useful probability for checking whether watching helps is

$$
P(Q\mid W).
$$

More completely, we should compare

$$
P(Q\mid W)
$$

with

$$
P(Q\mid W^c).
$$

## 5. Which probability is more useful if we want to describe users who passed the quiz?

If we want to describe users who passed the quiz, we should look at users in the group

$$
Q.
$$

Therefore, the useful probability is

$$
P(W\mid Q).
$$

We found that

$$
P(W\mid Q)=0.72.
$$

This means that among users who passed the quiz,

$$
72\%
$$

watched the lecture.

## Final Answers

$$
P(Q\mid W)=\frac{72}{90}=0.80
$$

$$
P(W\mid Q)=\frac{72}{100}=0.72
$$

$$
P(Q\mid W^c)=\frac{28}{60}=\frac{7}{15}\approx 0.4667
$$

$$
P(W\mid Q^c)=\frac{18}{50}=0.36
$$

$$
P(Q\mid W)\neq P(W\mid Q)
$$

because they answer different conditional questions.

To know whether watching the lecture helps, we should compare

$$
P(Q\mid W)
$$

and

$$
P(Q\mid W^c).
$$

To describe users who passed the quiz, we should use

$$
P(W\mid Q).
$$