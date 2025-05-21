# Challenge 5 – Least common multiple of a range

In this challenge, the objective is to **determine the least common multiple (LCM) of all positive integers up to a given number**.

## Problem Statement

**Task:**  
Find the least common multiple of all positive integer numbers up to 20.

## Data Context

- `n`: positive integer number.

Before reading the solution below, try solving the problem yourself and compare your approach and results.

## Brute Force Search for the Least Common Multiple

To find the least common multiple (LCM) of all integers in a given range, consider that the LCM must be a multiple of each number in that range. The approach is to examine successive multiples of the largest number in the range, checking for each whether it is divisible by all other numbers in the range. The first such multiple encountered is guaranteed to be the smallest number that is evenly divisible by every number in the range. This brute-force method is justified because it systematically tests each candidate in increasing order, ensuring that the smallest valid solution is found.

## Efficient LCM Calculation Using GCD

To efficiently compute the LCM for a range of numbers, one can use the mathematical relationship between the LCM and the greatest common divisor (GCD): for any two integers, the LCM can be found by dividing their product by their GCD. By applying this relationship iteratively, starting with 1 and combining it with each successive integer in the range, the process accumulates the LCM for the entire set. This method is justified because the LCM operation is associative, ensuring that the final result is the smallest number divisible by all numbers in the range.

## Final Result

For `n = 20`, the correct result is:

**232792560**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*