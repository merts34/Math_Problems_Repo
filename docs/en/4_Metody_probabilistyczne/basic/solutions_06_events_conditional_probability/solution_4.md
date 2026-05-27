# Problem 4 — Inclusion--Exclusion and Double Counting

A company surveyed 200 employees about two software tools.

Let

$$
A=\text{the employee uses Tool A}
$$

and

$$
B=\text{the employee uses Tool B}.
$$

The total number of employees is

$$
200.
$$

From the question, we know that

$$
|A|=130,
$$

$$
|B|=90,
$$

and

$$
|A\cap B|=60.
$$

## 1. Computing \(P(A)\), \(P(B)\), and \(P(A\cap B)\)

The probability of using Tool A is

$$
P(A)=\frac{|A|}{200}.
$$

Substituting the value:

$$
P(A)=\frac{130}{200}.
$$

Simplifying:

$$
P(A)=\frac{13}{20}.
$$

Therefore,

$$
P(A)=0.65.
$$

---

The probability of using Tool B is

$$
P(B)=\frac{|B|}{200}.
$$

Substituting the value:

$$
P(B)=\frac{90}{200}.
$$

Simplifying:

$$
P(B)=\frac{9}{20}.
$$

Therefore,

$$
P(B)=0.45.
$$

---

The probability of using both tools is

$$
P(A\cap B)=\frac{|A\cap B|}{200}.
$$

Substituting the value:

$$
P(A\cap B)=\frac{60}{200}.
$$

Simplifying:

$$
P(A\cap B)=\frac{3}{10}.
$$

Therefore,

$$
P(A\cap B)=0.30.
$$

## 2. Computing \(P(A\cup B)\) using inclusion--exclusion

The inclusion--exclusion formula is

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B).
$$

Substituting the values:

$$
P(A\cup B)=0.65+0.45-0.30.
$$

First,

$$
0.65+0.45=1.10.
$$

Then,

$$
1.10-0.30=0.80.
$$

Therefore,

$$
P(A\cup B)=0.80.
$$

This means that

$$
80\%
$$

of the employees use Tool A, Tool B, or both.

## 3. Computing the three remaining regions

### Employees who use Tool A but not Tool B

The event

$$
A\setminus B
$$

means that the employee uses Tool A but does not use Tool B.

We compute it by subtracting the employees who use both tools from all employees who use Tool A:

$$
|A\setminus B|=|A|-|A\cap B|.
$$

Substituting the values:

$$
|A\setminus B|=130-60.
$$

Therefore,

$$
|A\setminus B|=70.
$$

So,

$$
P(A\setminus B)=\frac{70}{200}.
$$

Simplifying:

$$
P(A\setminus B)=\frac{7}{20}.
$$

Thus,

$$
P(A\setminus B)=0.35.
$$

---

### Employees who use Tool B but not Tool A

The event

$$
B\setminus A
$$

means that the employee uses Tool B but does not use Tool A.

We compute it by subtracting the employees who use both tools from all employees who use Tool B:

$$
|B\setminus A|=|B|-|A\cap B|.
$$

Substituting the values:

$$
|B\setminus A|=90-60.
$$

Therefore,

$$
|B\setminus A|=30.
$$

So,

$$
P(B\setminus A)=\frac{30}{200}.
$$

Simplifying:

$$
P(B\setminus A)=\frac{3}{20}.
$$

Thus,

$$
P(B\setminus A)=0.15.
$$

---

### Employees who use neither Tool A nor Tool B

The event

$$
A^c\cap B^c
$$

means that the employee uses neither Tool A nor Tool B.

First, we know that

$$
P(A\cup B)=0.80.
$$

Therefore,

$$
P(A^c\cap B^c)=1-P(A\cup B).
$$

Substituting the value:

$$
P(A^c\cap B^c)=1-0.80.
$$

Thus,

$$
P(A^c\cap B^c)=0.20.
$$

In terms of number of employees:

$$
0.20\cdot 200=40.
$$

So,

$$
40
$$

employees use neither tool.

## 4. Computing \(P(A\mid B)\) and \(P(B\mid A)\)

First, we compute

$$
P(A\mid B).
$$

The conditional probability formula is

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}.
$$

Substituting the values:

$$
P(A\mid B)=\frac{0.30}{0.45}.
$$

Using the original counts, this is the same as

$$
P(A\mid B)=\frac{60}{90}.
$$

Simplifying:

$$
P(A\mid B)=\frac{2}{3}.
$$

As a decimal,

$$
P(A\mid B)\approx 0.6667.
$$

So,

$$
P(A\mid B)\approx 0.6667.
$$

This means that among employees who use Tool B, about

$$
66.67\%
$$

also use Tool A.

---

Now, we compute

$$
P(B\mid A).
$$

The conditional probability formula is

$$
P(B\mid A)=\frac{P(A\cap B)}{P(A)}.
$$

Substituting the values:

$$
P(B\mid A)=\frac{0.30}{0.65}.
$$

Using the original counts, this is the same as

$$
P(B\mid A)=\frac{60}{130}.
$$

Simplifying:

$$
P(B\mid A)=\frac{6}{13}.
$$

As a decimal,

$$
P(B\mid A)\approx 0.4615.
$$

So,

$$
P(B\mid A)\approx 0.4615.
$$

This means that among employees who use Tool A, about

$$
46.15\%
$$

also use Tool B.

## 5. Why is \(P(A\cup B)\neq P(A)+P(B)\)?

If we simply add

$$
P(A)+P(B),
$$

then employees who use both Tool A and Tool B are counted twice.

We have

$$
P(A)+P(B)=0.65+0.45.
$$

Therefore,

$$
P(A)+P(B)=1.10.
$$

But a probability cannot exceed 1 for a union of events in this situation.

The reason this happened is double counting.

The correct formula is

$$
P(A\cup B)=P(A)+P(B)-P(A\cap B).
$$

Substituting the values:

$$
P(A\cup B)=0.65+0.45-0.30.
$$

Therefore,

$$
P(A\cup B)=0.80.
$$

So,

$$
P(A\cup B)\neq P(A)+P(B)
$$

because the overlap

$$
A\cap B
$$

must be subtracted once.

## 6. Which group is counted twice in \(P(A)+P(B)\)?

The group counted twice is

$$
A\cap B.
$$

This is the group of employees who use both Tool A and Tool B.

There are

$$
60
$$

employees in this group.

Their probability is

$$
P(A\cap B)=\frac{60}{200}=0.30.
$$

## Final Answers

$$
P(A)=\frac{130}{200}=0.65
$$

$$
P(B)=\frac{90}{200}=0.45
$$

$$
P(A\cap B)=\frac{60}{200}=0.30
$$

$$
P(A\cup B)=0.65+0.45-0.30=0.80
$$

$$
P(A\setminus B)=\frac{70}{200}=0.35
$$

$$
P(B\setminus A)=\frac{30}{200}=0.15
$$

$$
P(A^c\cap B^c)=\frac{40}{200}=0.20
$$

$$
P(A\mid B)=\frac{60}{90}=\frac{2}{3}\approx 0.6667
$$

$$
P(B\mid A)=\frac{60}{130}=\frac{6}{13}\approx 0.4615
$$

$$
P(A\cup B)\neq P(A)+P(B)
$$

because the group

$$
A\cap B
$$

is counted twice in

$$
P(A)+P(B).
$$