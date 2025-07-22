Recall Poisson's formula:
$$
u(r, \theta) = \frac{a^{2}-r^{2}}{2\pi} \int_{0}^{2\pi} \frac{h(\phi)}{a^{2}-2ar \cos(\theta-\phi)+r^{2}} \, d\phi
$$
Which can be used to express any harmonic function inside a circle in terms of its boundary conditions.

If we replace its polar coordinates $(r, \theta)$ with the vector $\vec{x}=(x, y)$, and define $\vec{x}'$ as any point on the boundary $(a, \phi)$, then we can use the cosine law to express:
$$
\left| \vec{x}-\vec{x}' \right| ^{2} = a^{2}+r^{2} - 2ar \cos(\theta-\phi)
$$
And Poisson's formula takes the alternate form:
$$
u(\vec{x}) = \frac{a^{2}-|\vec{x}|^{2}}{2\pi a} \int _{|\vec{x}'|=a} \frac{u(\vec{x}')}{\left| \vec{x}-\vec{x}' \right| ^{2}} \, ds'
$$
Where the differential is some arc length along the circumference $ds'=a\cdot d\phi$. The boundary function has been re-written $u(\vec{x}')=h(\phi)$.

Theorem 1:
> Let $h(\phi)=h(\vec{x}')$ be any continuous function on the circle $C=\partial D$. Then, the Poisson formula provides the only harmonic function in $D$ for which
$$
\lim_{ \vec{x} \to \vec{x}_{0} } u(\vec{x}) = h(\vec{x}_{0}) \text{ for all }\vec{x}_{0}\in C
$$
> Which means that $u(\vec{x})$ is a continuous function on $\bar{D}$ and differentiable to all orders inside $D$.
### Mean Value Property
Let $u$ be a harmonic function in a disk $D$, continuous in its closure $\bar{D}$. Then the value of $u$ at the centre of $D$ equals the average of $u$ on its circumference
### Maximum Principle
Let $u(\vec{x})$ be harmonic in $D$. The maximum must be obtained somewhere on the boundary $\partial D$.
### Circles, Wedges, and Annuli
- I'm not going to repeat examples in the textbook notes, and this portion is mostly examples
Example geometries for each shape:
$$
\begin{align}
\text{Wedge: } & \{ 0<\theta<\theta_{0}, 0<r<a \} \\
\text{Annulus: } & \{ 0<a<r<b \} \\
\text{Exterior of a Circle: } & \{ a<r<\infty \}
\end{align}
$$
For each of these, Dirichlet, Neumann, and Robin, separation of variables should work.
- Often times the equations that appear in these problems are the same as ones that have already been solved, you just need to change the boundary conditions
- For the exterior of a circle, the logic of the interior circle can be used, you just need to swap there the finite boundary needs to be
- The annulus gets very complex, because it is challenging to claim any finite boundary conditions
- Problems with the wedge are also very similar to problems with the circle
