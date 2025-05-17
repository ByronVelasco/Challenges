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

## Algorithm

Iterates through all starting numbers less than `k`, generating their respective Collatz sequences by repeatedly applying the sequence rules until reaching 1. For each starting number, it counts the length of the sequence. The algorithm tracks and returns the starting number that produces the longest Collatz sequence.

---

## Final Result

For `k=1000000`, the correct result is:

**837799**