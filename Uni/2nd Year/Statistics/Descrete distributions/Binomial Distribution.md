## Overview
- The Binomial distribution is a discrete probability distribution that describes the number of successes in a fixed number of independent Bernoulli trials.
- Each trial has two possible outcomes: success or failure.

## Use Case
- Used when conducting a fixed number of independent trials with two possible outcomes in each trial, such as flipping a coin a certain number of times or conducting a series of yes/no experiments.

## Formula
- Probability Mass Function (PMF):$$
  P(X = k) = \binom{n}{k} \cdot p^k \cdot (1 - p)^{n - k}
  $$
  - \( n \): Total number of trials
  - \( k \): Number of successes
  - \( p \): Probability of success in each trial
  
## Example
- **Coin Flipping**:
  - Suppose we flip a fair coin 5 times (\( n = 5 \)).
  - Let \( p = 0.5 \) (fair coin).
  - We want to find the probability of getting exactly 3 heads (\( k = 3 \)).
  - Using the Binomial PMF:
   $$P(X = 3) = \binom{5}{3} \cdot 0.5^3 \cdot (1 - 0.5)^{5 - 3}$$
$$ = \frac{5!}{3!(5-3)!} \cdot 0.5^3 \cdot 0.5^2$$
$$ = \frac{5!}{3!2!} \cdot 0.5^3 \cdot 0.5^2$$
$$ = \frac{5 \times 4}{2 \times 1} \cdot 0.125 \cdot 0.25$$
$$  = 10 \cdot 0.125 \cdot 0.25$$
$$ = 0.3125$$

