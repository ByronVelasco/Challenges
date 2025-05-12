# Challenge 7 – k-th prime number

In this challenge, the goal is to **find the k-th prime number**.

## Problem Statement

**Task:**  
Find the 10001st prime number.

---

## Data Context

- `k`: positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

---

## First approach

Compute the list of the first k-th prime numbers and take the last one.

- **Computational Cost:** very high cost
- **Advantages:** Simple and intuitive
- **Disadvantages:** Becomes very slow with larger inputs

---

## Optimal Approach

The only even prime number is `2`. In addition, it is known that every number has at most one prime number greater than $\sqrt n$. This knowledge limits our **prime-search** to odd numbers less than $\sqrt n$.

- **Computational Cost:** Constant time (independent of the target).
- **Advantages:** Very fast, ideal for large targets.

---

## Final Result

For `k = 10001`, the correct result is:

**104743**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*