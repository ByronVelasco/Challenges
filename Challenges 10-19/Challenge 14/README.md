# Challenge 14 – Longest Collatz Sequence

In this challenge, the objective is to **find the starting number under a given limit that produces the longest Collatz sequence**.  
A **Collatz sequence** is generated from a starting positive integer by repeatedly applying the following rules:
- If the number is even, divide it by 2.
- If the number is odd, multiply it by 3 and add 1.

Continue this process with each new value until the sequence reaches 1.

## Problem Statement

**Task:**  
Find the longest Collatz Sequence with a starting number under 1 million.

## Data Context

- `k`: integer number greater than 1.

Before reading the solution below, try solving the problem yourself and compare your approach and results.

## Systematic Generation and Analysis of Collatz Sequences

This approach systematically examines every integer from 1 up to a specified limit, generating the Collatz sequence for each number. For each starting value, it repeatedly applies the Collatz rules—halving the number if it is even, or multiplying by three and adding one if it is odd—until reaching 1. The length of each sequence is tracked, and the method identifies the starting number that produces the longest sequence within the given range.

## Optimized Collatz Sequence Search Using Memoization

This approach leverages memoization to efficiently determine the length of Collatz sequences for large ranges of numbers. By storing previously computed sequence lengths in a dictionary, it avoids redundant calculations for numbers that appear multiple times across different sequences. The method iterates through a subset of numbers, generating their Collatz sequences until reaching a value with a known sequence length, then updates the stored lengths for all encountered values. This significantly reduces computation time compared to recalculating each sequence from scratch.

## Final Result

For `k=1000000`, the correct result is:

**837799**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*