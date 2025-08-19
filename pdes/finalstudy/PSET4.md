### Question 1
---
a.
We are interested in determining the value of:
$$
b^{2}-4ac
$$
Where, in this case, we have:
$$
a=1 \qquad b=1 \qquad c=-20
$$
Therefore,
$$
b^{2}-4ac = (1) - 4(1)(-20) = 1 + 4(20) >0
$$
And so this equation is hyperbolic.

---
b.
Factor the operator:
$$
u_{xx} + u_{xt} -20 u_{tt} = \left( \frac{ \partial  }{ \partial x } +5 \frac{ \partial  }{ \partial t }  \right) \left( \frac{ \partial  }{ \partial x } -4 \frac{ \partial  }{ \partial t }  \right)u =0
$$
Define the new variables $\alpha=5x-t$ and $\beta=4x+t$. Then, from chain rule, we have:
$$
u_{x} = \frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial x } + \frac{ \partial u }{ \partial \beta } \frac{ \partial \beta }{ \partial x } = 5u_{\alpha} + 4u_{\beta}
$$
$$
u_{t} = \frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial t } + \frac{ \partial u }{ \partial \beta } \frac{ \partial \beta }{ \partial t } = -u_{\alpha} + u_{\beta}
$$
Therefore, we have:
$$
\left( \frac{ \partial  }{ \partial x } + 5 \frac{ \partial  }{ \partial t }  \right) = 5u_{\alpha} + 4u_{\beta} + 5(-u_{\alpha} + u_{\beta}) = 9u_{\beta}
$$
$$
\frac{ \partial  }{ \partial x } -4 \frac{ \partial  }{ \partial t } = 5u_{\alpha} + 4u_{\beta} - 4(-u_{\alpha} + u_{\beta}) = 9 u_{\alpha}
$$
And so the equation is simplified into:
$$
9^{2} u_{\alpha \beta} =0 \implies u_{\alpha \beta} =0 \implies u(\alpha, \beta) = f(\alpha) + g(\beta)
$$
Converting back into the original coordinate system:
$$
u(x, t) = f(5x-t) + g(4x+t)
$$
---
c.
Directly applying the boundary conditions, I obtain:
$$
u(x, 0) = f(5x) + g(4x) = x
$$
And,
$$
u_{t} = -f'(5x-t) + g'(4x+t) \implies u_{t}(x, 0) = -f'(5x) + g'(4x) = e^{ x }
$$
Integrating both sides,
$$
-\frac{1}{5} f(5x) + \frac{1}{4} g(4x) = e^{ x }
$$
Which yields the system of equations:
$$
\begin{cases}
f(5x)+g(4x)=x \\
-\frac{1}{5}f(5x) + \frac{1}{4}g(4x) = e^{ x }
\end{cases}
$$
Solve for $g$ by adding them together:
$$
f(5x)+g(4x) + 5 \left[ -\frac{1}{5}f(5x) + \frac{1}{4}g(4x) \right] = \frac{9}{4} g(4x) = x + 5e^{ x }
$$
Solve for $f$ by subtracting the two:
$$
f(5x)+g(4x) - 4 \left[ -\frac{1}{5}f(5x) + \frac{1}{4}g(4x) \right] = \frac{9}{5} f(5x) = x - 4e^{ x }
$$
Swap back to the original coordinate system:
$$
\frac{9}{5} f(w) = \frac{w}{5} - 4e^{ w/5 } \implies f(5x-t) = \frac{5}{9} \left[ \frac{5x-t}{5} - 4e^{ (5x-t)/5 } \right]
$$
$$
\frac{9}{4} g(w) = \frac{w}{4} + 5e^{ w/4 } \implies g(4x+t) = \frac{4}{9} \left[ \frac{4x+t}{4} + 5e^{ (4x+t)/4 } \right] 
$$
---
### Question 2
We are looking for solutions in the form $u(x, t)=e^{ i(kx-\omega t) }$. First I will compute the derivatives of this function:
$$
u_{tt} = \frac{ \partial^{2} }{ \partial t^{2} } e^{ ikx }e^{ -i\omega t } = e^{ ikx } \frac{ \partial^{2} }{ \partial t^{2} } e^{ -i\omega t } = -\omega^{2} e^{ i(kx-\omega t) }
$$
$$
u_{xx} = \frac{ \partial^{2} }{ \partial x^{2} } e^{ ikx }e^{ -i\omega t } = e^{ -i\omega t } \frac{ \partial^{2} }{ \partial x^{2} } e^{ ikx } = -k^{2} e^{ i(kx-\omega t) }
$$
Substitute into the function:
$$
\begin{align}
u_{tt} + c^{2}  u_{xx} + m^{2}u & = -\omega^{2} e^{ i(kx-\omega t) } + c^{2} (-k^{2} e^{ i(kx-\omega t) }) + m^{2} (e^{ i(kx-\omega t) }) \\
 & = e^{ i(kx-\omega t) } \left[ -\omega^{2} + c^{2}(-k^{2}) + m^{2} \right] =0
\end{align}
$$
Then,
$$
-\omega^{2} - c^{2}k^{2} + m^{2} =0 \implies m^{2} = \omega^{2} + c^{2}k^{2}
$$
Solving specifically for $\omega$ and $k$ yields:
$$
\omega = \pm \sqrt{ m^{2}-(ck)^{2} } \qquad k = \pm \frac{\sqrt{ m^{2}-\omega^{2} }}{c}
$$
### Question 3
