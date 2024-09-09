## Overview
- The Multinomial distribution is a generalization of the Binomial distribution to multiple categories.
- It describes the probability of observing a specific combination of outcomes across multiple categories in a fixed number of trials.

## Use Case
- Used when conducting a fixed number of independent trials with more than two possible outcomes in each trial, such as rolling a multi-sided die or categorizing items into multiple classes.

## Formula
- Probability Mass Function (PMF):
  $$
  P(X_1 = n_1, X_2 = n_2, ..., X_k = n_k) = \frac{n!}{n_1! \cdot n_2! \cdot ... \cdot n_k!} \cdot p_1^{n_1} \cdot p_2^{n_2} \cdot ... \cdot p_k^{n_k}
  $$
  - $X_i$: Number of observations in category $i$
  - $n_i$: Number of observations in category $i$
  - $p_i$: Probability of category $i$
  - $n$: Total number of trials
  - $k$: Number of categories

## Example
- **Dice Rolling**:
  - Suppose we roll a fair 6-sided die 10 times.
  - We want to find the probability of getting 2 ones, 3 twos, 4 threes, and 1 four.
  - Let $p_1 = \frac{1}{6}$, $p_2 = \frac{1}{6}$, $p_3 = \frac{1}{6}$, and $p_4 = \frac{1}{6}$ be the probabilities of each outcome.
  - Using the Multinomial PMF:
    $$
    P(X_1 = 2, X_2 = 3, X_3 = 4, X_4 = 1) = \frac{10!}{2! \cdot 3! \cdot 4! \cdot 1!} \cdot \left(\frac{1}{6}\right)^2 \cdot \left(\frac{1}{6}\right)^3 \cdot \left(\frac{1}{6}\right)^4 \cdot \left(\frac{1}{6}\right)^1
    $$
