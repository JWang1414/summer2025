Example problem
$$
\begin{cases}
u_{tt}-c^{2}u_{xx}=xt \\
f=0 \\
g=0
\end{cases}
$$
From previous knowledge, the solution will be along the lines of
$$
u(x, t) = \frac{1}{2c}\int_{0}^{t} \int_{x-c(t-s)}^{x+c(t-s)} ys \, dy  \, ds = \frac{1}{2c} \int_{0}^{t} \frac{s}{2}(4ctx-4ccsx) \, ds =\frac{xt^{3}}{6}
$$
---
Another way people tried to solve the in-homogeneous wave equation was to factor out the derivative operator
$$
\begin{align}
\left( \frac{ \partial^{2} }{ \partial t^{2} } -c^{2}\frac{ \partial^{2} }{ \partial x^{2} } \right) u & =xt \\
\left( \frac{ \partial  }{ \partial t } +c\frac{ \partial  }{ \partial x }  \right)\left( \frac{ \partial  }{ \partial t } -c\frac{ \partial  }{ \partial x }  \right)u & =xt \\
\end{align}
$$
Now, we can defined the new variable $v$, which results in two first order PDEs
$$
\begin{align}
v & =\left( \frac{ \partial }{ \partial t } -c\frac{ \partial  }{ \partial x }  \right)u \\
xt & =\left( \frac{ \partial  }{ \partial t } +c\frac{ \partial  }{ \partial x }  \right)v
\end{align}
$$
---
Example problem.
Verify that
$$
u(x, t) = \begin{cases}
h\left( t-\frac{x}{c} \right) &  & x<ct \\
0 &  & x>ct
\end{cases}
$$
Solves
$$
\begin{align}
u_{tt}=c^{2}u_{xx} &  & x>0 \\
u(x,0)=0 &  & u_{t}(x,0)=0 \\
u(0,t)=h(t)
\end{align}
$$
The derivatives for $x<ct$ are quite simple.
$$
\begin{align}
u_{t}=h'\left( t-\frac{x}{c} \right) &  & u_{tt}=h''\left( y-\frac{x}{c} \right) &  & u_{xx}=\frac{1}{c^{2}}h''\left( t-\frac{x}{c} \right)
\end{align}
$$
