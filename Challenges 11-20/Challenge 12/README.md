# Challenge 12 – Highly Divisible Triangular Number

In this challenge, the goal is to **find the lowest triangle number with at least k divisors**. A **triangle number** is made of the sum of the first n natural numbers, e.g., 15 = 1+2+3+4+5 is a triangle number.

## Problem Statement

**Task:**  
Find the lowest triangle number with at least 500 divisors.

---

## Data Context

- `k`: positive integer number.

Before reading the solution below, try solving the problem yourself and compare your approach and results.

---

## Algorythm

Compute all triangle numbers and count their divisors. Return the first triangle number such that its number of divisors is greater than or equal to `k`. Recall that every divisor comes in pairs, e.g., divisors of 15 are (1, 15), (3, 5), and each pair has at most one divisor greater than $\sqrt{n}$. This limits our search only to divisors less than or equal to $\sqrt{n}$.

---

## Final Result

For `k=500`, the correct result is:

**70600674**