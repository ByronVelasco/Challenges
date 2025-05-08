# Challenge 4 – Largest palindromic number

In this challenge, the goal is to **find the largest palindromic number** obtained from the product of two numbers less than a threshold.

## Problem Statement

**Task:**  
Find the largest palindrome made from the product of two 3-digit numbers.

---

## Data Context

- `threshold`: positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

---

## First approach

Computes all possible products of two numbers less than the threshold and cheks if the product is a palindrome.

---

## Optimal Approach

Since there are repeated products, for example $11 \cdot 2 = 2 \cdot 11$, we can limit to those where $y \geq x$. Also, we can start the search in descending order of the factors. In this way, we can skip all those products that are less than the maximum palindrome found until that point since $x \cdot y > x \cdot (y-k)$, for any $k \geq 1$.

- **Advantages:** less products and palindromic validation.

---

## Final Result

For `threshold = 1000`, the correct result is:

**906609**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*