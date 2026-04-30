# Task 6 — Combinations in Card Problems

A standard deck has:

- 13 hearts
- 39 non-hearts
- 12 face cards (J, Q, K in 4 suits)
- 40 non-face cards

Since the order of cards in a hand does not matter, we use **combinations**.

---

## 1. In how many ways can 5 cards be drawn so that the hand contains exactly 2 hearts?

We choose:

- 2 hearts from 13
- 3 non-hearts from 39

So the number of hands is:

\[
\binom{13}{2}\binom{39}{3}
\]

Now calculate:

\[
\binom{13}{2}=78,\qquad \binom{39}{3}=9139
\]

\[
78 \cdot 9139 = 712842
\]

**Answer:** **712842**

---

## 2. In how many ways can a 5-card hand contain at least one heart?

First count all possible 5-card hands:

\[
\binom{52}{5}
\]

Then subtract the hands with **no hearts**, meaning all 5 cards come from the 39 non-hearts:

\[
\binom{39}{5}
\]

So the number of hands with at least one heart is:

\[
\binom{52}{5}-\binom{39}{5}
\]

Now calculate:

\[
\binom{52}{5}=2598960,\qquad \binom{39}{5}=575757
\]

\[
2598960 - 575757 = 2023203
\]

**Answer:** **2023203**

---

## 3. In how many ways can a 5-card hand contain no face cards (J, Q, K)?

There are 12 face cards in the deck, so the number of non-face cards is:

\[
52-12=40
\]

We choose all 5 cards from these 40 non-face cards:

\[
\binom{40}{5}
\]

Now calculate:

\[
\binom{40}{5}=658008
\]

**Answer:** **658008**