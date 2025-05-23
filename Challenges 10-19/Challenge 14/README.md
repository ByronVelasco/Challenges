# Challenge 14 – Longest Collatz Sequence

In this challenge, the goal is to **find the longest Collatz Sequence**. A **Collatz sequence** is a sequence of numbers produced from a starting positive integer, following these rules:
- If the number is even, divide it by 2.
- If the number is odd, multiply it by 3 and add 1.
Repeat the process with the resulting number. The sequence ends when it reaches 1.

## Problem Statement

**Task:**  
Find the longest Collatz Sequence with a starting number under 1 million.

---

## Data Context

- `k`: integer number greater than 1.

Before reading the solution below, try solving the problem yourself and compare your approach and results.

---

## First Approach

Iterates through all starting numbers less than `k`, generating their respective Collatz sequences by repeatedly applying the sequence rules until reaching 1. For each starting number, it counts the length of the sequence. The algorithm tracks and returns the starting number that produces the longest Collatz sequence.

## Optimized Approach

Many numbers in the Collatz sequence eventually reach values that have already been computed for smaller starting numbers. To avoid redundant calculations, we use memoization to store the length of each sequence as it is found. When generating a sequence, if we encounter a number whose sequence length is already known, we can immediately use the stored value instead of recalculating it. Additionally, since every even number's next step is simply half its value, we can use the relation `lenght_Collatz(n) = length_Collatz(n/2) + 1` for even `n` to further optimize the process. This approach significantly reduces computation time, especially for large values of `k`.

---

## Final Result

For `k=1000000`, the correct result is:

**837799**