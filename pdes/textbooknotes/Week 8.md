### Laplace's Equation
If a diffusion or wave process is stationary, or independent of time, then $u_{t}=u_{tt}=0$, and both of them reduce to the Laplace equation:
$$
\Delta u=0
$$
Which expands into:
$$
\begin{align}
u_{xx}=0 & \text{ in one dimension} \\
(\nabla \cdot \nabla)u=\Delta u = u_{xx} + u_{yy} =0 & \text{ in two dimensions}
\end{align}
$$
And so on. The in-homogeneous version is called *Poisson's equation*:
$$
\Delta u =f
$$
Where $f$ is a given function.

---

**ASIDE**

Recall the Cauchy-Riemann equations for some function $f(z)=u(z)+iv(z)$ in terms of the complex variable $z=x+iy$.
$$
\begin{align}
\frac{ \partial u }{ \partial x } = \frac{ \partial v }{ \partial y }  &  & \frac{ \partial u }{ \partial y } = - \frac{ \partial v }{ \partial x } 
\end{align}
$$
Recall that any complex function that satisfies the Cauchy-Riemann equations is analytic. Differentiate these equations to find that:
$$
u_{xx} = v_{yx} = v_{xy} = -u_{yy}
$$
Such that $\Delta u=0$ and $\Delta v=0$. Where $\Delta$ is the 2-D Laplacian. Thus, one can conclude that the real and imaginary parts of an analytic complex function are always harmonic

---

We are interested in solving the Laplace or Poisson's equations in a given domain $D$ with a condition on the boundary $\partial D$ such that
$$
\Delta u=f\text{ in }D
$$
With the possible boundary conditions:
$$
\begin{align}
u=h &  & \frac{ \partial u }{ \partial n } =h &  & \frac{ \partial u }{ \partial n } +au =h
\end{align}
$$
Where one of these conditions set on the $\partial D$
### Maximum Principle
Definition:
> Let $D$ be a connected bounded open set. Let $u(\vec{r})$ be a harmonic function in $D$ that is continuous on $\bar{D}=D\cup \partial D$. Then, the maximum and the minimum values of $u$ are attained on $\partial D$ and nowhere inside, unless $u$ is constant
- This statement is valid for 2-D and 3-D
- I have used $u(\vec{r})$ as a shorthand to represent both $u(x, y)$ and $u(x, y, z)$
### Uniqueness of the Dirichlet Problem
Suppose that we have two functions $u$ and $v$ that satisfy the conditions:
$$
\begin{cases}
\Delta u=f & \text{in }D \\
u=h & \text{on }\partial D
\end{cases}
$$
Subtract the two equations and defined $w=u-v$. Then,
$$
\begin{cases}
\Delta w=0 & \text{in }D \\
w=0 & \text{on }\partial D
\end{cases}
$$
By the maximum principle:
$$
0 = w(\vec{x}_{m}) \leq w(\vec{x}) \leq w(\vec{x}_{M}) =0 \text{  for all }\vec{x}\in D
$$
Where $w(\vec{x}_{m})$, $w(\vec{x})$, and $w(\vec{x}_{M})$ represent the minimum value, an arbitrary value, and the maximum, respectively.

