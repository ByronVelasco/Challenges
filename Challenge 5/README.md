# Challenge 5 – Least common multiple of a range

In this challenge, the goal is to **find the least common multiple** of all integer numbers less than or equal to a number.

## Problem Statement

**Task:**  
Find the least common multiple of all integer numbers less than or equal to 20.

---

## Data Context

- `n`: positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

---

## First approach

Computes every multiple of n and verifies if it is a multiple of every number in the list.

- **Computational Cost:** very high cost
- **Advantages:** Simple and intuitive
- **Disadvantages:** Becomes very slow with larger inputs

---

## Optimal Approach

The **Least Common Multiple (LCM)** of all integers from 1 to `n` can be computed efficiently using **prime factorization**.

Every number between 1 and `n` can be expressed as a product of prime powers. Therefore, the LCM of numbers from 1 to `n` is the product of all **maximum powers of prime numbers** that divide any number in the range `[1, n]`.

$\text{LCM}(1, 2, \dots, n) = \prod_{\substack{p \leq n \\ p\ \text{prime}}} p^{\alpha_p}$

Where:
- $\left( \alpha_p \right)$ is the **maximum exponent** such that $\left( p^{\alpha_p} \leq n \right)$
- If $\left( p \leq \sqrt{n} \right)$, then $\left( \alpha_p = \left\lfloor \log(n) / \log(p) \right\rfloor \right)$
- If $\left( p > \sqrt{n} \right)$, then only $\left( \alpha_p = 1 \right)$ is used   

- **Computational Cost:** low cost
- **Advantages:** Extremely fast, ideal for large targets
- **Disadvantages:** Requires understanding of prime numbers and prime factorization of a number.

**Idea taken from:** xcannibalrabbit

---

## Final Result

For `n = 20`, the correct result is:

**232792560**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*