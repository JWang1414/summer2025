- Some recap on older PDEs, boundary conditions, and separation of variables
---
Separation of variables example:
$$
\begin{cases}
ut_{t} = u_{x}+2u \\
u(0, t) = u(\pi, t) = 0
\end{cases}
$$
Begin the separation of variables by supposing:
$$
u(x, t) = X(x)T(t)
$$
Plugging this into the original PDE, this gives us
$$
tXT'=X''T+2XT
$$
And, because we know, from the boundary conditions, that $X(0)T(t) = X(\pi)T(t)=0$ we can make the claim that $X(0)=X(\pi)=0$ for all $t$.

Now, we solve the spatial problem for this PDE, which is $X''=\lambda X$

For $\lambda=0$
$$
X(x)=Ax+B
$$
And, from our boundary conditions, this implies that $A=B=0$ so there are no eigenfunctions with $\lambda=0$

For $\lambda = \beta^{2}>0$
$$
X(x) = A\cosh(\beta x) + B \sinh(\beta x )
$$
Doing the same thing, plugging in our boundary conditions, we determine $A=B=0$

For $\lambda=-\beta^{2}<0$
$$
X(x) = A\cos(\beta x) + B\sin(\beta x)
$$
Which, from our boundary conditions yields $\sin(\beta \pi)=0$. For this to be true, $\beta$ must be some integer $n$ and so the eigenvalues and associated eigenfunctions are:
$$
\begin{cases}
\lambda_{n} = -n^{2} \\
X_{n}(x) = B_{n} \sin(nx)
\end{cases}
$$
Now for the temporal perspective. From the initial PDE, we have the problem:
$$
tu_{t} = u_{xx} + 2u \Rightarrow tT_{n}' = (2-n^{2})T_{n}
$$
Which has the solution
$$
T_{n} = t^{2-n^{2}}
$$
From this, we conclude that the final expression for the solution is
$$
u(x, t) = \sum_{n=1}^{\infty} B_{n} \sin(nx) t^{2-n^{2}}
$$
And, substituting in the boundary conditions
$$
u(x, 0) = \sum_{n=1}^{\infty} B_{n} \sin(nx) = 0
$$
Which, actually tells us there is no unique solution. The way you can tell is that sine is an odd function, and 0 is a constant, and so even function