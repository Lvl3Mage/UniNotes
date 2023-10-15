$\text{A sequence is defined as an function a : }\mathbb{N} \rightarrow \text{X where X is a set (usually X=}\mathbb{R\text{)}}$
$\text{Usually a(n) is written as } a_n\text{. This expression is typically called the general term of the sequence}$
#todo growing, shrinking and monotone sequence (monotone is both growing and shrinking)
## Bounding
The sequence $a_n$ can be:
- Upper bounded if $\exists M \in \mathbb{R}$ such that $a_n \leq M$ for all $n \in \mathbb{N}$.
- Lower bounded if $\exists M \in \mathbb{R}$ such that $a_n \geq M$ for all $n \in \mathbb{N}$.
If a sequence meets both of these conditions, it is simply called **bounded**.

In some cases, the bounds can also serve as sequence maximums and minimums:
- A **lower bound** can be referred to as a **minimum** if it is the largest lower bound and is a part of the sequence $a_n$.
- Similarly, an **upper bound** can be called a **maximum** if it is the smallest upper bound and belongs to the sequence $a_n.

For example, let's consider the sequence defined by $a_n = \frac{1}{n}$.
- This sequence is **upper bounded by 1**, and 1 serves as the sequence's maximum.
- It is also **lower bounded by 0**, although the lower bound is not the sequence minimum since it is not part of the sequence.
## Convergence
We can define a sequence as converging to a certain value ($l$) when for any epsilon value selected that is above 0 ($\forall  \mathcal{E} \gt 0$) exists a term in the sequence ($a_n$) such that $|a_n - l| \leq \mathcal{E}$.
#todo add as mathematical expression
We can define a sequence as diverging $a+\infty$ ( or $a-\infty$) if:
#todo describe in text
$$\forall M \in \mathbb{R} \space \exists n_0 \in \mathbb{N} \text{ such that } a_n \geq M \text{ if } n \geq n_0$$
We can write:
$$\lim_{n \to \infty} a_n = +\infty$$
A sequence is said to be oscillating if it is neither convergent or divergent.

- If a sequence is **convergent** then it is also **bounded**.
- If a sequence is divergent $a + \infty$ ($a - \infty$) then it is not **upper bounded** (**lower bounded**).

## Limit arithmetic
$a \in \mathbb{R}, +\infty, -\infty$
- $a \pm \infty = \pm \infty$
- $a \cdot (\pm \infty) = \pm \infty \text{ if a }\gt 0, \mp \infty \text{ if a } \lt 0$
- $\frac{a}{\pm \infty} = 0$
- $\frac{\pm \infty}{a} = \pm \infty \text{ if a }\gt 0, \mp \infty \text{ if a } \lt 0$
- $0^{\infty} = 0$
### Undetermined values
- $0\cdot (\pm \infty)$
- $\frac{0}{0}$
- $\frac{\pm \infty}{\pm \infty}$
- $0^0$
- $1^{\infty}$
- $\infty^0$
### Properties of limits with sequences
If $\displaystyle \lim _{n\to \infty } a_n = l_1$ and $\displaystyle \lim _{n\to \infty } b_n = l_2$ 
($l_1, l_2 \in \mathbb{R}, 0+\infty, 0-\infty$)
- $\displaystyle \lim _{n\to \infty } a_n\pm b_n = l_1 \pm l_2$
- $\displaystyle \lim _{n\to \infty } \frac{a_n}{b_n} = \frac{l_1}{l_2}$ if $l_2 \pm 0$
- $\displaystyle \lim _{n\to \infty } k\cdot a_n = k\cdot l_1 (k\in \mathbb{R})$ 
## Stoltz theorem
If we have a $\displaystyle \lim _{n\to \infty }{\frac {a_{n}}{b_{n}} }$ and:
- $\lim{a_n} = 0$ and $b_n$ is shrinking with $\lim b_n = 0$
or
- $b_n$ is growing and $\lim b_n = +\infty$
${\displaystyle \lim _{n\to \infty }{\frac {a_{n+1}-a_{n}}{b_{n+1}-b_{n}}}=l }$
### Square root principle
If a $\displaystyle \lim_{n\to \infty } \sqrt[n]{a_n}$ is not determined ($a_n\geq 0$), but $\displaystyle \lim_{n\to \infty } \frac{a_{n+1}}{a_n} = l(n^2 \space real \space 0+\infty)$ exists. Then $\displaystyle \lim_{n\to \infty } \sqrt[n]{a_n} = l$ also exists.
Ex [[Sequence exercises#Square root priniciple]]

### Sandwich principle
If we have $a_n \leq b_n \leq c_n$
and $\displaystyle \lim_{n\to \infty } a_n = \lim_{n\to \infty } c_n = l \to (n \in \mathbb{R} \space and \space 0 \pm \infty)$
Then exists $\displaystyle \lim_{n\to \infty } b_n = l$
Ex [[Sequences#Sandwich principle]]
## Subsequences
A subsequence of a sequence $a_n$ is a sequence of terms of $a_n$ where each next selected index (k) in the subsequence $a_{n_k}$ is bigger than the last (i.e. $n_1 \lt n_2 \lt n_3 ...$).

## Subsequences
A subsequence of a sequence $a_n$ is essentially a new sequence, denoted as $a_{n_k}$, which is formed by picking terms from the original sequence $a_n." The key characteristic of a subsequence is that the index of each selected term, represented as $n_k$, is always greater than the index of the previous term (i.e., $n_1 \lt n_2 \lt n_3 ...$).

>[!note] 
>The actual values of the selected terms don't impact whether a sequence qualifies as a subsequence of another sequence. What matters is the pattern of index growth, as expressed in the inequality $n_1 \lt n_2 \lt n_3 ...$

