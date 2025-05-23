# Challenge 10 – Sum of prime numbers

In this challenge, the objective is to **calculate the sum of all prime numbers less than a specified number**.

## Problem Statement

**Task:**  
Calculate the sum of prime numbers below 2000000.

## Data Context

- `k`: positive integer number.

Before reading the solutions below, try solving the problem yourself and compare your approach and results.

## Efficient Prime Summation Using the Sieve of Eratosthenes

This approach utilizes the Sieve of Eratosthenes algorithm to efficiently identify all prime numbers below a given limit. The method begins by assuming all numbers in the range are prime, then iteratively marks the multiples of each discovered prime as non-prime. By the end of the process, only prime numbers remain unmarked, allowing for their sum to be calculated efficiently.

## Optimized Sieve for Odd Numbers Only

A more efficient approach leverages the fact that 2 is the only even prime number. By initializing the sum with 2 and applying the Sieve of Eratosthenes only to odd numbers, memory usage and computation time are significantly reduced. This method marks non-prime odd numbers and accumulates the sum of all primes below the given limit.

## Final Result

For `k=2000000`, the correct result is:

**142913828922**