### Question 1
---
a.
Re-write the PDE as dot product using the gradient of the function $u$,
$$
3u_{x} + 8u_{y} = \begin{bmatrix}
3 \\
8
\end{bmatrix} \cdot \nabla u =0
$$
This means solutions must be parallel to the line $8x-3y$, and so this PDE has the general solution:
$$
u(x, y) = f(8x-3y)
$$
---
b.
Define the two new variables $\alpha=3x+8y$ and $\beta=8x-3y$. Using the chain rule, we have:
$$
\begin{align}
u_{x} & = \frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial x } + \frac{ \partial u }{ \partial \beta } \frac{ \partial \beta }{ \partial x } = 3 u_{\alpha} + 8 u_{\beta} \\
u_{y}  & = 8u_{\alpha} - 3u_{\beta}
\end{align}
$$
Substitute back into the original equation:
$$
3u_{x} + 8u_{y} = 3 (3u_{\alpha} + 8u_{\beta}) + 8(8u_{\alpha} - 3u_{\beta}) = 9u_{\alpha} + 24u_{\beta} + 64u_{\alpha} - 24u_{\beta} = 73 u_{\alpha} =0
$$
I conclude that $u_{\alpha}=0$. The solution is therefore a function exclusively in terms of $\beta$.
$$
u(\alpha, \beta) = f(\beta) = f(8x-3y)
$$
---
c.
From the auxiliary condition:
$$
u(0, y) = f(0-3y) = f(3y) = \cos y
$$
Substitute $z=3y$, $y=z /3$,
$$
f(z) = \cos\left( \frac{z}{3} \right) \implies f(8x-3y) = \cos\left( \frac{8x-3y}{3} \right) = \cos\left( \frac{8}{3}x-y \right)
$$
I conclude the general form is:
$$
u(x, y) = \cos\left( \frac{8}{3}x-y \right)
$$
### Question 2
---
a.
$$
u_{t} + tu_{x} = \begin{bmatrix}
1 \\
t
\end{bmatrix} \cdot \nabla u =0
$$
Where, at every point $(t, x)$, its tangent vector $\left( 1, \frac{dx}{dt} \right)$ is perpendicular to $(1, t)$. Therefore,
$$
\frac{dx}{dt} = t \implies \int  \, dx = \int t \, dt \implies x = \frac{t^{2}}{2} + C
$$
---
b.
The characteristics are determined uniquely by the constant $C$. The general solution is therefore:
$$
x=\frac{t^{2}}{2} + C \implies C = x - \frac{t^{2}}{2}
$$
The general solution can be written as:
$$
u(x, t) = f\left( x-\frac{t^{2}}{2} \right)
$$
---
c.
From the auxiliary conditions:
$$
u(x, 0) = f\left( x-\frac{0^{2}}{2} \right) = f(x) = \sin x
$$
Therefore,
$$
u(x, t) = \sin\left( x-\frac{t^{2}}{2} \right)
$$
### Question 3
I will attempt to solve this problem using the change of variables method. Define the new variables $\alpha=ax+by$ and $\beta=bx-ay$. Then,
$$
\begin{align}
u_{x} & = \frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial x } + \frac{ \partial u }{ \partial \beta } \frac{ \partial \beta }{ \partial x } = au_{\alpha} + bu_{\beta} \\
u_{y} & = bu_{\alpha} - au_{\beta}
\end{align}
$$
Substitute this back into the original equation:
$$
\begin{align}
au_{x} + bu_{y} & = a(au_{\alpha} + bu_{\beta}) + b(bu_{\alpha} - au_{\beta}) \\
 & = a^{2} u_{\alpha} + abu_{\beta} + b^{2} - abu_{\beta} \\
 & = (a^{2}+b^{2}) u_{\alpha} \\
 & = 6
\end{align}
$$
I obtain an ODE in terms of $\alpha$, with the solution:
$$
u_{\alpha} = \frac{6}{a^{2}+b^{2}} \implies u = \frac{6\alpha}{a^{2}+b^{2}} + f(\beta)
$$
Swapping back to $(x, y)$ coordinates, the general solution is:
$$
u(x, y) = \frac{6(ax+by)}{a^{2}+b^{2}} + f(bx-ay)
$$
### Question 4
---
a.
Recall that for any given second-order PDE in the form:
$$
au_{xx}+bu_{xy} + cu_{yy} + du_{x} + eu_{y} + fu=0
$$
Then we can classify the PDE according to:
$$
\begin{align}
b^2-4ac<0,  &  & \text{equation is an elliptic} \\
b^2-4ac=0,  &  & \text{equation is a parabolic} \\
b^2-4ac>0,  &  & \text{equation is a hyperbolic}
\end{align}
$$
For this equation we have:
$$
a=1 \qquad b=2 \qquad c=-8
$$
Which yields:
$$
b^{2}-4ac = 2^{2} - 4(1)(-8) = 36
$$
And so this equation is hyperbolic.

---
b.
Factor the equation:
$$
u_{xx} + 2u_{xt} - 8u_{tt} = \left( \frac{ \partial^{2} }{ \partial x^{2} } + 2 \frac{ \partial  }{ \partial x } \frac{ \partial  }{ \partial t } - 8\frac{ \partial^{2} }{ \partial t^{2} }  \right)u = \left( \frac{ \partial  }{ \partial x } -2\frac{ \partial  }{ \partial t }  \right) \left( \frac{ \partial  }{ \partial x } +4 \frac{ \partial  }{ \partial t }  \right)u =0
$$
Yielding two homogeneous equations:
$$
u_{x} -2u_{t} =0 \qquad u_{x} + 4u_{t} =0
$$
Recall that PDEs in the for $au_{x}+bu_{y}=0$ have solutions in the form:
$$
u(x, y) = f(bx-ay)
$$
So these two equation have the solutions:
$$
\begin{align}
u_{x} - 2u_{t} =0 &  \implies u(x, t) = f(-2x-t) \\
u_{x}+4u_{t}=0 & \implies u(x, t) = g(4x-t)
\end{align}
$$
And so I conclude the full general solution to this equation is:
$$
u(x, t) = f(-2x-t) + g(4x-t)
$$
