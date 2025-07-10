### Question 1
---
a.
For this equation we have:
$$
\begin{align}
a=1 &  & b=1 &  & c=-20
\end{align}
$$
We are interested in the value of:
$$
b^{2}-4ac = 1^{2} - 4(1)(-20) = 81 > 0
$$
Which implies that this equation is hyperbolic

---
b.
Factor this problem into:
$$
\left( \frac{ \partial  }{ \partial x } +5 \frac{ \partial  }{ \partial t }  \right)\left( \frac{ \partial  }{ \partial x } -4 \frac{ \partial  }{ \partial t }  \right)u =0
$$
The problem has now been split into two identical PDEs, both of which can be solved with the geometric method. I will use $\xi \in \mathbb{R}$ as an arbitrary constant.
$$
u_{x} + \xi u_{t}=0 = \begin{bmatrix}
1 \\
\xi
\end{bmatrix} \cdot \nabla u =0
$$
In this form, for some vector $[a, b]$, the characteristic curves will be along the line $bx-at=c$ for some constant $c$. Therefore:
$$
\begin{bmatrix}
a \\
b
\end{bmatrix} = \begin{bmatrix}
1 \\
\xi
\end{bmatrix} \implies bx-at = \xi x - t = c
$$
And so the general solution for this problem is:
$$
u(x, t) = f(5x-t) + g(-4x-t)
$$
---
c.
$$
u(x, 0) = f(5x) + g(-4x) = x
$$
$$
u_{t} = -f_{t}(5x-t) - g_{t}(-4x-t) \implies u_{t}(x, 0) = -f_{t}(5x) - g_{t}(-4x) = e^{ x }
$$
- No clue how to solve this system of equations
---
### Question 2
Compute $u_{tt}$ and $u_{xx}$
$$
\begin{align}
u_{tt} & = \frac{ \partial^{2} }{ \partial t^{2} } e^{ ikx }e^{ -i\omega t } = e^{ ikx } \frac{ \partial^{2} }{ \partial t^{2} } e^{ -i\omega t } = -\omega^{2} e^{ i(kx-\omega t) } = -\omega^{2} u(x, t) \\
u_{xx} & = \frac{ \partial^{2} }{ \partial x^{2} } e^{ ikx }e^{ -i\omega t } = e^{ -i\omega t } \frac{ \partial^{2} }{ \partial x^{2} } e^{ ikx } = -k^{2} e^{ i(kx-\omega t) } = -k^{2}u(x, t)
\end{align}
$$
Substitute into the original equation
$$
\begin{align}
u_{tt} - c^{2}u_{xx} + m^{2}u & = (-\omega^{2}u) - c^{2} (-k^{2}u) + m^{2}u \\
 & = -\omega^{2}u + (ck)^{2}u + m^{2}u \\
 & = (c^{2}k^{2} - \omega^{2} + m^{2})u \\
 & = 0
\end{align}
$$
Dividing both sides by $u$, I obtain:
$$
(ck)^{2}-\omega^{2}+m^{2}=0
$$
- Don't know how to progress from here
---
### Question 3
