# Challenge 6 – Difference of square sums

In this challenge, the goal is to **calculate the difference between the square of the sum and the sum of the squares** of the first n natural numbers.

## Problem Statement

**Task:**  
Find the difference between the square of the sum and the sum of the squares of the first one hundred natural numbers.

## Data Context

- `n`: positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

## Calculating the Sum Square Difference

Computes the sum of the first `n` natural numbers and squares it. Then, computes the sums of squares of the first `n` natural numbers. Finally, computes the difference.

## Optimized Calculation Using Closed-Form Formulas

To find the difference between the square of the sum and the sum of the squares of the first **n** natural numbers, consider the following:

1. The sum of the first _n_ natural numbers is given by the formula:  
$$
S = 1 + 2 + 3 + \ldots + n = \frac{n(n+1)}{2}
$$

2. The square of this sum is:  
$$
(S)^2 = \left(\frac{n(n+1)}{2}\right)^2
$$

3. The sum of the squares of the first _n_ natural numbers is:  
$$
Q = 1^2 + 2^2 + 3^2 + \ldots + n^2 = \frac{n(n+1)(2n+1)}{6}
$$

4. The required difference is:  
$$
(S)^2 - Q = \left(\frac{n(n+1)}{2}\right)^2 - \frac{n(n+1)(2n+1)}{6}
$$

This expression provides a direct way to compute the difference using closed-form formulas.

## Final Result

For `n = 100`, the correct result is:

**25164150**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*