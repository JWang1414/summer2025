### Green's First Identity
Recall the divergence theorem:
$$
\iiint_{D} \nabla \cdot \vec{F} \, d\vec{x} = \iint_{\partial D} \vec{F}\cdot \vec{n} \, dS
$$
Where $\vec{F}$ is any vector function, and $D$ is a bounded solid region, and $\vec{n}$ is the unit outer normal on the boundary $\partial D$

Green's first identity states that:
$$
\iint_{\partial D} v \frac{ \partial u }{ \partial n } \, dS = \iiint_{D} \nabla v\cdot \nabla u \, d\vec{x} + \iiint_{D} v\Delta u \, d\vec{x}
$$
Where $u$ and $v$ are two arbitrary functions of three variables. $\vec{n}$ is the same as above, the unit outer normal on the boundary $\partial D$.
### Mean Value Property
> The average value of any harmonic function over any sphere equals its value at the centre. That is:
$$
\frac{1}{4\pi r^{2}} \iint_{S} u\, dS = u(\vec{0})
$$
> Where $r$ is the radius of the sphere, and $S$ is the surface of the sphere.
### Maximum Principle
> If $D$ is any solid region, a non-constant harmonic function in $D$ cannot take its maximum value inside $D$, but only on the boundary $\partial D$
### Dirichlet's Principle
Among all the functions $w(\vec{x})$ in $D$ that satisfy the Dirichlet boundary condition
$$
w = h(\vec{x}) \qquad \text{on }\partial D
$$
The lowest energy occurs for the harmonic function satisfying these conditions.

The energy in this context is defined as:
$$
E[w] = \frac{1}{2} \iiint_{D} \left| \nabla w \right| ^{2} \, d\vec{x}
$$
> The theorem states that, if $u(\vec{x})$ is the unique harmonic function in $D$ satisfying the Dirichlet conditions, and $w(\vec{x})$ is any other function in $D$ that satisfies the same conditions, then:
$$
E[w] \geq E[u]
$$
### Green's Second Identity
For any two arbitrary functions $u$ and $v$
$$
\iiint_{D} (u\Delta v -v\Delta u) \, d\vec{x} = \iint_{\partial D} \left( u \frac{ \partial v }{ \partial n } - v \frac{ \partial u }{ \partial n }  \right) \, dS
$$
Any boundary condition is called symmetric for the operator $\Delta$ if the right side vanishes for all pairs of functions $u$ and $v$ that satisfy the boundary conditions. Dirichlet, Neumann, and Robin conditions are all symmetric.
### Representation Formula
Used to represent any harmonic function as an integral over the boundary. If $\Delta u=0$ in $D$, then:
$$
u(\vec{x}_{0}) = \frac{1}{4\pi} \iint_{\partial D} \left[ -u(\vec{x}) \frac{ \partial  }{ \partial n } \left( \frac{1}{\left| \vec{x}-\vec{x}_{0} \right| } \right) + \frac{1}{\left| \vec{x}-\vec{x}_{0} \right| } \frac{ \partial u }{ \partial n }  \right] \, dS
$$
- There is a 2D version of this written in the textbook
### Green's Functions
The Green's Function $G(\vec{x})$ for the operator $\Delta$ and the domain $D$ at the point $\vec{x}_{0}\in D$ is a function defined for $\vec{x}\in D$ such that:
1. $G(\vec{x})$ possesses continuous second derivatives and $\Delta G=0$ in $D$, except at the point $\vec{x}=\vec{x}_{0}$
2. $G(\vec{x})=0$ for $x \in \partial D$
3. The function $G(\vec{x})+1 /(4\pi \left| \vec{x}-\vec{x}_{0} \right|)$ is finite at $\vec{x}_{0}$ and has continuous second derivatives everywhere and is harmonic at $\vec{x}_{0}$
It can be shown that a Green's function exists, and is unique. The typical notation for the Green's function is $G(\vec{x}, \vec{x}_{0})$

Theorem 1:
> If $G(\vec{x}, \vec{x}_{0})$ is the Green's function, then the solution of the Dirichlet problem is given by the formula:
$$
u(\vec{x}_{0}) = \iint_{\partial D} u(\vec{x}) \frac{ \partial G(\vec{x}, \vec{x}_{0}) }{ \partial n } \, dS
$$

For any region $D$ we have a Green's function, it is always symmetric:
$$
G(\vec{x}, \vec{x}_{0}) = G(\vec{x}_{0}, \vec{x}) \qquad \text{for }\vec{x}\neq \vec{x}_{0}
$$
Theorem 2:
> The solution of the problem;
$$
\begin{cases}
\Delta u=f & \text{in }D \\
u=h & \text{on }\partial D
\end{cases}
$$
> is given by
$$
u(\vec{x}_{0}) = \iint_{\partial D} h(\vec{x}) \frac{ \partial G(\vec{x}, \vec{x}_{0}) }{ \partial n } \, dS + \iiint_{D} f(\vec{x}) G(\vec{x}, \vec{x}_{0}) \, d\vec{x}
$$
