# Task 1 — Recognizing Counting Models

In each problem, the main goal is to decide **which counting model fits the situation best**.  
To do that, we look at one key question:

**Does order matter, or does it not matter?**  
We also check whether repetition is allowed, and whether the arrangement is linear or circular.

---

## 1. Arranging 7 students in a line

Here, we place 7 different students in a straight line.

This is a **permutation**, because:

- all 7 students are used,
- each student is different,
- and the **order matters**.

For example, if Alice is first and Bob is second, that is different from Bob being first and Alice being second.

So the correct model is:

$$
7!
$$

because we are arranging 7 distinct people in order.

---

## 2. Choosing 4 members of a committee from 12 people

In this problem, we only want to **select** 4 people from 12.

This is a **combination**, because:

- we are choosing a group,
- **order does not matter**.

For example, choosing Anna, John, Maria, and Tom is the same committee as choosing Tom, Maria, Anna, and John.  
It is still the same group of 4 people.

So the correct model is:

$$
\binom{12}{4}
$$

This counts the number of ways to choose 4 people from 12 without caring about order.

---

## 3. Assigning gold, silver, and bronze medals among 15 athletes

This is a **k-permutation**.

Why?

Because:

- we choose **3 athletes** out of 15,
- and **order matters**, since gold, silver, and bronze are different positions.

For example:

- Alice gets gold, Bob gets silver, Carol gets bronze

is different from

- Bob gets gold, Alice gets silver, Carol gets bronze.

Even though the same 3 athletes are involved, the medal positions are different, so the outcome is different.

So the correct model is:

$$
P(15,3)=\frac{15!}{(15-3)!}=\frac{15!}{12!}
$$

This is called a **k-permutation**, or an ordered selection without repetition.

---

## 4. Forming a 6-digit PIN code

This is a **sequence with repetition**.

Why?

Because:

- the PIN has 6 positions,
- each position can be filled with any digit from 0 to 9,
- and digits **can repeat**.

For example:

- 111111 is allowed,
- 202020 is allowed,
- 000123 is also allowed.

So repetition is possible, and the order of digits clearly matters, because:

- 123456 is different from 654321.

Each of the 6 positions has 10 choices.

Therefore, the total number of PIN codes is:

$$
10^6
$$

So the correct model is **sequence with repetition**.

---

## 5. Arranging the letters of the word BANANA

This is a **permutation with repeated elements**.

Why?

Because we are arranging letters in order, but some letters repeat:

- A appears 3 times,
- N appears 2 times,
- B appears 1 time.

If all 6 letters were different, we would simply have:

$$
6!
$$

But because some letters are repeated, many arrangements look the same.  
For example, swapping one A with another A does not create a new arrangement, because the letters are identical.

So we must divide by the factorials of the repeated letters:

$$
\frac{6!}{3! \cdot 2!}
$$

Therefore, the correct model is **permutation with repeated elements**.

---

## 6. Seating 6 people around a round table

This is a **circular permutation**.

Why?

Because the people are arranged in a circle, not in a line.

In a circle, rotations do not create a new arrangement.  
For example, if everyone moves one chair to the left, the seating is still considered the same circular arrangement.

That is why circular arrangements are counted differently from ordinary permutations.

For \(n\) distinct people around a round table, the formula is:

$$
(n-1)!
$$

So for 6 people:

$$
(6-1)! = 5!
$$

Therefore, the correct model is **circular permutation**.

---

# Final Answers Summary

1. Arranging 7 students in a line → **Permutation**  
   $$
   7!
   $$

2. Choosing 4 members of a committee from 12 people → **Combination**  
   $$
   \binom{12}{4}
   $$

3. Assigning gold, silver, and bronze medals among 15 athletes → **k-permutation**  
   $$
   \frac{15!}{12!}
   $$

4. Forming a 6-digit PIN code → **Sequence with repetition**  
   $$
   10^6
   $$

5. Arranging the letters of BANANA → **Permutation with repeated elements**  
   $$
   \frac{6!}{3! \cdot 2!}
   $$

6. Seating 6 people around a round table → **Circular permutation**  
   $$
   5!
   $$