Recall the identity:
$$
\iiint_{D} v\Delta u \, d\vec{x} = \iint_{\partial D} v \frac{ \partial u }{ \partial n } \, dS - \iiint_{D} \nabla u\cdot \nabla v \, d\vec{x}
$$
This is Green's first identity. We will now move onto Green's second identity. Starting from the first, you can derive the second with algebraic manipulation:
$$
\iiint_{D} (v\Delta u - u\Delta v) \, d\vec{x} = \iint_{\partial D} \left( v \frac{ \partial u }{ \partial n } - u\frac{ \partial v }{ \partial n }  \right) \, dS
$$

Definition
> The *representation formula* represents a harmonic function as an integral over the boundary.

> If $\Delta u=0$ in $D$, then for $\vec{X}_{0}\in D$ we have
$$
u(\vec{x}_{0}) = \frac{1}{4\pi} \iint_{\partial D} \left[ -u(\vec{x}) \frac{ \partial  }{ \partial n } \left( \frac{1}{|\vec{x}-\vec{x}_{0}|} \right) + \frac{1}{|\vec{x}-\vec{x}_{0}|} \frac{ \partial u }{ \partial n }  \right] \, dS
$$

When using the representation formula, our goal is to remove one of the terms within the formula. Since, if we have a Dirichlet problem, we cannot know $\frac{ \partial u }{ \partial n }$, and if we have a Neumann problem, we cannot now $u(\vec{x})$, and so on. This modified version is called Green's function for $D$

The Green's function $G(\vec{x}, \vec{x}_{0})$ for the Laplacian (w/Dirichlet boundary conditions) on domain $D$ with source point $\vec{x}_{0}\in D$ is a function defined for $\vec{x}\in D$ such that
1. $G$ has smooth second derivative, and $\Delta G=0$ in $D$, except at the point $\vec{x}=\vec{x}_{0}$
2. $G(\vec{x}, \vec{x}_{0})=0$ for all $\vec{x}\in \partial D$
3. The function $G(\vec{x}, \vec{x}_{0}) + \frac{1}{4\pi(\vec{x}-\vec{x}_{0})}$ is finite at $\vec{x}_{0}$ and has smooth second derivatives everywhere and is harmonic at $\vec{x}_{0}$
- Typically you would try to minimize the blow out of the fundamental $\frac{1}{4\pi(\vec{x}-\vec{x}_{0})}$ equation by finding another function $G$ that blows up at the same point, and so adding them together would hide it
- In practice, finding $G$ is incredibly challenging, but it does exist

We can use Green's function to solve the Dirichlet problem for Laplace's equation:

Theorem:
> Let $D$ be a bounded domain in $\mathbb{R}^{3}$. For $\vec{x}_{0}\in D$, let $G(\vec{x}, \vec{x}_{0})$ be the associated Green's function on $D$. That is, the function which satisfies the conditions above.

> Let $u$ be a smooth function that solves (the Dirichlet problem):
$$
\begin{cases}
\Delta u=0 \\
u=g
\end{cases}
$$
> Then,
$$
u(\vec{x}_{0}) = \iint_{\partial D} g(\vec{x}) \frac{ \partial  }{ \partial n } G(\vec{x}, \vec{x}_{0}) \, dS
$$
- Generally speaking, although $G$ is very hard to find, usually it's not too bad to work with

Why is there a separation between $\vec{x}$ and $\vec{x}_{0}$ in the Green's function? $\vec{x}_{0}$ is a fixed point in $D$ while $\vec{x}$ lies on $\partial D$ and is a variable over which we integrate. But, a property of Green's functions is that they are interchangeable

Symmetry of Green's function:
> For any $\vec{x}, \vec{x}_{0}\in D$ with $\vec{x}\neq \vec{x}_{0}$, we have:
$$
G(\vec{x}, \vec{x}_{0}) = G(\vec{x}_{0}, \vec{x})
$$
