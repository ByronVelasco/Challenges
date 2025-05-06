# Challenge 1 – Sum of Multiples

In this challenge, the goal is to **sum all the multiples** of two given numbers that are less than a specified threshold.

## Problem Statement

**Task:**  
Find the sum of all the multiples of `3` and `5` that are **less than `1000`**.

---

## Data Context

- `threshold`: an integer greater than 1.
- `n1` and `n2`: positive integers.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

---

## Naive Approach

This method involves iterating through all the numbers less than the threshold and summing those that are divisible by either `n1` or `n2`.

- **Computational Cost:** Linear (proportional to the threshold)
- **Advantages:** Simple and intuitive
- **Disadvantages:** Becomes slower with larger inputs

---

## Optimal Approach (Mathematical Formula)

The optimal method avoids looping and instead uses arithmetic series formulas to compute the result directly. It works by summing the multiples of each number individually and subtracting the sum of their common multiples (to avoid double-counting).

For a number `x`, the sum of its multiples below a threshold is computed using the formula for the sum of the first `n` integers multiplied by `x`, where `n` is the number of such multiples.

- **Computational Cost:** Constant time (independent of the target)
- **Advantages:** Extremely fast, ideal for large targets
- **Disadvantages:** Requires understanding of arithmetic series and handling overlapping multiples correctly (using least common multiple)

---

## Final Result

For `threshold = 1000`, `n1 = 3`, and `n2 = 5`, the correct result is:

**233168**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*