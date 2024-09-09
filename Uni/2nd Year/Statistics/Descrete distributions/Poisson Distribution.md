## Overview
- The Poisson distribution models the number of events occurring in a fixed interval of time or space, given that these events occur with a constant rate and are independent of the time since the last event.
- It is often used to model rare events or phenomena where the probability of occurrence is small over a specific interval.

## Use Case
- Used in various fields such as insurance (to model the number of claims per day), telecommunications (to model the number of phone calls arriving at a call center), and biology (to model the number of mutations in a DNA sequence).

## Formula
- Probability Mass Function (PMF):
  $$
  P(X = k) = \frac{e^{-\lambda} \cdot \lambda^k}{k!}
  $$
  - $k$: Number of events occurring in the interval
  - $\lambda$: Average rate of events occurring in the interval (also known as the rate parameter)
  - $e$: Euler's number, approximately equal to 2.71828

## Example
- **Call Center**:
  - Suppose a call center receives on average 10 calls per hour $( \lambda = 10 )$.
  - We want to find the probability of receiving exactly 5 calls in the next hour $( k = 5 )$.
  - Using the Poisson PMF:
$$
    P(X = 5) = \frac{e^{-10} \cdot 10^5}{5!}
    $$
$$
    = \frac{e^{-10} \cdot 100000}{120}
    $$
$$
    \approx 0.037
    $$

