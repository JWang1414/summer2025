Recall the Laplace equation:
$$
\Delta u=f=0
$$
We have chosen $f=0$ in this case, so we have the homogeneous version

Lets look at solutions to the Laplace equation in 2D. We have to solve the equation:
$$
u_{xx} + u_{yy} =0
$$
Which has the solution
$$
u = \log|r|
$$
Where $r$ is the radius. We have swapped to polar coordinates. So, it appears the solutions appear only on $r$.

In 3D, we might have solutions in a form like:
$$
u(\theta, \phi, r) = \frac{1}{4\pi r^{2}}
$$
And in higher order dimensions, maybe something like:
$$
\frac{1}{\alpha(n-1)r^{n-1}}
$$
---
$$
\begin{cases}
\Delta u=0 & 0<a<r<b\\
u=A & r=a \\
u=B & r=b
\end{cases}
$$
This is an annulus, or a "donut shape". From here, we can assume that $u=u(r)$ because the boundary conditions are perfectly radially symmetric.
$$
\Delta u = \frac{ \partial^{2}u }{ \partial r^{2} } + \frac{2}{r} \frac{ \partial u }{ \partial r }
$$
And all the angle related terms are equal to 0. Guess that the solution looks like $Ar^{k}$. This gives us the equation:
$$
\begin{align}
k(k-1)Ar^{k-2} + \frac{2}{r}kAr^{k-1}  & =0 \\
k(k+1)Ar^{k-2} & =0
\end{align}
$$
Which has roots $k=0, -1$. By the boundary conditions, the result is:
$$
u(r) = \frac{A_{1}}{r} + A_{2} = -\frac{1}{r} \frac{ab(A-B)}{a-b} + \frac{aB-bB}{a-b}
$$
---
$$
\begin{cases}
\Delta u=0 & 0\leq r<a \\
u(a, \theta)=1+3\sin\theta
\end{cases}
$$
Recall the implied boundary condition:
$$
u(0, \theta) <\infty
$$
Assume that:
$$
\begin{align}
u(r, \theta) & = 1 + f(r) \sin \theta \\
u(r=a) & = 1+ f(a) \sin \theta \\
f(a) & =3
\end{align}
$$
Place this into the initial equation:
$$
\Delta u = u_{rr} + \frac{1}{r} u_{r} + \frac{1}{r^{2}} u_{\theta\theta}
$$
- All computations from here
---
### Green's Functions
- You can use Green's functions $G(x, y)$ to solve the Laplace equation
- This is because these functions are symmetrical in the $x$ and $y$, while also solving the Laplace equation
We have:
$$
\Delta G(x, y) =0
$$
Where $x \in \Omega$. And,
$$
\begin{align}
u(x) & = \int _{\partial \Omega} G(x, y)f(y) \, dy \\
\Delta u(x) & = \int _{\partial \Omega} \Delta G(x, y)f(y) \, dy 
\end{align}
$$
$$
g(x) = u|_{\partial \Omega} = \int _{\partial \Omega} G(x, y)f(y) \, dy
$$
These two functions are equivalent to:
$$
\begin{cases}
\Delta u=0 & x \in \Omega \\
u|_{\partial \Omega}=g
\end{cases}
$$
Which gives us two different methods of solving for a solution. One with differential equations, and one with integration