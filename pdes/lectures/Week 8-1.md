Readings: Strauss Ch 6, Harmonic functions

Definition:
The Laplacian of a function $u$ defined on some domain in $\mathbb{R}^{N}$ is defined as
$$
\Delta u = \nabla \cdot \nabla u = \sum_{i=1}^{N} u_{x_{i}x_{i}}
$$
An example, for s 3D function is:
$$
\Delta u(x, y, z) = u_{xx} + u_{yy} + u_{zz}
$$
- Recall that this is only true in the Cartesian plane
### Laplace's Equation
Defined to be:
$$
\Delta u=0
$$
A solution to the Laplace equation is called a *harmonic function*

The inhomogeneous version of the Laplace's equation $\Delta u=f$ with some given function $f$ is called Poisson's equation

If a diffusion or wave process is independent of time, then they will reduce to the Laplace equation.

Maximum Principle:
> Let $D$ be a connected bounded open set (in $N$-space, typically 2D or 3D space). Let $u$ be a harmonic function in $D$ that is continuous in $\bar{D}=D\cup \partial D$. Then, the maximum (and minimum) values of $u$ are attained on $\partial D$ and nowhere inside. (Unless $u$ is constant)

---
Example:
Prove that solutions to the Dirichlet problem are unique:
$$
\begin{cases}
\Delta u=f  & \text{on }\\
u=h & \text{on }\partial D
\end{cases}
$$
Suppose we have two solutions $u_{1}$ and $u_{2}$
- Subtract the two, and you will find they are the same
- Apply the maximum principle and conclude they are unique
---
- Missing notes here
- Something about invariance
- An example given in 2D

In 2D, the Laplacian is invariant to rotations. That is, if you provide a new basis $x'$ and $y'$ that are related to the original coordinates $x$, $y$, then the Laplacian will give you the same result:
$$
u_{xx} + u_{yy} = u_{x'x'} + u_{y'y'}
$$
In polar coordinates, with $x=r\cos \theta$ and $y=r\sin \theta$, the Laplacian in 2 dimensions goes to:
$$
\Delta_{2} = \frac{ \partial^{2} }{ \partial x^{2} } + \frac{ \partial^{2} }{ \partial y^{2} } = \frac{ \partial^{2} }{ \partial r^{2} } + \frac{1}{r} \frac{ \partial  }{ \partial r } + \frac{1}{r^{2}} \frac{ \partial^{2} }{ \partial \theta^{2} }
$$
In 3D, the Laplacian remains invariant under rigid motions

Suppose we rotated our coordinate system $\vec{x} = (x_{1}, x_{2}, x_{3})$ with some rotation $R$; such an $R$ is given by a 3x3 orthogonal matrix and the new coordinates are: $\vec{x}'=R\vec{x}$. We'll find that $\Delta u=u_{x_{1}'x_{1}'}+u_{x_{2}'x_{2}'}+u_{x_{3}'x_{3}'}$, that is, it remains unchanged.

In this course, the spherical coordinates will be defined as: $(r, \theta, \phi)$ with $\theta$ as the polar angle and $\phi$ as the azimuthal angle.
$$
\begin{cases}
x = r\sin \theta \cos \phi \\
y = r\sin \theta \sin \phi \\
z = r\cos \theta
\end{cases}
$$
---
Example:
Find the solutions that depend only on $r$ of $u_{xx}+u_{yy}=1$ in the annulus $a<r<b$ with $u(x, y)$ vanishing on both parts of the boundary $r=a$ and $r=b$

Assuming a radial solution,
$$
u_{rr} + \frac{1}{r}u_{r}=1
$$
We have:
$$
\begin{align}
ru_{rr} + u_{r}=r \\
(ru_{r})_{r}=r
\end{align}
$$
And
$$
ru_{r}=\frac{r^{2}}{2}+C_{1} \Rightarrow u_{r} = \frac{r}{2}+\frac{C_{1}}{r}
$$
Integrate:
$$
u = \frac{r^{2}}{4} + C_{1} \ln r + C_{2}
$$
Which gives us:
$$
\begin{align}
u(a) & = \frac{a^{2}}{4} + C_{1}\ln a + C_{2}=0 \\
u(b) & = \frac{b^{2}}{4} + C_{1}\ln b + C_{2}=0
\end{align}
$$
Which is a system of two equations with two unknowns

---