Since the maximum and minimum values of $w(\vec{x})$ are zero, we can conclude $w\equiv 0$ and $u \equiv v$
### Invariance in 2-D
The Laplace equation is invariant under rigid motion. In a plane, this means under translation and rotation. A translation is defined by:
$$
x'=x+a \qquad y'=y+b
$$
And a rotation is defined by:
$$
\begin{align}
x' & = x\cos \alpha + y \sin \alpha \\
y' & = -x \sin \alpha + y \cos \alpha
\end{align}
$$
In both cases, under chain rule, one can see that:
$$
u_{xx} + u_{yy} = u_{x'x'} + u_{y'y'}
$$
Recall that the 2-D Laplacian:
$$
\Delta_{2} = \frac{ \partial^{2} }{ \partial x^{2} } + \frac{ \partial^{2} }{ \partial y^{2} }
$$
Has the form
$$
\Delta_{2} = \frac{ \partial^{2} }{ \partial r^{2} } + \frac{1}{r} \frac{ \partial  }{ \partial r } + \frac{1}{r^{2}} \frac{ \partial  }{ \partial \theta^{2} }
$$
In polar coordinates.
### Invariance in 3-D
Once again, the Laplacian is invariant under all rigid motions in space. Recall that any rotation in 3-D is given by
$$
\vec{x}' = B\vec{x}
$$
Where $B$ is a orthogonal matrix. From here, you can prove that:
$$
\Delta u = u_{x'x'} + u_{y'y'} + u_{z'z'}
$$
In this course, the spherical coordinates will be defined as:
$$
\begin{align}
r & = \sqrt{ x^{2}+y^{2}+z^{2} } = \sqrt{ s^{2}+z^{2} } \\
s & = \sqrt{ x^{2}+y^{2} } \\
\end{align}
$$
$$
\begin{align}
x & =s \cos \phi &  & z=r\cos \theta \\
y & = s \sin \phi &  & s=r\sin \theta
\end{align}
$$
We are using $\phi$ as the azimuthal angle, and $\theta$ as the polar angle.
### Rectangles and Cubes
For these domains, it is possible to solve the problem with separation of variables. The procedure is very similar to the one we are familiar to.
1. Look for separated solutions of the PDE
2. Put in the homogeneous boundary conditions to get the eigenvalues
	- This step is the one that relies on special geometry
3. Sum the series.
4. Put in the inhomogeneous initial or boundary conditions
It is important to complete the homogeneous boundary conditions before the inhomogeneous ones
### Poisson's Formula
What about the Dirichlet problem for a circle? The rotational invariance of $\Delta$ provides a hint that the circle is a natural shape for harmonic functions. Consider the problem:
$$
\begin{cases}
u_{xx} + u_{yy} =0 & \text{for }x^{2}+y^{2}<a^{2} \\
u=h(\theta) & \text{for }x^{2}+y^{2}=a^{2}
\end{cases}
$$
The circle has radius $a$ and boundary data $h(\theta)$. After separation of variables, the Laplacian becomes:
$$
R''\Theta + \frac{1}{r} R'\Theta + \frac{1}{r^{2}} R\Theta'' =0
$$
From which we can extract the two ODEs:
$$
\begin{align}
\Theta'' + \lambda\Theta & =0 \\
r^{2} R'' + rR' - \lambda R & =0
\end{align}
$$
For $\Theta(\theta)$ we have the implicit boundary conditions:
$$
\Theta(\theta) = \Theta(\theta+2\pi)\text{ for }-\infty<\theta<\infty
$$
$$
\Theta'(\theta) = \Theta'(\theta+2\pi) \text{ for } -\infty<\theta<\infty
$$
And furthermore, for $R(r)$, on the interval $0<r<a$ we also require that the solutions at $r=0$ are finite. Afterwards, you will find the solutions are:
$$
u = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} r^{n} (A_{n} \cos n\theta + B_{n} \sin n\theta)
$$
With coefficients:
$$
\begin{align}
A_{n} & =\frac{1}{\pi a^{n}} \int_{0}^{2\pi} h(\phi) \cos n\phi \, d\phi  \\
B_{n} & = \frac{1}{\pi a^{n}} \int_{0}^{2\pi} h(\phi) \sin n\phi \, d\phi 
\end{align}
$$
Now, if you complete the summation for $u$ explicitly, you will find:
$$
u(r, \theta) = (a^{2}-r^{2}) \int_{0}^{2\pi} \frac{h(\phi)}{a^{2}-2ar \cos(\theta-\phi)+r^{2}} \, \frac{d\phi}{2\pi}
$$
Which is *Poisson's formula*. It is the exact expression of any harmonic function inside a circle in terms of its boundary values.
