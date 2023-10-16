### Basic Limit exercises
#### 1)
##### c)
For: $a_n=\frac{1}{log_2(n)}$
Find the term $n_0 \in \mathbb{N}$ such that $|a_n-l| \leq \epsilon$ for every $n \geq n_0$ for $\epsilon > 0$:
$$\displaystyle \lim_{n\to \infty }{\frac{1}{\log_{2}{n}}} = \lim_{n\to \infty }{\frac{1}{n}} = 0$$
$$|\frac{1}{\log_{2}{n}}-0| \leq \epsilon$$
$$\frac{1}{\log_{2}{n}} \leq \epsilon$$
$$\frac{1}{\epsilon} \leq \log_{2}{n}$$
$$2^\frac{1}{\epsilon} \leq n$$
$$2^\frac{1}{\epsilon} \leq n$$

#### 3)
##### a)
$\displaystyle \lim_{n \to \infty}{\frac{n^3 - 2n + 4}{1 + 30n - n^2}}$
Dividing everything by $n^2$
$\displaystyle \lim_{n \to \infty}{\frac{n^1 - \frac{2}{n} + \frac{4}{n^2}}{\frac{1}{n^2} + \frac{30}{n} - 1}} = \lim_{n \to \infty}{\frac{n - 0 + 0}{0 + 0 - 1}} = -\infty$
##### b)
$+\infty$ - Can be resolved fairly easily 
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

### All of em
#### 3)
##### a)
$\displaystyle \lim_{n \to \infty}{\frac{1^2 + 5^2 + ... + (4n-3)^2}{4n^3 + 5}} = \displaystyle \lim_{n \to \infty}{\frac{\infty}{\infty}}$
Stoltz criteria
$\displaystyle \lim_{n \to \infty}{\frac{1^2 + 5^2 + ... + (4n-3)^2 +(4(n+1)-3)^2  - (1^2 + 5^2 + ... + (4n-3)^2)}{4(n+1)^3 + 5 - (4n^3+5)}}$

$\displaystyle \lim_{n \to \infty}{\frac{(4(n+1)-3)^2}{4(n+1)^3 + 5 - (4n^3+5)}}$


$\displaystyle \lim_{n \to \infty}{\frac{1 + 8n + 16n^2)}{4 + 12n + 12n^2}} = \frac{0+ 0 + 16}{0 + 0 + 12} = \frac{4}{3}$

##### b)
$\displaystyle \lim_{n \to \infty}{\frac{3^n}{5n-1}}$

Stoltz criteria

$\displaystyle \lim_{n \to \infty}{\frac{3^{n+1} - 3^n}{ (5(n+1)-1)-(5n-1)}}$
$\displaystyle \lim_{n \to \infty}{\frac{3\cdot3^{n} - 3^n}{ 5n+5-1-5n+1}}$
$\displaystyle \lim_{n \to \infty}{\frac{2\cdot3^{n}}{5}} = +\infty$
##### d)
$\displaystyle \lim_{n\to \infty}{\sqrt[n]{\frac{3n}{(2n)!}}}$
$\displaystyle \lim_{n\to \infty}{\frac{\frac{3(n+1)}{(2(n+1))!}}{\frac{3n}{(2n)!}}}$
$\displaystyle \lim_{n\to \infty}{\frac{\frac{3n+3}{(2n+2))!}}{\frac{3n}{(2n)!}}}$
$\displaystyle \lim_{n\to \infty}{\frac{(3n+3)\cdot(2n)!}{3n\cdot (2n+2)!}}$


$\displaystyle \lim_{n\to \infty}{\frac{(3n+3)}{3n}} \cdot \frac{(2n)!}{(2n+2)!}$
$\displaystyle \lim_{n\to \infty}{\frac{3n+3}{3n}} \cdot \frac{(2n)!}{(2n+2) \cdot (2n+1) \cdot (2n)!}$
$\displaystyle \lim_{n\to \infty}{\frac{3n+3}{3n}} \cdot \frac{1}{(2n+2) \cdot (2n+1)} = 1\cdot \frac{1}{+\infty} = 0$

$\displaystyle \lim_{n\to \infty}{\sqrt[n]{\frac{3n}{(2n)!}}} = 0$

##### e)
$\displaystyle \lim_{n \to \infty}{\frac{cos(3^n)}{2n^2 + 4n + 5}}$
Sandwich criteria

$\displaystyle \lim_{n \to \infty}{\frac{-1}{2n^2 + 4n + 5}} \leq  \lim_{n \to \infty}{\frac{cos(3^n)}{2n^2 + 4n + 5}} \leq  \lim_{n \to \infty}{\frac{1}{2n^2 + 4n + 5}}$
$0 \leq \frac{cos(3^n)}{2n^2 + 4n + 5} \leq 0$
Thus $\displaystyle \lim_{n \to \infty}{\frac{cos(3^n)}{2n^2 + 4n + 5}} = 0$ 
