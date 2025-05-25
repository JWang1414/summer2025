### The Maximum Principle
This study will be for the diffusion equation, defined to be
$$
u_{t} = ku_{x x}
$$
The principle states that:
	If $u(x,t)$ satisfies the diffusion equation in a rectangle in space-time, then the maximum value of $u(x, t)$ is assumed either initially, $t=0$, or on the lateral sides $x=0, l$
- An alternate version of the maximum principle states that the maximum cannot be assumed anywhere inside the rectangle, only the edges (unless $u$ is constant)

The minimum principle states the same thing, that the minimum can be attained only on the edges
- A proof is done using the interval $[-u(x, t)]$

Physical interpretation:
- Given a rod with no internal heat source, the hottest spot and the coldest spot can initially only be at the ends of the rod
- The same for a substance diffusing along a tube, the highest initial concentration must be highest on one end
### Uniqueness
Specifically, this is referring to the uniqueness of the Dirichlet problem for the diffusion equation. This problem states that:
$$
\begin{align}
u_{t}-ku_{xx} & =f(x, t) & \text{ for } 0<x<l \text{ and } t>0 \\
u(x, 0) & =\phi(x) \\
u(0, t) & =g(t) & u(k, t)=h(t)
\end{align}
$$
Where $f$, $\phi$, $g$, and $h$ are all given functions.

*Uniqueness* is defined by a solution being completely given by its initial and boundary conditions. There is no ambiguity, or duplicates
### Stability
Means that the initial and boundary conditions are correctly formulated.

Lets define $h=g=f=0$. Let $u_{1}(x,0)=\phi_{1}(x)$ and $u_{2}(x,0)=\phi_{2}(x)$. Then the function $w=u_{1}-u_{2}$ as the solution with initial datum $\phi_{1}-\phi_{2}$.

From the *energy method*, we can state that:
$$
\int_{0}^{l} \left[ u_{1}(x,t)-u_{2}(x,t) \right] ^{2} \, dx \leq \int_{0}^{l} \left[ \phi_{1}(x)-\phi_{2}(x) \right] ^{2} \, dx
$$
- The right equation measures the "nearness" of the initial data for two solutions
- The left measures the "nearness" of the solutions at any later time
- Define a region of "nearness". If we start at $t=0$, for example, we stay nearby
- The definition of stability in a "square integral sense"

We can also write another definition, based on the maximum principle:
$$
\max_{0\leq x\leq l}\left| u_{1}(x,t)-u_{2}(x,t) \right| \leq \max_{0\leq x\leq l} \left| \phi_{1}(x)-\phi_{2}(x) \right|
$$
Which is valid for $t>0$.
- This version is known as the stability in a "uniform sense"
