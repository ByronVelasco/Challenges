# Challenge 6 – Difference of square sums

In this challenge, the goal is to **find the difference of $S_1$ and $S_2$** where $S_1$ is the sum of the squares of the first `n` natural numbers, and $S_2$ is the square of the sum of the first `n` natural numbers.

## Problem Statement

**Task:**  
Find such difference of the first one hundred natural numbers.

---

## Data Context

- `n`: positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

---

## First approach

Computes the sum of the first `n` natural numbers and squares it. Then, computes the sums of squares of the first `n` natural numbers. Finally, computes the difference.

- **Computational Cost:** high cost
- **Advantages:** Simple and intuitive
- **Disadvantages:** Becomes very slow with larger inputs

---

## Optimal Approach

The optimal method avoids looping and instead uses arithmetic series formulas to compute the result directly. Mathematically, the sum of squares of the first `n` natural numbers is given by $\frac{n(n+1)(2n+1)}{2}$. The square of the sum of the first `n` natural numbers is given by $\left(\frac{n(n+1)}{2}\right)^2$. With some arytmethic, the result is $\frac{n(n+1)(n-1)(3*n+2)}{12}$.

- **Computational Cost:** Constant time (independent of the target).
- **Advantages:** Extremely fast, ideal for large targets
- **Disadvantages:** Requires understanding of arithmetic series.

---

## Final Result

For `n = 100`, the correct result is:

**25164150**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*