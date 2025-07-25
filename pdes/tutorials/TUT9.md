Solve PDE on the circular domain $\Omega$ with the boundary conditions::
$$
\frac{ \partial u }{ \partial r } -hu=f(\theta)
$$
Recall that we also have the implied boundary conditions:
1. $u$ is periodic
2. $u<\infty$ in $\Omega$

We can use separation of variables for this problem, like we always have.
- Important note: Separation of variables generally only works for simple shapes like circles and squares.

Assume that $u$ is harmonic. That is, in the domain $\Omega$
$$
\Delta u= u_{rr} + \frac{1}{r}u_{r} + \frac{1}{r^{2}}u_{\theta\theta} =0
$$
Begin the separation of variables by assuming:
$$
u(r, \theta) = R(r)T(\theta)
$$
Substituting this into the Laplacian:
$$
\begin{align}
R''T + \frac{1}{r}R'T + \frac{1}{r^{2}} RT''  & =0 \\
r^{2} \frac{R''}{R} + r \frac{R'}{R} = -\frac{T''}{T} =\lambda
\end{align}
$$
From the boundary conditions we learn:
$$
\begin{align}
u(0, \theta) <\infty  & \Rightarrow R(r) <\infty \\
u(r, 0) & = u(r, 2\pi) \\
u_{\theta}(r, 0) & = u_{\theta}(r, 2\pi)
\end{align}
$$
And from the given boundary condition:
$$
u_{r} -hu = R'T - hRT = f
$$
Check for $\lambda=\beta^{2}>0$
$$
T'' = -\lambda T = -\beta^{2}T
$$
Which has the solution:
$$
T = A \sin \beta\theta + B \cos \beta\theta
$$
Apply boundary conditions:
$$
T(0) = T(2\pi) \Rightarrow B = B \cos(2\pi \beta) \Rightarrow \beta \in \mathbb{Z}
$$
So we have positive eigenvalues $\lambda_{n}=n^{2}$ with the eigenfunctions:
$$
T_{n}(\theta) = C_{1} \cos(n\theta) + C_{2} \sin(n\theta)
$$
- You can try to find the other eigenvalues, but this question just has these positive ones
Now we turn our attention to the radial part. Which requires solving the problem:
$$
r^{2} R''_{n} + r R'_{n} = n^{2}R
$$
Which has the solution:
$$
R_{n}(r) = C_{3}r^{n} + C_{4}r^{-n}
$$
From the boundary conditions:
$$
R(0) < \infty \Rightarrow R_{n}(0) = C_{3} 0^{n} + C_{4} 0^{-n} < \infty \Rightarrow C_{4}=0
$$
We conclude that for the eigenvalues $\lambda_{n}=n^{2}$ the eigenfunctions are:
$$
R_{n}(r)T_{n}(\theta) = r^{n} (C_{1} \cos(n\theta) + C_{2} \sin(n\theta))
$$
Final solution:
$$
u = C_{0} + \sum_{n=1}^{\infty} r^{n} (A_{n} \cos n\theta + B_{n} \sin n\theta)
$$
You can substitute this full equation into the boundary condition for $f$ to determine what the function is.
$$
f(\theta) = u_{r} - hu
$$
---
Now what is the domain is a square or rectangle instead of a circle? Furthermore, what is the boundary conditions aren't exactly equal?

We can try the separation of variables to obtain the boundary conditions:
$$
\begin{align}
g(y) & = \sum_{n=1}^{\infty} A_{n}X_{n}(a)Y_{n}(y) \\
f(y) & = \sum_{n=1}^{\infty} A_{n}X_{n}(b)Y_{n}(y)
\end{align}
$$
- Something about trying a solution in the form $u=v_{1}+v_{2}+v_{3}+\dots$

---
For an annuli in the region $g<r<f$ with the conditions like:
$$
v_{r}+v=f \qquad w_{r}+w=u
$$
You can try the solution $u+v+w$.
- I have no idea what this means
---
Example with a wedge:
