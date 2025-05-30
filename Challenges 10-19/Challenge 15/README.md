# Challenge 15 – Lattice Paths

In this challenge, the objective is to **determine the total number of lattice paths in an $n \times n$ grid**.  
A **lattice path** is any route from the top-left corner to the bottom-right corner of the grid, moving only to the right or downward at each step.

## Problem Statement

**Task:**  
Find the total number of lattice paths in a $20\times 20$ grid.

## Data Context

- `n`: integer number greater than 1.

Before reading the solution below, try solving the problem yourself and compare your approach and results.

## Brute Force Recursive Search for Lattice Paths

The problem of counting the number of unique paths from the top-left to the bottom-right corner of an $n \times n$ grid, moving only right or down, can be approached recursively. At any interior point in the grid, there are exactly two choices: move right or move down. The total number of paths from a given point is therefore the sum of the number of paths from the point immediately to the right and the point immediately below.

This recursive structure continues until reaching the boundary of the grid—either the bottom row or the rightmost column—where only one path remains (moving straight to the destination along the edge). By summing the possibilities at each step and storing previously computed results (memoization), redundant calculations are avoided, and the total number of unique routes is efficiently determined.

## Efficient Lattice Path Counting Using Binomial Coefficients

At each step in an $n \times n$ grid, there are two possible moves: right or down. To reach the bottom-right corner from the top-left, a total of $n$ moves right and $n$ moves down must be made, in any order. The total number of unique paths corresponds to the number of distinct sequences of these moves. This is a classic combinatorial problem, where the number of such sequences is given by the binomial coefficient:
$$
\text{Number of paths} = \binom{2n}{n} = \frac{(2n)!}{n! \, n!}
$$

This formula counts all possible ways to arrange $n$ right moves and $n$ down moves among $2n$ steps.

## Final Result

For `n=20`, the correct result is:

**137846528820**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*