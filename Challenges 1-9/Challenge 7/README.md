# Challenge 7 – k-th prime number

In this challenge, the goal is to **find the k-th prime number**.

## Problem Statement

**Task:**  
Find the 10001st prime number.

## Data Context

- `k`: positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

## Prime Number Search Using Square Root Optimization

In previous challenges, we used the fact that 2 is the only even prime number and that any composite number has at least one prime factor less than or equal to its square root. Building on these ideas, we can efficiently identify prime numbers by checking divisibility only up to the square root and skipping even numbers greater than 2. By counting primes in this way, we can find and return the k-th prime number.

## Efficient Prime Search Using the Prime Number Theorem and Sieve of Eratosthenes

To efficiently find the k-th prime number, we rely on the **Prime Number Theorem**, which states that the number of primes less than a given number $n$ is approximately $\frac{n}{\ln(n)}$. This relationship allows us to estimate an upper bound for the location of the k-th prime. Specifically, the k-th prime is roughly near $k \ln(k)$, and a more accurate estimate is given by $k(\ln(k) + \ln(\ln(k)))$ for large values of $k$.

With this upper bound, we can use the **Sieve of Eratosthenes** algorithm to efficiently generate all prime numbers up to the estimated limit. The sieve works by iteratively marking the multiples of each prime as composite, ensuring that only primes remain unmarked. By counting the primes as they are found, we can identify the k-th prime without checking every number individually, greatly improving computational efficiency.

## Final Result

For `k = 10001`, the correct result is:

**104743**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*