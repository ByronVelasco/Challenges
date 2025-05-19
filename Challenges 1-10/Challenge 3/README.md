# Challenge 3 – Largest Prime Factor

In this challenge, the objective is to **determine the largest prime factor** of a given number.

## Problem Statement

**Task:**  
Find the largest prime factor of $600851475143$

## Data Context

- `n`: positive integer number greater than 1.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

## Brute Force Function Implementation

To find the largest prime factor of a given number:

1. First, determine if the number itself is prime by checking divisibility from 2 up to its square root. If it is only divisible by 1 and itself, it is prime.
2. If the number is not prime, search for its largest factor by starting from half of the number and decrementing.
3. For each candidate factor, check if it divides the number evenly and if it is a prime number.
4. The process stops when the largest such prime factor is found.

## Efficient Prime Factorization by Progressive Division

To efficiently determine the largest prime factor of a given integer, one can utilize the following mathematical approach:

First, remove all factors of 2 from the number, as 2 is the smallest and only even prime. This ensures that the remaining value is odd, simplifying subsequent steps. After eliminating all factors of 2, proceed to check divisibility by odd numbers, starting from 3 and incrementing by 2 each time. For each odd candidate, if it divides the current value evenly, divide the value by this candidate and continue the process. This stepwise division removes smaller prime factors early, reducing the size of the number to be factored and thus improving efficiency.

The process continues until the square of the current candidate exceeds the remaining value. At this point, if the remaining value is greater than 1, it must itself be a prime number and is therefore the largest prime factor. This method is justified because, after removing all smaller prime factors, any remaining factor greater than the square root of the original number must be prime.

## Final Result

For `n = 600851475143`, the correct result is:

**6857**

---

*Challenge yourself: Try solving it using both methods and reflect on their differences in logic and efficiency!*