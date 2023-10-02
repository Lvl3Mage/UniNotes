### 2)
#### a)
$$P(n): 2(3^0+3^1 + ... + 3^n) = 3^{n+1} - 1$$
##### Base step
$n=1$
$2(3^0 + 3^1) = 3^2 - 1? => 8 = 8$ 

$For \space n = k$
$$2(3^0 + 3^1 + ... + 3^k) = 3^{k+1}-1 => (HI)$$
##### Induction step
$$2(3^0 + 3^1 + ... + 3^k + 3^{k+1}) = 3^{k+1+1}-1$$
$$2(3^0 + 3^1 + ... + 3^k) + 2(3^{k+1}) = 3^{k+2}-1$$
Replacing proven part $2(3^0 + 3^1 + ... + 3^k)$ by $3^{k+1}-1$
$$ 3^{k+1}-1 + 2(3^{k+1}) = 3^{k+2}-1$$
$$ 3^1\cdot3^{k+1} = 3^{k+2}$$
$$3^{k+2} = 3^{k+2}$$

#### b)
$$\forall \space n \geq 2 :(1-\frac{1}{4})\cdot(1-\frac{1}{9})\cdot...\cdot(1-\frac{1}{n^2}) = \frac{n+1}{2n}$$
##### Base step
$n=2$
$$(1-\frac{1}{4}) = \frac{2+1}{2\cdot2}$$
$$\frac{3}{4} = \frac{3}{4}$$
$For\space n = k$
$$(1-\frac{1}{4})\cdot(1-\frac{1}{9})\cdot...\cdot(1-\frac{1}{k^2}) = \frac{k+1}{2k}$$
##### Induction step

$$(1-\frac{1}{4})\cdot(1-\frac{1}{9})\cdot...\cdot(1-\frac{1}{k^2})\cdot(1-\frac{1}{(k+1)^2}) = \frac{k+1}{2k}$$
#todo finish the induction step

### 4)

#todo Prove that the problem works for n = 1
#todo The next square can be constructed out of 4 previous squares and a n=1 square
### 5)
$$\forall \space n \geq 3 \space \exists \space Set \space A_n \space \text{of length n where the sum of } A_n \space \text{is divisible by each element in } A_n$$
#### Base step
$n=3$
$$A_3 = \set{1,2,3}$$
$$1+2+3 = 6$$
$$6 \space is \space \dot{1}, \dot{2},\dot{3}$$
$For \space n=k$
$$\exists \space A_n \text{ for k} => (HI)$$
#### Induction step
$$\text{if } A_{k+1} = A_k \space \cup \space {Sum(A_k)}$$
$$Sum(A_k \space \cup \space {Sum(A_k)}) = 2\cdot Sum(A_k) \text{ which is } \dot{Sum(A_k)}$$
