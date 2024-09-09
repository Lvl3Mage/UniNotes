## Overview
- The Negative Binomial distribution models the number of successes in a sequence of independent Bernoulli trials before a specified number of failures occurs.
- Unlike the Binomial distribution, which focuses on the number of trials until a fixed number of successes, the Negative Binomial distribution focuses on the number of successes until a fixed number of failures.

## Use Case
- Used when you want to model the number of successes (e.g., number of goals scored, number of defective items produced) before observing a certain number of failures (e.g., strikes in baseball before three outs, defective products in a production run).

## Formula
- Probability Mass Function (PMF):
  $$
  P(X = k) = \binom{k + r - 1}{k} \cdot p^r \cdot (1 - p)^k
  $$
  - $k$: Number of successes
  - $r$: Number of failures
  - $p$: Probability of success in each trial
  
## Example
- **Baseball Game**:
  - Suppose a baseball team needs to score 3 runs ($r = 3$) before getting 2 outs to win the game.
  - Let \( p = 0.3 \) be the probability of scoring a run in each at-bat.
  - We want to find the probability of scoring exactly 3 runs before getting 2 outs.
  - Using the Negative Binomial PMF:
$$
    P(X = 3) = \binom{3 + 2 - 1}{3} \cdot 0.3^3 \cdot (1 - 0.3)^2
    $$
