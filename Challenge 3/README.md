# Challenge 1 – Largest Prime Factor

In this challenge, the goal is to **find the largest prime factor** of a number.

## Problem Statement

**Task:**  
Find the largest prime number of $600851475143$

---

## Data Context

- `n`: positive integer number greater than 1.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

---

## First method

Uses the prime factors decomposition of a number. It divides the number by its prime factors (k=2, 3, 5, 7,...) until `n=1`. When this point is reached, the last prime factor is the largest one. Note that 2 is the only even prime number. Thus, we can speed up the algorithm with steps by 2, starting from 3.

---

## Optimal Approach

It has been proven that a prime factor of `n` is at most equal to $\sqrt{n}$. If there is no any prime number until this point, then `n` is a prime number.

- **Advantages:** ideal for large targets

---

## Final Result

For `n = 600851475143`, the correct result is:

**6857**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*