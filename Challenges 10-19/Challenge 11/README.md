# Challenge 11 – Largest product in the same direction

In this challenge, the goal is to **find the largest product in the same direction (up, down, right, left, diagonal)** of k adjacent numbers.

## Problem Statement

**Task:**  
Find the largest product of four adjacent numbers in the same direction.

---

## Data Context

- `matrix`: a `n x n` matrix.
- `k`: positive integer number.

Before reading the solution below, try solving the problem yourself and compare your approach and results.

---

## Algorithm

Search the largest product of adjacent numbers in the three directions separetly: horizontal, vertical and diagonal. Choose the largest one. Recall that any product by zero is zero.

---

## Final Result

For `k=4`, the correct result is:

**70600674**