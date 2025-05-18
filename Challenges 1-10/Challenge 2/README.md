# **Challenge 2 – Sum of even Fibonacci numbers**

In this challenge, the goal is to **find the sum all the even Fibonacci numbers less than a given threshold.**

## Problem Statement

**Task:**  
Find the sum of all the even Fibonacci numbers less than `4000000`.

## Data Context

- `k`: a positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

## Brute Force Function Implementation

The problem involves finding the sum of all even-valued terms in the Fibonacci sequence that do not exceed a given limit. The Fibonacci sequence is defined by the recurrence relation:

$$
F_0 = 0, \quad F_1 = 1
$$

$$
F_n = F_{n-1} + F_{n-2} \quad \text{for} \quad n \geq 2
$$

The task is to compute:

$$
\text{Sum} = \sum_{\substack{F_n < \text{limit} \\ \\ F_n \text{ even}}} F_n
$$

That is, sum all Fibonacci numbers less than or equal to the specified limit, considering only those terms that are even.

## Optimized Approach Using Even Fibonacci Recurrence

The sum of even-valued terms in the Fibonacci sequence up to a given limit can be efficiently computed by leveraging the fact that every third Fibonacci number is even. The sequence of even Fibonacci numbers follows its own recurrence relation:
$$
E(n) = 4\cdot E(n-1) + E(n-2)
$$
where $E(n)$ denotes the n-th even Fibonacci number, with initial values $E(1) = 2$ and $E(2) = 8$. This relation allows direct generation of even Fibonacci numbers without computing the odd terms, significantly reducing the number of calculations required. The process continues until the generated even Fibonacci number exceeds the specified upper limit, and the sum of all such terms is accumulated.

## Final Result

For `k = 4000000`, the correct result is:

**4613732**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*