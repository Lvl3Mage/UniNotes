A 2 variable function $f(x,y)$ forms a plane with height defined at every point $(x,y)$ by the value of the function.
#todo add example of 3d view of $f(x,y)=x\cdot y$ from desmos
# Derivatives of 2 variable functions
The derivative of the 2 variable function $f(x,y)$ is composed of partial derivatives in the both the x and y axes.
## Partial derivatives
The partial derivative in the x axis is the Instantaneous velocity of $f(x,y)$ when moving in the x direction. 
This derivative is typically denoted as $\frac{\partial f}{\partial x}(a,b)$ 
The same applies for the y axis which is denoted as: $\frac{\partial f}{\partial y}(a,b)$

>[!tip] How to calculate partial derivatives
>When calculating a partial derivative of the function $f(x,y)$ in the axis x we simply treat all the other variables ($y$) as constants (as if they were a number like 1, 2 or 3). The sample applies for the y axis.
>Example:
>$$f(x,y) = x^4 + x^3 y + 5 x^2 y^2 - x + 4$$
>$$\frac{\partial f}{\partial x} = 4x^3 + 3x^2 y + 10 x y^2 - 1$$
>$$\frac{\partial f}{\partial y} = 0 + x^3 \cdot 1 + 5x^2 \cdot 2y - 0 + 0$$

## The function gradient
The gradient of the function $f(x,y)$ is defined as:
$$\nabla  f(x,y) = (\frac{\partial f}{\partial x}(a,b),\frac{\partial f}{\partial y}(a,b))$$

It is a vector field where at every point $(a,b)$ it is equal to a vector compose of the partial derivatives in he x and y axis. 

When taking a vector $v$ we can calculate the **rate of change** of **of the original function** $f(x,y)$ in the direction of $v$ at point $(a,b)$ using the **dot product** between the ***fucking* gradient** and the *fucking* normalized vector **$v$**:
$$D_vf(a,b) = \nabla f(a,b) \cdot \frac{v}{|v|}$$
## Tangent plane
To calculate the tangent plate to a function $f(x,y)$ at point $(a,b)$ we can use the following formula:

$$z=f(a,b)+\nabla f(a,b) \cdot (x-a, y-b)$$

# Double derivatives
You can also derive the partial derivatives of a partial derivative in both y and x axis.

For the example function $f(x,y)$ the results might look something like this:
$$
\frac{\partial f}{\partial x} \to
\begin{cases}
      \frac{\partial^2f}{\partial x^2}\\
      \frac{\partial^2f}{\partial x \partial y}\\
\end{cases}
$$
$$
\frac{\partial f}{\partial y} \to
\begin{cases}
      \frac{\partial^2f}{\partial y \partial x}\\
      \frac{\partial^2f}{\partial y^2}\\
\end{cases}
$$
## Hessian matrix
A hessian matrix is a matrix composed of the partial derivatives of a function that describes its curvature. The matrix takes the following form:
$$ 
\begin{bmatrix}
f_{xx} & f_{xy} \\
f_{yx} & f_{yy} 
\end{bmatrix}
\to
\begin{bmatrix}
\frac{\partial^2f}{\partial x^2} & \frac{\partial^2f}{\partial x \partial y} \\
\frac{\partial^2f}{\partial y \partial x} & \frac{\partial^2f}{\partial y^2} 
\end{bmatrix}  $$
