## Derivative
Consider a 1 variable function $y = f(x)$
The derivative of this function $f'(x)$ can be understood as several things:
- The slope of a tangent line at point $x$.
- The growth rate of the function at $x$.
- The velocity of the function $f(x)$ at $x$.
All of these are different ways of expressing the same thing.

>[!info] The tangent of a function
>The tangent line of a function $f(x)$ at a point $a$ can be calculated as:
>$$y=f(a) + f'(a)(x-a)$$

## Taylor polynomial
The taylor  polynomial is a series of sums of the derivatives of a function $f(x)$ that can be used to approximate this function.
Some examples of taylor polynomial of degrees 1, 2 and 3 of $f(x)$ centered at point $a$ are:
$$P_{1,a}=f(a) + \frac{f'(a)}{1!}(x-a)$$
$$P_{2,a}=f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f''(a)}{2!}(x-a)^2$$
$$P_{3,a}=f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3$$
This polynomial will progressively approximate the function $f(x)$ as the degree of the taylor polynomial grows.

>[!info] Taylors polynomial: generic form
>You can express the taylor polynomial of degree $t$ centered at a as:
>$$\sum^{t}_{n=0}{\frac{f^n(a)}{n!}(x-a)^n}$$ 

### Example: approximating the sine function near 0

1. First derivative:
$$
f'(x) = \sin'(x) = \cos(x)$$

2. Second derivative:
$$
f''(x) = \cos'(x) = -\sin(x)
$$

3. Third derivative:
$$
f'''(x) = -\sin'(x) = -\cos(x)
$$

4. Fourth derivative:
$$
f''''(x) = -\cos'(x) = \sin(x)
$$

Now, let's rewrite the Taylor polynomials for the sine function centered at $(a = 0)$

1. **3rd-degree Taylor approximation of the sine function centered at $(a = 0)$:**

$$
P_{3,0}(x) = \sin(0) + \cos(0)(x - 0) - \frac{\sin(0)}{2}(x - 0)^2 - \frac{\cos(0)}{6}(x - 0)^3
$$

Simplifying this, we get:

$$
P_{3,0}(x) = x - \frac{x^3}{6}
$$

2. **4th-degree Taylor approximation of the sine function centered at $(a = 0)$:**
$$
P_{4,0}(x) = \sin(0) + \cos(0)(x - 0) - \frac{\sin(0)}{2}(x - 0)^2 - \frac{\cos(0)}{6}(x - 0)^3 + \frac{\sin(0)}{24}(x - 0)^4
$$

Simplifying this, we get:
$$
P_{4,0}(x) = x - \frac{x^3}{6} + \frac{x^4}{24}
$$
# Lagrange error bound

$$Error = |\frac{f^{n+1}(c)}{(n+1)!}(x-a)^{n+1}|$$ $c$ being the value between $x$ and $a$
#todo you basically maximize the term with c in it idk