Fisher 2.1
### Question 18
Cauchy-Riemann equations:
$$
\begin{align}
u_{x}=v_{y} &  & v_{x}=u_{y}
\end{align}
$$
Define $z=x+iy$, then $\bar{z}=x-iy$. $h(z)=\bar{z}$ can be split into the two functions $h(z)=u(z)+iv(z)$, where $u(z)=\mathrm{Re}(z)$ and $v(z)=-\mathrm{Im}(z)$.
$$
\begin{align}
u_{x} = \frac{ \partial x }{ \partial x } =1 &  & u_{y} = \frac{ \partial x }{ \partial y } =0 \\
v_{x} = \frac{ \partial  }{ \partial x } (-y)=0 &  & v_{y} = \frac{ \partial  }{ \partial y } (-y)=-1
\end{align}
$$
The Cauchy-Riemann equations assert that
$$
\begin{align}
1=-1 &  & 0=-0
\end{align}
$$
Which is false. Therefore, we conclude $h(z)$ is not analytic.