### Question 2
---
a.
Begin by computing $u_{tt}$, $u_{r}$, and $u_{rr}$
$$
u_{tt} = \frac{ \partial^{2} }{ \partial t^{2} } \frac{v}{r} = \frac{1}{r} v_{tt}
$$
$$
u_{r} = \frac{ \partial  }{ \partial r } \frac{v}{r} = \frac{v_{r}}{r} - \frac{v}{r^{2}}
$$
$$
u_{rr} = \frac{ \partial  }{ \partial r } \frac{v_{r}}{r} - \frac{ \partial  }{ \partial r } \frac{v}{r^{2}} = \frac{v_{rr}}{r} - \frac{v_{r}}{r^{2}} - \left[ \frac{v_{r}}{r^{2}} - \frac{2v}{r^{3}} \right] = \frac{v_{rr}}{r} -\frac{2v_{r}}{r^{2}} + \frac{2v}{r^{3}}
$$
Substituting back into the original equation:
$$
\frac{v_{tt}}{r} = u_{tt} = c^{2} \left( u_{rr} + \frac{2}{r} u_{r} \right) = c^{2} \left[ \left( \frac{v_{rr}}{r} -\frac{2v_{r}}{r^{2}} + \frac{2v}{r^{3}} \right) + \frac{2}{r} \left( \frac{v_{r}}{r} - \frac{v}{r^{2}} \right)  \right] = c^{2} \left( \frac{v_{rr}}{r} \right)
$$
Which yields the final equation:
$$
\frac{v_{tt}}{r} = \frac{c^{2}}{r} v_{rr} \implies v_{tt} - c^{2} v_{rr} =0
$$
---
b.
This problem has been reduced to the homogeneous wave equation. This has the solution:
$$
v(r, t) = f(r+ct) + g(r-ct)
$$
Where $f$ and $g$ are two undetermined functions. Hence, the general solution for $u$ is:
$$
u(r, t) = \frac{1}{r} \left[ f(r+ct) + g(r-ct) \right] 
$$

---
c.
Based on the original definition of $v$
$$
v(r, t) = ru(r, t)
$$
The initial conditions are:
$$
v(r, 0) = ru(r, 0) = rf(r) \qquad v_{t}(r, 0) = ru_{t}(r, 0) = rg(r)
$$
---
d.
Since $r$ is the radial coordinate, I require that $v$ is finite at $r=0$.

To avoid confusion, I will rewrite the general solution for $v$ using the new functions:
$$
v(r, t) = a(r+ct) + b(r-ct)
$$
From the boundary conditions:
$$
\begin{align}
v(r, 0) & = a(r) + b(r) = rf(r) \\
v_{t}(r, 0) & = ca'(r) - c b'(r) = rg(r)
\end{align}
$$
Integrating the second equation, I obtain the system of equations:
$$
\begin{align}
a(r) + b(r) & = rf(r) \\
ca(r) - c b(r) & = \int rg(r) \, dr 
\end{align}
$$
Adding and subtracting these two equations together to solve for $a(r)$ and $b(r)$ yields:
$$
\begin{align}
a(r) & = \frac{r}{2} f(r) + \frac{1}{2c} \int rg(r) \, dr  \\
b(r) & = \frac{r}{2} f(r) - \frac{1}{2c} \int rg(r) \, dr 
\end{align}
$$
Which implies that $v$ is:
$$
v(r, t) = rf(r) + \frac{1}{2c} \int (r+ct)g(r+ct) \, dr - \frac{1}{2c} \int (r-ct)g(r-ct) \, dr
$$
---
e.
The final form of $u$ is:
$$
u(r, t) = \frac{v(r, t)}{r} = f(r) + \frac{1}{2cr} \left[ \int (r+ct)g(r+ct) \, dr - \int (r-ct)g(r-ct) \, dr \right]
$$
