Dirichlet problem for a circle:
$$
\begin{cases}
u_{xx}+u_{yy}=0 & x^{2}+y^{2}<a^{2} \\
u=h(\theta) & x^{2}+y^{2}=a^{2}
\end{cases}
$$
We have a circle of radius $a$, and the boundary value problems have been around and inside it.

Previously, after separation of variables, we discovered Poisson's formula:
$$
u(r, \theta) = \frac{a^{2}-r^{2}}{2\pi} \int_{0}^{2\pi} \frac{h(\phi)}{a^{2}-2ar\cos(\theta-\phi)+r^{2}} \, d\phi
$$
Write $\vec{x}=(x, y)$ as a point with polar coordinates $(r, \theta)$. Let $\vec{x}'$ be a point on the boundary.
$$
u(\vec{x}) = \frac{a^{2}-|\vec{x}|^{2}}{2\pi a} \int _{|\vec{x}'|=a} \frac{u(\vec{x}')}{|\vec{x}-\vec{x}'|^{2}} \, ds'
$$
Where $ds$ is a small arc length of the circle. This integral is, therefore, one that goes around the boundary of the circle, for every vector $\vec{x}'$

Mean Value Property:
> Let $u$ be a harmonic function in a disc $D$ (continuous in its closure $\bar{D}$) then, the value of $u$ at the centre of $D$ equals the average of $u$ on its circumference
- Made significantly easier to compute if the origin $\vec{0}$ is chosen to be the centre of the disc

Recall that we previously stated the maximum principle for harmonic functions on a disc $D$. The proof of that statement relies on the mean value property.

---
Example:
Suppose that $u$ is a smooth harmonic function in the disc $D$ centred at $\delta$ with radius 2, and that $u=3\sin(2\theta)+1$ for $r=2$.

What is the maximum value of $u$ in $\bar{D}$?

Use the maximum principle to find:
$$
u = 3\sin(2\theta)+1 \leq 3+1=4
$$

Calculate the value of $u$ at the origin

By the mean value property,
$$
u(\vec{0}) = \frac{1}{2\pi(2)} \int _{|\vec{x}|=2} u(\vec{x}') \, ds' = \frac{1}{4\pi} \int_{0}^{2\pi} (3 \sin(2\theta)+1) \, (2d\theta)
$$
Which is equal to:
$$
u(\vec{0}) = 1
$$
---
