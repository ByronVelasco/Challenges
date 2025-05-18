# Challenge 1 – Sum of Multiples

In this challenge, the goal is to **find the sum of all natural numbers less than a given threshold that are multiples of either of two specified numbers.**

## Problem Statement

**Task:**  
Find the sum of all multiples of `3` and `5` that are **less than `1000`**.

## Data Context

- `k`: an integer greater than 1.
- `n1` and `n2`: positive integers (preferably coprime for the optimal method to work correctly).

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

## Brute Force Function Implementation

This first approach uses a straightforward loop to check each number below `k` and adds it to the sum if it is a multiple of either `n1` or `n2`. This brute-force method is easy to understand and implement, but may not be the most efficient for very large values of `k`.

## Efficient Sum Using Inclusion-Exclusion Principle

The optimized version uses mathematical formulas and the inclusion-exclusion principle to efficiently compute the sum of all multiples of `n1` or `n2` below `k`. Instead of checking each number individually, it calculates the sum of multiples directly, resulting in much faster performance, especially for large values of `k`.

**Note:** This function works correctly when `n1` and `n2` are coprime (i.e., have no common divisors other than 1).

## Final Result

For `k = 1000`, `n1 = 3`, and `n2 = 5`, the correct result is:

**233168**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*