### Stoltz principle
#### 1)
$\displaystyle \lim_{n\to \infty } \frac{n}{2^n} = \frac{+\infty}{+\infty}$
$\displaystyle \lim_{n\to \infty } \frac{n+1 - n}{2^{n+1} - 2^n} = \lim_{n\to \infty } \frac{1}{2^n(2^1-1)} = \lim_{n\to \infty } \frac{1}{2^n} = 0$
Therefore $\displaystyle \lim_{n\to \infty } \frac{n}{2^n} = 0$
### Square root principle
#### 3)
$\displaystyle \lim_{n\to \infty } \sqrt[n]{n!} =\lim_{n\to \infty } {n!}^\frac{1}{n} = +\infty^0$
$a_n = n! \to \displaystyle \lim_{n\to \infty } \frac{(n+1)!}{n!} = \lim_{n\to \infty } \frac{(n+1) \cdot n!}{n!} = \lim_{n\to \infty } \frac{n+1}{1} = +\infty$
Therefore $\displaystyle \lim_{n\to \infty } \sqrt[n]{n!} = +\infty$
### Sandwich principle
#### 2)
$\displaystyle \lim_{n\to \infty } \frac{n^2 -1}{2n^2 - 1} \leq \lim_{n\to \infty } \frac{n^2 + \cos{(n^{100})}}{2n^2 - 1} \leq \lim_{n\to \infty } \frac{n^2 + 1}{2n^2 - 1}$
$\displaystyle \lim_{n\to \infty } \frac{n^2 -1}{2n^2 - 1} = \frac{1}{2}$ and $\lim_{n\to \infty } \frac{n^2 -1}{2n^2 + 1} = \frac{1}{2}$ 
Therefore $\lim_{n\to \infty } \frac{n^2 + \cos{(n^{100})}}{2n^2 - 1} = \frac{1}{2}$
