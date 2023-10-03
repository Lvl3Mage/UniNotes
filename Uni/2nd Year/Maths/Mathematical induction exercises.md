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
# Strong induction

### 1)
$$\forall \space n \geq 24 \space \exists \space a,b \in \mathbb{N} \space where \space 7\cdot a + 5 \cdot b = n$$
#### Base steps
$24 = 7\cdot2 + 5\cdot2$
$25 = 7\cdot0 + 5\cdot5$
$26 = 7\cdot3 + 5\cdot1$
$27 = 7\cdot1 + 5\cdot4$
$28 = 7\cdot4 + 5\cdot0$
$$\exists \space a,b\text{ for [24, 25, ..., k]} => (HI)$$
#### Induction step
$$\exists \space a,b \text{ for } k+1?$$
$\text{ for } k+1-5 \space \exists \space a_{k+1-5},b_{k+1-5}$
$k+1-5 = 7 \cdot a_{k+1-5} + 5 \cdot b_{k+1-5}$
$$k+1 = 7\cdot a_{k+1-5} + 5 \cdot b_{k+1-5} + 5 =  7\cdot a_{k+1-5} + 5 \cdot (b_{k+1-5}+1)$$
>[!tip] Short explanation
>We calculate the numbers for the 5 cases proceeding 24 (itself included)
>We go back 5 cases from the $k+1$ case and since that falls into our range (beacause $k \geq 28$) we know that the values of a and b exist.
>Therefore we can go back to our $k+1$ case adding 5 to the $k+1-5$ case by substituting $b$ for $b+1$

### 4) fibonacci
$$a_1 = 1, a_2 = 1, a_n=a_{n-1} + a_{n-2}$$
$$a_n \leq 2^n?$$
$n=1$
$a_1 = 1 \leq 2^1$
$a_2 = 1 \leq 2^2$
$a_3 = 2 \leq 2^3$
$$a_n \leq 2^n \text{ for } n=1,2,3, ...,k$$
#### Induction step
$$a_{k+1}\leq2^{k+1}$$
$$a_{k}(\leq 2^k)+a_{k-1}(\leq 2^{k-1})\leq2^{k}+2^{k-1}\leq 2^{k+1}$$
$$2^{k}+2^{k-1}\leq 2^{k+1}$$
Dividing everything by $2^{k-1}$
$$2+1\leq 2^2$$
$$3\leq 4$$

