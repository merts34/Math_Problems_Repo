# Problem 2 — Four Regions of a Sample Space

A company classifies support tickets according to two properties:

- whether the ticket is technical,
- whether the ticket was solved during the first contact.

Let

$$
T=\text{the ticket is technical}
$$

and

$$
S=\text{the ticket was solved during the first contact}.
$$

The total number of tickets is

$$
350.
$$

## 1. Probabilities of the four disjoint regions

The event

$$
T\cap S
$$

means that the ticket is technical and was solved during the first contact.

From the table, there are 90 such tickets. Therefore,

$$
P(T\cap S)=\frac{90}{350}.
$$

Simplifying:

$$
P(T\cap S)=\frac{9}{35}.
$$

As a decimal,

$$
P(T\cap S)\approx 0.2571.
$$

---

The event

$$
T\cap S^c
$$

means that the ticket is technical and was not solved during the first contact.

From the table, there are 60 such tickets. Therefore,

$$
P(T\cap S^c)=\frac{60}{350}.
$$

Simplifying:

$$
P(T\cap S^c)=\frac{6}{35}.
$$

As a decimal,

$$
P(T\cap S^c)\approx 0.1714.
$$

---

The event

$$
T^c\cap S
$$

means that the ticket is not technical and was solved during the first contact.

From the table, there are 160 such tickets. Therefore,

$$
P(T^c\cap S)=\frac{160}{350}.
$$

Simplifying:

$$
P(T^c\cap S)=\frac{16}{35}.
$$

As a decimal,

$$
P(T^c\cap S)\approx 0.4571.
$$

---

The event

$$
T^c\cap S^c
$$

means that the ticket is not technical and was not solved during the first contact.

From the table, there are 40 such tickets. Therefore,

$$
P(T^c\cap S^c)=\frac{40}{350}.
$$

Simplifying:

$$
P(T^c\cap S^c)=\frac{4}{35}.
$$

As a decimal,

$$
P(T^c\cap S^c)\approx 0.1143.
$$

## 2. Verification that the four probabilities add up to 1

Now we add the four probabilities:

$$
P(T\cap S)+P(T\cap S^c)+P(T^c\cap S)+P(T^c\cap S^c)
$$

Substituting the values:

$$
\frac{90}{350}+\frac{60}{350}+\frac{160}{350}+\frac{40}{350}
$$

Adding the numerators:

$$
\frac{90+60+160+40}{350}
$$

$$
\frac{350}{350}=1.
$$

Therefore,

$$
P(T\cap S)+P(T\cap S^c)+P(T^c\cap S)+P(T^c\cap S^c)=1.
$$

So these four disjoint regions cover the whole sample space.

## 3. Computing \(P(T\cup S)\) and \(P(T^c\cup S)\)

The event

$$
T\cup S
$$

means that the ticket is technical, solved during the first contact, or both.

Using the four regions,

$$
P(T\cup S)=P(T\cap S)+P(T\cap S^c)+P(T^c\cap S).
$$

Substituting the values:

$$
P(T\cup S)=\frac{90}{350}+\frac{60}{350}+\frac{160}{350}.
$$

Adding the numerators:

$$
P(T\cup S)=\frac{90+60+160}{350}.
$$

$$
P(T\cup S)=\frac{310}{350}.
$$

Simplifying:

$$
P(T\cup S)=\frac{31}{35}.
$$

As a decimal,

$$
P(T\cup S)\approx 0.8857.
$$

---

Now we compute

$$
P(T^c\cup S).
$$

The event

$$
T^c\cup S
$$

means that the ticket is not technical, solved during the first contact, or both.

The only region not included in

$$
T^c\cup S
$$

is

$$
T\cap S^c.
$$

Therefore,

$$
P(T^c\cup S)=1-P(T\cap S^c).
$$

Substituting the value:

$$
P(T^c\cup S)=1-\frac{60}{350}.
$$

Write 1 as

$$
1=\frac{350}{350}.
$$

Then,

$$
P(T^c\cup S)=\frac{350}{350}-\frac{60}{350}.
$$

$$
P(T^c\cup S)=\frac{290}{350}.
$$

Simplifying:

$$
P(T^c\cup S)=\frac{29}{35}.
$$

As a decimal,

$$
P(T^c\cup S)\approx 0.8286.
$$

## 4. Computing \(P(S\mid T)\) and \(P(S\mid T^c)\)

The conditional probability formula is

$$
P(S\mid T)=\frac{P(T\cap S)}{P(T)}.
$$

From the table,

$$
P(T\cap S)=\frac{90}{350}
$$

and

$$
P(T)=\frac{150}{350}.
$$

Therefore,

$$
P(S\mid T)=\frac{\frac{90}{350}}{\frac{150}{350}}.
$$

The denominators cancel:

$$
P(S\mid T)=\frac{90}{150}.
$$

Simplifying:

$$
P(S\mid T)=\frac{3}{5}.
$$

Thus,

$$
P(S\mid T)=0.60.
$$

---

Now compute

$$
P(S\mid T^c).
$$

Using the conditional probability formula:

$$
P(S\mid T^c)=\frac{P(T^c\cap S)}{P(T^c)}.
$$

From the table,

$$
P(T^c\cap S)=\frac{160}{350}
$$

and

$$
P(T^c)=\frac{200}{350}.
$$

Therefore,

$$
P(S\mid T^c)=\frac{\frac{160}{350}}{\frac{200}{350}}.
$$

The denominators cancel:

$$
P(S\mid T^c)=\frac{160}{200}.
$$

Simplifying:

$$
P(S\mid T^c)=\frac{4}{5}.
$$

Thus,

$$
P(S\mid T^c)=0.80.
$$

## 5. Does being a technical ticket change the probability of being solved during the first contact?

Yes, being a technical ticket changes the probability of being solved during the first contact.

For technical tickets,

$$
P(S\mid T)=0.60.
$$

For non-technical tickets,

$$
P(S\mid T^c)=0.80.
$$

Since

$$
0.60\neq 0.80,
$$

the probability of being solved during the first contact is different for technical and non-technical tickets.

More specifically, technical tickets are less likely to be solved during the first contact.

## Final Answers

$$
P(T\cap S)=\frac{90}{350}=\frac{9}{35}\approx 0.2571
$$

$$
P(T\cap S^c)=\frac{60}{350}=\frac{6}{35}\approx 0.1714
$$

$$
P(T^c\cap S)=\frac{160}{350}=\frac{16}{35}\approx 0.4571
$$

$$
P(T^c\cap S^c)=\frac{40}{350}=\frac{4}{35}\approx 0.1143
$$

$$
P(T\cup S)=\frac{310}{350}=\frac{31}{35}\approx 0.8857
$$

$$
P(T^c\cup S)=\frac{290}{350}=\frac{29}{35}\approx 0.8286
$$

$$
P(S\mid T)=\frac{90}{150}=0.60
$$

$$
P(S\mid T^c)=\frac{160}{200}=0.80
$$

Therefore,

$$
\text{being a technical ticket changes the probability of being solved during the first contact.}
$$