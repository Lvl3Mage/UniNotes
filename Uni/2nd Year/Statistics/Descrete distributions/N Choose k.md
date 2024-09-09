## Overview
- $\binom{n}{k}$ represents the number of ways to choose $k$ successes from $n$ trials without regard to order.

## Formula
- Binomial Coefficient:
  $$
  \binom{n}{k} = \frac{n!}{k!(n - k)!}
  $$
  - $n!$: Factorial of $ n $, the product of all positive integers up to $ n $.
  - $k!$: Factorial of $ k $.
  - $(n - k)!$: Factorial of $n - k$.

## Example
- **Coin Flipping**:
  - Suppose we want to find the number of ways to get exactly 3 heads in 5 coin flips.
  - Using the binomial coefficient:
    $$
    \binom{5}{3} = \frac{5!}{3!(5 - 3)!} = \frac{5!}{3!2!} = \frac{5 \times 4}{2 \times 1} = 10
    $$
  - So, there are 10 different ways to get exactly 3 heads in 5 coin flips without regard to order.
