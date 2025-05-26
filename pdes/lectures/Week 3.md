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
### Diffusion on the Half-Line
Define the domain of this half-line to be $D=(0, \infty)$, and take the Dirichlet boundary condition at the single endpoint $x=0$. The problem is:
$$
\begin{align}
v_{t}-kv_{xx} & =0 &  & \text{ in }\{ 0<x<\infty, 0<t<\infty \} \\
v(x,0) & =\phi(x) &  & \text{ for }t=0 \\
v(0,t) & =0 &  & \text{ for }x=0
\end{align}
$$
- If the solution to the PDE on this open region exists, we know that it will be unique because of our previous discussions

Define $\phi _\text{odd}$, the unique odd extension of $\phi$ to the whole line
$$
\phi _\text{odd}(x)= \begin{cases}
\phi(x) &  & \text{for }x>0 \\
-\phi(-x) &  & \text{for }x<0 \\
0 &  & \text{for }x=0
\end{cases}
$$
- Trivially, this function is odd such that $\phi(-x)\equiv -\phi(+x)$

Define another solution $u$, which is the solution for
$$
\begin{align}
u_{t}-ku_{xx} & =0 \\
u(x,0) & =\phi _\text{odd}(x)
\end{align}
$$
For the whole line $-\infty<x<\infty$, $0<t<\infty$

It is given by the formula
$$
u(x,t)=\int_{-\infty}^{\infty} S(x-y, t)\phi _\text{odd}(y) \, dy
$$
- Notice that $v(x,t)=u(x,t)$ for $x>0$. Considering only positive values of $x$, they are the same function
- $u$ must be an odd function, and so $u(0,t)=0$, as required by $v$'s initial data
- $u$ satisfies the same PDE, and so $v$ must also satisfy that PDE
- Since $v=u$ for $x>0$, and both have the same initial conditions for $x>0$, the initial conditions $\phi$ are satisfied for both $u$ and $v$

We can derive the formula for $v$ with our formula for $u$:
$$
u(x,t)=\int_{0}^{\infty} \left[ S(x-y, t)-S(x+y, t) \right] \phi(y) \, dy
$$
Therefore,
$$
v(x,t) = \frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \left[ \exp\left( -\frac{(x-y)^{2}}{4kt} \right)-\exp\left( -\frac{(x+y)^{2}}{4kt} \right) \right]\phi(y)  \, dy
$$
- The strategy taken to find $v$ is known as the *method of odd extensions*, or *reflection method*
### Neumann Problem
$$
\begin{align}
w_{t}-kw_{xx} & =0 &  & \text{for }0<x<\infty, 0<t<\infty \\
w(x,0) & =\phi(x) \\
w_{x}(0,t) & =0
\end{align}
$$
Instead, we define the even extension
$$
\phi _\text{even}(x) = \begin{cases}
\phi(x) &  & \text{for }x\geq 0 \\
\phi(-x) &  & \text{for }x\leq 0
\end{cases}
$$
- Even functions are functions such that $f(-x)=f(x)$
- If $f$ is an even function, then its derivative must be an odd function, and so $f'(0)=0$

The resultant explicit formula is
$$
w(x,t)= \frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \left[ \exp\left( -\frac{(x-y)^{2}}{4kt} \right) + \exp\left( -\frac{(x+y)^{2}}{4kt} \right) \right] \phi(y) \, dy
$$
