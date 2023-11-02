![[MasterTheorem.png]]

Given the equation:
$$T(N)=aT(\frac{N}{b}) + \theta(N^{k} \cdot log_p{N})$$ with $a\geq 1$, $b \gt 1$ and $p \geq 0$

$$
T(N) =
\begin{cases}
      \text{if } a \gt b^k & O(N^{log_b{a}})\\
      \text{if } a = b^k & O(N^{k} \cdot {log_{p+1}{N}})\\
      \text{if } a \lt b^k & O(N^{k} \cdot {log_{p}{N}})\\
\end{cases}
  
$$

#todo add examples
