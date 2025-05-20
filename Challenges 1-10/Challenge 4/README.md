# Challenge 4 – Largest palindromic number

In this challenge, the objective is to **identify the largest palindromic number** that can be formed as the product of two numbers, each less than a given threshold.

## Problem Statement

**Task:**  
Find the largest palindrome made from the product of two 3-digit numbers.

## Data Context

- `k`: positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

## Finding the Largest Palindromic Product by Exhaustive Search

To determine whether a number is a palindrome, one must check if its sequence of digits reads identically forwards and backwards. This can be achieved by reversing the digits of the number and comparing the reversed value to the original. If both are equal, the number is palindromic.

To find the largest palindromic product below a certain limit, consider all possible products of two numbers less than the given threshold. By systematically checking each product in descending order, and updating the maximum whenever a larger palindromic number is found, the search ensures that the largest such product is identified. The process can be optimized by breaking out of the inner search loop early if the current product cannot exceed the largest palindrome found so far, thus reducing unnecessary computations.

## Palindromic Product Search Using String Comparison

To identify the largest palindromic product of two numbers below a given limit, consider all possible products in descending order. For each product, determine if it is a palindrome by converting the number to a string and checking if it reads the same forwards and backwards. This string-based comparison eliminates the need for a separate digit-reversal process, streamlining the palindromicity check. By iterating from the largest factors downward and breaking early when further products cannot exceed the current maximum, the search is both exhaustive and efficient.

## Final Result

For `k = 1000`, the correct result is:

**906609**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*