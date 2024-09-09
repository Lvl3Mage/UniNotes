## Overview
- The Hypergeometric distribution models the probability of drawing a specific number of successes (items of interest) from a finite population without replacement.
- It is commonly used in situations where you have a finite population and want to calculate the probability of drawing a certain number of items of interest in a sample without replacement.

## Use Case
- Used in various fields such as quality control (sampling from a production batch), biology (sampling from a population of organisms), and genetics (calculating probabilities of inheritance).

## Formula
- Probability Mass Function (PMF):
  $$
  P(X = k) = \frac{\binom{K}{k} \cdot \binom{N - K}{n - k}}{\binom{N}{n}}
  $$
  - \( K \): Total number of items of interest in the population
  - \( N \): Total population size
  - \( n \): Sample size
  - \( k \): Number of items of interest in the sample

## Example
- **Quality Control**:
  - Suppose a production batch contains 20 defective items out of 100.
  - We randomly sample 5 items from the batch without replacement.
  - We want to find the probability of obtaining exactly 2 defective items in the sample.
  - Using the Hypergeometric PMF:
$$
    P(X = 2) = \frac{\binom{20}{2} \cdot \binom{80}{3}}{\binom{100}{5}}
    $$
