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
Since $f(x)$ and $g(x)$ are both single variable equations, their derivatives are simply:
$$
u_{t}(x, t) = -f'(5x-t) - g'(-4x-t) \implies u_{t}(x, 0) = -f'(5x) - g'(-4x) = e^{ x }
$$
Integrate the newly obtained equation:
$$
\begin{align}
- \int f'(5x) + g'(-4x) \, dx & = \int e^{ x } \, dx  \\
-\left[ \frac{1}{5} f(5x) + \left( -\frac{1}{4} \right) g(-4x) \right]  & = e^{ x } \\
-\frac{1}{5} f(5x) + \frac{1}{4} g(-4x)  & = e^{ x }
\end{align}
$$
So, we now have the system of equations:
$$
\begin{cases}
f(5x) + g(-4x) = x \\
-\frac{1}{5} f(5x) + \frac{1}{4} g(-4x) = e^{ x }
\end{cases}
$$
Solving this system of equations:
$$
f(5x) = \frac{5}{9} (x - 4e^{ x }) \qquad g(-4x) = \frac{4}{9} (x + 5e^{ x })
$$
And therefore, in terms of the original variables
$$
f(5x-t) = \frac{5}{9} \left( x - \frac{t}{5} - 4e^{ (5x-t)/5 } \right) \qquad 
g(-4x-t) = \frac{4}{9} \left( x+\frac{t}{4} + 5e^{ (4x+t)/4 } \right)
$$
Plugging back into the original equation:
$$
u(x, t) = \frac{5}{9} \left( x - \frac{t}{5} - 4e^{ (5x-t)/5 } \right) + \frac{4}{9} \left( x+\frac{t}{4} + 5e^{ (4x+t)/4 } \right)
$$
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
$k$ and $\omega$ expressed in terms of each other are:
$$
k = \pm \sqrt{ \frac{\omega^{2}-m^{2}}{c^{2}} } \qquad \omega = \pm \sqrt{ (ck)^{2}+m^{2} }
$$
---
### Question 3
I recognize this as the homogeneous Dirichlet conditions for the wave equation. In this case:
$$
u(x, 0) = \phi(x) = \sin \left( \frac{2\pi x}{l} \right) \qquad u_{t}(x, 0) = \psi(x) = \sin \left( \frac{3\pi x}{l} \right)
$$
Recall the solutions are expressed in the form:
$$
u(x, t) = \sum_{n=1}^{\infty} \left( A_{n} \cos\left( \frac{n\pi ct}{l} \right) + B_{n} \sin\left( \frac{n\pi ct}{l} \right) \right) \sin\left( \frac{n\pi x}{l} \right)
$$
With
$$
\phi(x) = \sum_{n=1}^{\infty} A_{n} \sin\left( \frac{n\pi x}{l} \right)
$$
$$
\psi(x) = \sum_{n=0}^{\infty} \frac{n\pi c}{l} B_{n} \sin\left( \frac{n\pi x}{l} \right)
$$
Substituting in the given conditions:
$$
\phi(x) = \sin\left( \frac{2\pi x}{l} \right) = \sum_{n=0}^{\infty} A_{n} \sin\left( \frac{n\pi x}{l} \right) \implies A_{2}=1
$$
$$
\psi(x) = \sin\left( \frac{3\pi x}{l} \right) = \sum_{n=0}^{\infty} \frac{n\pi c}{l} B_{n} \sin\left( \frac{n\pi x}{l} \right) \implies \frac{3\pi c}{l}B_{3} =1 \implies B_{3} = \frac{l}{3\pi c}
$$
All other coefficients $A_{n}=B_{n}=0$. Hence, the full solution can be written as:
$$
u(x, t) = \cos\left( \frac{2\pi ct}{l} \right) \sin\left( \frac{2\pi x}{l} \right) + \frac{l}{3\pi c} \sin\left( \frac{3\pi ct}{l} \right) \sin\left( \frac{3\pi x}{l} \right)
$$
### Question 4
---
a.
Look for separated solutions of the PDE in the form $u(x, t)=X(x)T(t)$. Substituting into the PDE:
$$
X(x)T'(t) - kX''(x)T(t) =0 \implies \begin{cases}
X'' + \lambda X =0 \\
T' + \lambda kT =0
\end{cases}
$$
Where $\lambda$ is some constant.

---
b.
Focusing on the spatial equation, check for eigenvalues when $\lambda=0$. Then, the problem is: $X''=0$. Which has solutions:
$$
X = Ax+B
$$
The boundary conditions state that:
$$
u_{x}(0, t) =0 \implies X'(0) = A = 0
$$
And,
$$
u(\pi, t) =0 \implies X(\pi) = A\pi + B = 0 + B=0
$$
Since $A=B=0$, I conclude that $\lambda=0$ is not an eigenvalue.

Check for $\lambda=-\gamma^{2}<0$. The problem becomes $X''-\gamma^{2}X=0$. Which has solutions:
$$
X = A \cosh(\gamma x) + B \sinh(\gamma x)
$$
The boundary conditions state that:
$$
u_{x}(0, t) = 0 \implies X'(0) = A \sinh(0) + B \cosh(0) = B=0
$$
And,
$$
u(\pi, t) =0 \implies X(\pi) = A \cosh(\gamma \pi) + B \sinh(\gamma \pi) \implies A=0
$$
I conclude that there are no negative eigenvalues.

Check for $\lambda=\beta^{2}>0$. The problem becomes $X''+\beta^{2}X=0$. Which has solutions:
$$
X = A \sin(\beta x) + B \cos(\beta x)
$$
The boundary conditions state that:
$$
u_{x}(0, t) =0 \implies X'(0) = \beta (A \cos (0) - B \sin(0)) \implies A=0
$$
And,
$$
u(\pi, t) =0 \implies X(\pi) = B \cos(\beta \pi) \implies \cos(\beta \pi) =0
$$
I conclude there there are positive eigenvalues such that:
$$
\beta = n + \frac{1}{2} \implies \lambda = \beta^{2} = \left( n + \frac{1}{2} \right)^{2}
$$
With the eigenfunctions
$$
X_{n}(x) = \cos\left( \left( n+\frac{1}{2} \right)x \right)
$$
For the temporal part, the equation to solve is:
$$
T' + \left( n+\frac{1}{2} \right)^{2} kT =0 \implies T(t) = c_{n} \exp \left[ -\left( n+\frac{1}{2} \right)^{2}kt \right]
$$
---
c.
The full solution can be expressed as:
$$
u(x, t) = \sum_{n=1}^{\infty} X_{n}(x)T_{n}(x) = \frac{c_{0}}{2} + \sum_{n=1}^{\infty} c_{n} \exp \left[ -\left( n+\frac{1}{2} \right)^{2}kt \right] \cos\left( \left( n+\frac{1}{2} \right)x \right)
$$
---
d.
From the boundary conditions:
$$
u(x, 0) = \phi(x) = \sum_{n=1}^{\infty} c_{n} \cos\left( \left( n+\frac{1}{2} \right)x \right)
$$
Which has the coefficients:
$$
c_{n} = \frac{2}{\pi} \int_{0}^{\pi} \phi(x) \cos\left( \left( n+\frac{1}{2} \right)x \right) \, dx
$$
