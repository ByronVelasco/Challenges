# Challenge 11 – Largest product in the same direction

In this challenge, the objective is to **find the largest product that can be formed by multiplying k adjacent numbers in the same direction (up, down, left, right, or diagonally) within a matrix**.

## Problem Statement

**Task:**  
Find the largest product of four adjacent numbers in the same direction.

## Data Context

- `matrix`: a `n x n` matrix.
- `k`: positive integer number.

Before reading the solution below, try solving the problem yourself and compare your approach and results.

## Systematic Search for the Largest Product of Adjacent Numbers in a Matrix
The approach systematically examines all possible groups of adjacent numbers in a square matrix, considering every row, column, and both diagonal directions. For each direction, it iterates through the matrix, calculating the product of consecutive elements of a specified length. If a zero is encountered, the search skips ahead to optimize performance. The process ensures that the largest product found in any direction is identified and returned.

## Final Result

For `k=4`, the correct result is:

**70600674**