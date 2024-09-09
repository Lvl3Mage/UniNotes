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


# Convergence criteria
## Geometric series
Given a sequence $a_n = r^n$ we can denote its sum sequence as $\displaystyle \sum^{\infty}_{n=1}{r^n}$
>[!summary] Cases based of $r$ values
>- If $-1 \lt r \lt 1$ then the series is **convergent** and equal to $\frac{r}{1-r}$ 
> - If $r \geq 1$ then the series is **divergent** to $+\infty$ 
> - If $r \lt -1$ then the series is **oscillating** and non-bounded
> - If $r = -1$ then the series is **oscillating** and bounded
## P-series
A p-series is a series defined as $\displaystyle \sum^{\infty}_{n=1}{\frac{1}{n^k}}$
>[!summary] Cases based of $k$ values
> - If $0 \lt k \lt 1$  then the p-series is **divergent**
> - If $k = 1$ then the p-series is called a **harmonic series**  and is **divergent** 
> - If $r \gt 1$ then the p-series is **convergent**

>[!warning] Hidden geometric series
>A series like $\displaystyle \sum^{\infty}_{n=1}{\frac{1}{2^n}}$ might seem like something related to p-series at first but is actually a **geometric series** with $k=\frac{1}{2}$: 
>$$\sum^{\infty}_{n=1}{\frac{1}{2^n}} \to \sum^{\infty}_{n=1}{\frac{1^n}{2^n}} \to \sum^{\infty}_{n=1}{\frac{1}{2}^n}$$

## Comparison Criteria

>[!info] General idea
>The general idea of the comparison criteria is given a series of the sequence $a_n$ ($\displaystyle \sum^{\infty}_{n=1}{a_n}$) find a different sequence $b_n$ which is either:
>1. **Convergent** *and* **is above $a_n$ after a certain point**
>2. **Divergent** *and* **is below $a_n$ after a certain point**
>After that it's fairly easy to understand why $a_n$ would be either **convergent (1)** or **divergent (2)**
>1. Since $b_n$ is **above $a_n$** and **convergent** $a_n$ cannot surpass it and thus must be also **convergent**.
>2. Since $b_n$ is below $a_n$ and **divergent** $a_n$ cannot drop beneath it and must also be **divergent**. 

Consider 2 series $\displaystyle \sum^{\infty}_{n=1}{a_n}$ and $\displaystyle \sum^{\infty}_{n=1}{b_n}$
- If $0 \leq a_n \leq b_n$ and $\displaystyle \sum^{\infty}_{n=1}{b_n}$ converges then $\displaystyle \sum^{\infty}_{n=1}{a_n}$ also converges
- If $0 \leq b_n \leq a_n$ and $\displaystyle \sum^{\infty}_{n=1}{b_n}$ diverges then $\displaystyle \sum^{\infty}_{n=1}{a_n}$ also diverges
## Limit criteria
Consider 2 series $\displaystyle \sum^{\infty}_{n=1}{a_n}$ and $\displaystyle \sum^{\infty}_{n=1}{b_n}$
We can calculate $\displaystyle \lim_{n \to \infty}{\frac{a_n}{b_n}} = l$
- If $0 \lt l \lt \infty$ then both series have **the same character** (either both diverge or both converge)
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
Consider the series $\displaystyle \sum^{\infty}_{n=1}{a_n}$
If both of the listed conditions are true:
- The sign of the term $a_n$ alternates
- The sequence $|a_n|$ is always decreasing and converges at 0
Then the series is convergent

# Sum of series
For series of type $\displaystyle \sum^{\infty}_{n=1}\frac{P(n)}{Q(n)}$ if $P(n)$ and $O(n)$ are polynomials with simple roots we can separate the polynomials into fractions:

>[!example]
>#### Initial series:
>$$\sum^{\infty}_{n=1}{\frac{8n+10}{n^3 + 3n^2+2n}}$$
>#### Solving the divisor for 0
>$n^3 + 3n^2+2n \to (n^2 + 3n+2)n = 0$
>1. $n_1=0$
>2. $n^2+3n+2 = 0 \to n_2 = -1, n_3 = -2$
>   
>**Therefore**
>**$$n^3 + 3n^2+2n = n(n+1)(n+2)$$**
>**$$\frac{8n+10}{n^3 + 3n^2+2n} = \frac{A}{n} + \frac{B}{n+1} + \frac{C}{n+2}$$**
>
>#### Calculating A, B and C
>$$\frac{8n+10}{\cancel{n^3 + 3n^2+2n}} = \frac{A(n+1)(n+2) + B(n)(n+2) +C(n)(n+1)}{\cancel{n(n+1)(n+2)}}$$
>$$8n+10 = A(n+1)(n+2) + B(n)(n+2) +C(n)(n+1)$$
>
>1. $A \to n=0 \to 0+10 = A(0+1)(0+2) + \cancel{B(0)(0+2)} + \cancel{C(0)(0+1)}$
>$2A = 10$
>**$A=5$**
>2. $B \to n=-1 \to -8+10 = \cancelto{0}{A(1-1)(-1+2)} + B(-1)(-1+2) + \cancelto{0}{C(-1)(1-1)}$
>$-B = 2$
>**$B=-2$**
>3. $C \to n=-2 \to -16+10 = \cancelto{0}{A(1-2)(2-2)} + \cancelto{0}{B(-2)(2-2)} + C(-2)(1-2)$
>$2C = -6$
>**$C=-3$**
>
>#### Substituting A, B and C for calculated values:
>$$\frac{8n+10}{n^3 + 3n^2+2n} = \frac{5}{n} - \frac{2}{n+1} - \frac{3}{n+2}$$

After decomposing the initial sequence into several smaller fractions we can rewrite the series as a sum of several series. 
>[!example] 
>$$\sum^{\infty}_{n=1}{\frac{8n+10}{n^3 + 3n^2+2n}} = \sum^{\infty}_{n=1}\frac{5}{n} - \sum^{\infty}_{n=1}\frac{2}{n+1} - \sum^{\infty}_{n=1}\frac{3}{n+2}$$

This series sum can be written out with offsets in a way such that the divisors in each column are equal
>[!example] 
>$$
>\begin{align} 
>\frac{5}{1} + \frac{5}{2} + \cancel{\frac{5}{3}} + \cancel{\frac{5}{4}} + \cancel{...}\\ 
>             -\frac{2}{2} - \cancel{\frac{2}{3}} - \cancel{\frac{2}{4}} - \cancel{...}\\
>             -\cancel{\frac{3}{3}} - \cancel{\frac{2}{4}} - \cancel{...}
>\end{align}
>= \frac{5}{1} + \frac{5}{2} - \frac{2}{2} = \frac{13}{2}
>$$
