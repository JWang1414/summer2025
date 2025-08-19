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
This is the Dirichlet problem for the homogeneous wave equation on the finite line. The solutions for this problem follow the form:
$$
u(x, t) = \sum_{n=1}^{\infty} \left[ c_{n} \cos\left( \frac{n\pi ct}{l} \right) + d_{n} \sin\left( \frac{n\pi ct}{l} \right) \right] \sin\left( \frac{n\pi x}{l} \right)
$$
I will solve for the coefficients via coefficient matching. The initial functions must follow the form:
$$
\phi(x) = \sum_{n=1}^{\infty} c_{n} \sin\left( \frac{n\pi x}{l} \right) \qquad \psi(x) = \sum_{n=1}^{\infty} \frac{n\pi c}{l} d_{n} \sin\left( \frac{n\pi x}{l} \right)
$$
Where $\phi(x)=u(x, 0)$ and $\psi(x)=u_{t}(x, 0)$. Substituting into these formulae,
$$
\sin\left( \frac{2\pi x}{l} \right) = \sum_{n=1}^{\infty} c_{n} \sin\left( \frac{n\pi x}{l} \right) \implies \sin\left( \frac{2\pi x}{l} \right) = c_{2} \sin\left( \frac{2\pi x}{l} \right) \implies c_{2}=1
$$
$$
\begin{align}
\sin\left( \frac{3\pi x}{l} \right) & = \sum_{n=1}^{\infty} \frac{n\pi c}{l} d_{n} \sin\left( \frac{n\pi x}{l} \right) \\
\sin\left( \frac{3\pi x}{l} \right) & = \frac{3\pi c}{l} d_{3} \sin\left( \frac{3\pi x}{l} \right) \\
d_{3} & = \frac{l}{3\pi c}
\end{align}
$$
All other coefficients must be zero. The full solution can be written:
$$
\begin{align}
u(x, t) & = c_{2} \cos\left( \frac{2\pi ct}{l} \right) \sin\left( \frac{2\pi x}{l} \right) + d_{3} \sin\left( \frac{3\pi ct}{l} \right) \sin\left( \frac{3\pi x}{l} \right) \\
 & = \cos\left( \frac{2\pi ct}{l} \right) \sin\left( \frac{2\pi x}{l} \right) + \frac{l}{3\pi c} \sin\left( \frac{3\pi ct}{l} \right) \sin\left( \frac{3\pi x}{l} \right)
\end{align}
$$
### Question 4
---
a.
Assume that solutions are in the for $X(x)T(t)$. Then, the PDE becomes:
$$
X(x)T'(t)=kX''(x)T(t) \implies -\frac{T'(t)}{kT(t)} = -\frac{X''(x)}{X(x)} = \lambda
$$
Which yields the eigenvalue problem:
$$
\begin{align}
X''+\lambda X & = 0 \\
T'+\lambda kT & = 0
\end{align}
$$
---
b.
I will begin with the comparatively simpler $X$ eigenvalue problem.

Check if the boundary conditions are symmetric. Define $X_{1}$ and $X_{2}$ as two functions which satisfy the boundary conditions. Then,
$$
[X_{1}'X_{2} - X_{1}X_{2}']^{\pi}_{0} = X_{1}'(\pi)X_{2}(\pi) - X_{1}(\pi)X_{2}'(\pi) - (X_{1}'(0)X_{2}(0) - X_{1}(0)X_{2}'(0))
$$
According to the boundary conditions, we have $X'(0)=X(\pi)=0$ and therefore the above collapses into:
$$
= 0-0-(0-0) =0
$$
I conclude that these boundary conditions are symmetric. Now, I will attempt to apply the "negative eigenvalue" theorem.
$$
[XX']^{\pi}_{0} = X(\pi)X'(\pi) - X(0)X'(0) = 0-0 \leq 0
$$
By the negative eigenvalue theorem, there are no negative eigenvalues.

Check for $\lambda=0$. Then, the problem becomes:
$$
X'' =0 \implies X(x) = A+Bx
$$
From the boundary conditions:
$$
u_{x}(0, t) = X'(0) = B=0
$$
$$
u(\pi, t) = X(\pi) = A+B\pi = A+0 =0 \implies A=0
$$
Both $A$ and $B$ are zero, so I conclude that 0 is not an eigenvalue.

Check for $\lambda=\beta^{2}>0$. Then, the problem becomes:
$$
X'' + \beta^{2}X =0 \implies X(x) = A \cos(\beta x) + B \sin(\beta x)
$$
$$
X'(x) = -A\beta \sin(\beta x) + B\beta \cos(\beta x)
$$
From the boundary conditions:
$$
X'(0) = -A\beta \sin(0) + B \beta \cos(0) = B\beta =0 \implies B=0
$$
$$
X(\pi) = A \cos(\beta \pi) =0 \implies \cos(\beta \pi)=0
$$
I conclude that $\beta=n + 1 /2$ where $n\in \mathbb{N}$. The eigenvalues are therefore,
$$
\lambda_{n} = \left( n+\frac{1}{2} \right)^{2}
$$
With the associated eigenfunctions:
$$
X_{n}(x) = \cos \left[ \left( n+\frac{1}{2} \right)x \right]
$$
For the temporal part. We have:
$$
T' + \lambda kT =0 \implies T' =-\lambda kT \implies T(t) = e^{ -\lambda kt } = \exp \left\{  -\left( n+\frac{1}{2} \right)^{2}kt  \right\}
$$
---
Collecting all the admissible solutions into a series expansion:
$$
u(x, t) = \sum_{n=1}^{\infty} A_{n} \cos\left( \left( n+\frac{1}{2} \right)x \right) \exp \left\{  -\left( n+\frac{1}{2} \right)^{2}kt  \right\}
$$
---
From the initial conditions:
$$
u(x, 0) = \sum_{n=1}^{\infty} A_{n} \cos\left( \left( n+\frac{1}{2} \right)x \right) = \phi(x)
$$
Which is a Fourier cosine series on the interval $[0, \pi]$. The coefficients are:
$$
A_{n} = \frac{2}{\pi} \int_{0}^{\pi} \phi(x) \cos\left( \left( n+\frac{1}{2} \right)x \right) \, dx
$$
