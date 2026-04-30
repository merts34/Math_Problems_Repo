# Task 2 — Permutations

Permutations are used when **order matters**. In all of these questions, the order of the books, people, or questions is important, so we use factorials.

## 1. In how many ways can 8 different books be arranged on a shelf?

We have **8 different books**, and we want to place them in a row on a shelf.

Since all books are different, we count the number of possible orders of 8 distinct objects.

For the first position, we can choose any of the 8 books.  
For the second position, 7 books remain.  
For the third position, 6 books remain, and so on.

So the total number of arrangements is:

8 × 7 × 6 × 5 × 4 × 3 × 2 × 1 = 8!

8! = 40320

Therefore, the number of ways to arrange the books is **40320**.

---

## 2. In how many ways can 8 people sit in a row if two particular people must sit next to each other?

Here, there are **8 people** in total, but **two specific people must sit together**.

Since those two people must remain side by side, it is easier to treat them as **one single block** first.

So instead of thinking of 8 separate people, we now think of:

- 6 other individual people
- 1 block containing the two particular people

That means we have **7 objects** in total.

These 7 objects can be arranged in:

7!

ways.

However, inside the block, the two particular people can also switch places.  
For example, if the two people are A and B, then inside the block they can be:

- AB
- BA

So there are:

2!

ways to arrange the people inside the block.

Therefore, the total number of valid seatings is:

7! × 2!

7! × 2! = 5040 × 2 = 10080

So the number of ways is **10080**.

---

## 3. In how many ways can 8 people sit in a row if those two particular people must not sit next to each other?

In this question, the two particular people are **not allowed** to sit together.

The easiest method is:

1. Count all possible arrangements.
2. Subtract the arrangements where the two people are together.

### Step 1: Count all arrangements of 8 people

Since 8 people can sit in any order, the total number of arrangements is:

8! = 40320

### Step 2: Count arrangements where the two people sit together

From Question 2, we already know that the number of arrangements where the two particular people sit next to each other is:

7! × 2! = 10080

### Step 3: Subtract

So the number of arrangements where they do **not** sit together is:

8! - 7! × 2!

40320 - 10080 = 30240

Therefore, the number of ways is **30240**.

---

## 4. In how many ways can 10 questions in a test be ordered if the first question is fixed?

There are **10 questions**, but the first question is already fixed in place.

That means we do **not** rearrange all 10 questions.  
We only rearrange the remaining **9 questions**.

The number of ways to arrange 9 different questions is:

9!

9! = 362880

Therefore, the number of possible orderings is **362880**.

---

# Final Answers

- Books on a shelf: **40320**
- Two particular people must sit together: **10080**
- Two particular people must not sit together: **30240**
- Test questions with the first question fixed: **362880**