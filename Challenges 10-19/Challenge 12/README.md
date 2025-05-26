# Challenge 12 – Highly Divisible Triangular Number

In this challenge, the objective is to **find the smallest triangle number that has at least `k` divisors**.  
A **triangle number** is the sum of the first `n` natural numbers; for example, 15 is a triangle number because 15 = 1 + 2 + 3 + 4 + 5.

## Problem Statement

**Task:**  
Find the smallest triangle number that has at least 500 divisors.

## Data Context

- `k`: positive integer number.

Before reading the solution below, try solving the problem yourself and compare your approach and results.

## Brute Force Search for Highly Divisible Triangle Numbers

This approach incrementally generates triangle numbers by summing consecutive natural numbers. For each generated value, it calculates the total number of divisors by checking all integers up to its square root, counting both the divisor and its complement. The process continues until a triangle number is found that meets or exceeds the required number of divisors.

## Optimized Triangle Number Search Using Prime Factorization and Memoization

This method leverages the mathematical properties of triangle numbers and divisor counting to improve efficiency:

1. **Triangle Number Formula**: the $n$-th triangle number is given by: $$T_n = \frac{n(n+1)}{2}$$
  Since $n$ and $n+1$ are consecutive integers, they are always coprime (share no common factors except 1).


2. **Divisor Function Multiplicativity**: for two coprime numbers $a$ and $b$, the number of divisors of their product is the product of their individual divisor counts: $$d(a \cdot b) = d(a) \cdot d(b)$$ where $d(x)$ denotes the number of divisors of $x$.

3. **Efficient Factorization**:  
	- If $n$ is even, $T_n = \frac{n}{2} \cdot (n+1)$.
	- If $n$ is odd, $T_n = n \cdot \frac{n+1}{2}$.   

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This ensures both factors are integers and coprime, allowing the divisor counts to be multiplied directly.

4. **Memoization**:  
	Previously computed divisor counts are stored and reused to avoid redundant calculations, significantly speeding up the search.

By combining these properties, the function efficiently finds the smallest triangle number with at least $k$ divisors.

## Final Result

For `k=500`, the correct result is:

**70600674**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*