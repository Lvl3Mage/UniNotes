Given a sequence $a_n,$ it's sum sequence can be written like this:
$S_1 = a_1$
$S_2 = a_1 + a_2$
$...$
$S_n = a_1 + a_2 + ... + a_n$

The pair made out of a sequence and its sum $(a_n, S_n)$ is called a series of general term $a_n$. It can be expressed as $\displaystyle \sum^{\infty}_{n=1}{a_n}$.
Examples:
- $\displaystyle \sum^{\infty}_{n=1}{1/n}$ is called a harmonic series and is **divergent**.
- $\displaystyle \sum^{\infty}_{n=1}{1/2^n}$ is **convergent**.
- $\displaystyle \sum^{\infty}_{n=1}{1/n^2}$ is **convergent**.

$\displaystyle \sum^{\infty}_{n=1}{a_n}$ is convergent/divergent/oscillating if the partial sum sequence ($S_n$) is. Note that $\displaystyle \sum^{\infty}_{n=1}{a_n}$ is also used to denote the $\displaystyle \lim_{n \to \infty}{S_n}$

#todo add sum properties

## Geometric series
Given a sequence $a_n = r^n$ we can denote its sum sequence as $\displaystyle \sum^{\infty}_{n=1}{r^n}$
We can denote $S_n = r^1 + r^2 + ... + r^n$
If we multiply the whole equation by $r$ we get 
$(r)S_n = r^2 + r^3 + ... + r^n + r^{n+1}$

If we substract $(r)S_n$ from $S_n$ we get:
$S_n - (r)S_n = r^1 + r^2 + ... + r^n  - (r^2 + r^3 + ... + r^n + r^{n+1})$
$(1-r)S_n = r^1 - r^{n+1}$
And thus for $r \neq 1$
$$S_n = \frac{r-r^{n+1}}{1-r}$$
#todo add from image
# Convergence criteria
## P-series
#todo copy from photo
## Comparison Criteria
Consider 2 series $\displaystyle \sum^{\infty}_{n=1}{a_n}$ and $\displaystyle \sum^{\infty}_{n=1}{b_n}$
- If $0 \leq a_n \leq b_n$ and $\displaystyle \sum^{\infty}_{n=1}{b_n}$ converges then $\displaystyle \sum^{\infty}_{n=1}{a_n}$ also converges
- If $0 \leq b_n \leq a_n$ and $\displaystyle \sum^{\infty}_{n=1}{b_n}$ diverges then $\displaystyle \sum^{\infty}_{n=1}{a_n}$ also diverges
>[!tip]
>Given the sequence $a_n$ and series $\displaystyle \sum^{\infty}_{n=1}{a_n}$ we can find a different sequence $b_n$ that is obviously either smaller or bigger than $a_n$ and which converges or diverges. Using this sequence and the comparison criteria we can then prove that $\displaystyle \sum^{\infty}_{n=1}{a_n}$ either converges or diverges.  
## Limit criteria
Consider 2 series $\displaystyle \sum^{\infty}_{n=1}{a_n}$ and $\displaystyle \sum^{\infty}_{n=1}{b_n}$
We can calculate $\displaystyle \lim_{n \to \infty}{\frac{a_n}{b_n}} = l$
- If $0 \lt l \lt \infty$ then both series either diverge or converge.
- If $l=0$ and $\displaystyle \sum^{\infty}_{n=1} b_n$ converges, then $\displaystyle \sum^{\infty}_{n=1} a_n$ diverges
- If $l=+\infty$ and $\displaystyle \sum^{\infty}_{n=1} b_n$ diverges, then $\displaystyle \sum^{\infty}_{n=1} a_n$ converges
>[!info] 
>The point here is to select $b_n$ which you know converges or diverges and which, when calculating $l$ results in one of the cases.

## Alembert's criteria / ratio test
Consider the series $\displaystyle \sum^{\infty}_{n=1}{a_n}$
We can study $\displaystyle \lim_{n \to \infty}{\frac{a_{n+1}}{a_n}} = l$
- If $l \lt 1$ then the series converges
- If $l \gt 1$ then the series diverges
- If $l = 1$ then no information can be gathered using this criteria

## Leibniz criterion

# Sum of series
#todo copy from photo