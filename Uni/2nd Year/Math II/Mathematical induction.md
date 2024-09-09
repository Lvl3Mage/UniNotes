**Mathematical induction** is a method for proving that a statement $P(n)$ is true for every natural number, that is, that the infinitely many cases $P(0)\space P(1)\space P(2)\space ...$  all hold. Informal metaphors help to explain this technique, such as falling dominoes or climbing a ladder.

A **proof by induction** consists of two cases. The first, the **base case**, proves the statement for $n=0$without assuming any knowledge of other cases. The second case, the **induction step**, proves that _if_ the statement holds for any given case $n=k$, _then_ it must also hold for the next case $n=k+1$.

>[!summary] In other words
>What we are doing is proving that if the statement works for ANY of the numbers, it will work for the next one. In the induction step we are NOT proving that the statement works for a number. Instead we are proving that IF we have a number that the statement works for, it will work for the next.
 
## Example:
$P(n): 4^n - 1 \space is \space \dot{3}$

### Base step
For $n = 1$ $=>$ $4^1-1 = 3 \space is \space \dot{3}$
### Induction step
For $n=k$: $4^k - 1 \space is \space \dot{3}$
**Is it true that for $n=k+1$, $4^{k+1}-1 \space is \space \dot{3}?$**
$$4^{k+1} - 1$$
$$4^1 \cdot 4^k - 1$$
$$(3+1)\cdot4^k - 1$$
$$3\cdot4^k + 4^k - 1$$
We've already assumed that $4^k - 1 \space is \space \dot{3}$ is true and $3\cdot4^k \space is \space \dot{3}$ is also true so $3\cdot4^k + 4^k - 1$ must be true.
[[Mathematical induction exercises#2)]]
# Complete/Strong induction
Strong induction differentiates itself from weak induction by assuming that the statement $P(n)$ is true for **all** values before n.

$P(n) \text{ statement for } n \in \mathbb{N}$
$\text{If } P(n) \text{ is true for } n=1 \text{ or other}$
$\text{If we assume }  P(n) \text{ is true for } n=1,2,...,k \text{ is P(n) true for n=k+1?}$
[[Mathematical induction exercises#4)Fibonacci]]
## Example
#todo add example