### Question 1
This is a problem that has been solved in class before. The solution is in the form:
$$
u(r, \theta) = \sum_{n=1}^{\infty} A_{n} r^{n\pi/\beta} \sin\left( \frac{n\pi \theta}{\beta} \right)
$$
The coefficients can be determined from the boundary condition:
$$
\frac{ \partial u }{ \partial r } (a, \theta) = \sum_{n=0}^{\infty} A_{n} \left( \frac{n\pi}{\beta} \right) a^{(n\pi/\beta) -1} \sin\left( \frac{n\pi \theta}{\beta} \right) = \theta
$$
Which is now a Fourier sine series on the interval $[0, \beta]$ with the known coefficients:
$$
\begin{align}
A_{n} \left( \frac{n\pi}{\beta} \right)a^{(n\pi/\beta)-1} & = \frac{2}{\beta} \int_{0}^{\beta} \theta \sin\left( \frac{n\pi\theta}{\beta} \right) \, d\theta \\
A_{n} & = a^{1-n\pi/\beta} \left( \frac{2}{n\pi} \right) \int_{0}^{\beta} \theta \sin\left( \frac{n\pi\theta}{\beta} \right) \, d\theta
\end{align}
$$
### Question 2
---
a.
Substituting $\lambda=0$ into the problem:
$$
X'' + \lambda X = X'' =0 \implies X(x) = Ax+B
$$
From the boundary conditions:
$$
X(0) = B =0
$$
$$
X'(l) + X(l) = \left[ A \right] + \left[ Al+0 \right] = A(l+1) =0 \implies A=0
$$
Where I have assumed $l>0$ in the second line. I conclude that $\lambda=0$ is not an eigenvalue.

---
b.
Substituting $\lambda=-\gamma^{2}<0$ into the problem:
$$
X'' + \lambda X = X''-\gamma^{2}X =0 \implies X(x) = A\cosh(\gamma x) + B \sinh(\gamma x)
$$
From the boundary conditions:
$$
X(0) = A \cosh(0) + B \sinh(0) = A =0
$$
$$
X'(l) + X(l) = \left[ \gamma B \cosh(\gamma l) \right] + \left[ B \sinh(\gamma l) \right] =0 \implies B=0
$$
Where I have assumed $l>0$ in the second line. I conclude that there are no negative eigenvalues.

---
c.
Substituting $\lambda=\beta^{2}>0$ into the problem:
$$
X'' + \lambda X = X'' + \beta^{2}X =0 \implies X(x) = A\sin(\beta x) + B\cos(\beta x)
$$
From the boundary conditions:
$$
X(0) = A\sin(0) + B \cos(0) = B =0
$$
$$
\begin{align}
X'(l) + X(l) & = \left[ \beta A \cos(\beta l) \right] + \left[ A \sin(\beta l) \right] =0 \\
 & \implies \beta A \cos(\beta l) = -A\sin(\beta l) \\
 & \implies -\beta = \frac{\sin(\beta l)}{\cos (\beta l)} = \tan(\beta l)
\end{align}
$$
Therefore the eigenvalues are the intersections between the two functions $\beta$ and $-\tan(\beta l)$. This implies that there is an endless sequence of positive eigenvalues $\lambda_{n}=\beta^{2}_{n}$ along the positive real values where $n \in \mathbb{N}$. The corresponding eigenfunctions are:
$$
X(x) = \sin(\beta_{n} x)
$$
REMEMBER TO INCLUDE A GRAPH HERE

---
d.
According to Theorem 1 on page 120 of Strauss:
> For symmetric boundary conditions, any two eigenfunctions that correspond to distinct eigenvalues are orthogonal.

A set of boundary conditions is symmetric if:
$$
f'(x)g(x) - f(x)g'(x) \big|^{x=b}_{x=a} =0
$$
For any pair of functions $f$ and $g$ both of which satisfy the boundary conditions. In this case, the boundary conditions are defined on the interval from 0 to $l$, so the problem becomes:
$$
f'(x)g(x) - f(x)g'(x) \big|^{x=l}_{x=0} = f'(l)g(l) - f(l)g'(l) - \left[ f'(0)g(0) - f(0)g'(0) \right]
$$
Applying the boundary conditions, $X(0)=0$ and $X'(l)=-X(l)$, this becomes:
$$
-f(l)g(l) - f(l)\left[ -g(l) \right] -0 = f(l)g(l) - f(l)g(l) =0
$$
And therefore this set of boundary conditions is symmetric, and I conclude that the eigenfunctions corresponding to different eigenvalues are orthogonal.
### Question 3
This problem has already been solved in class. The solutions are:
$$
u(r, \theta) = \frac{1}{2} A_{0} + \sum_{n=1}^{\infty} r^{-n} (A_{n} \cos(n\theta) + B_{n} \sin(n\theta))
$$
Applying the boundary condition $r=a$ yields,
$$
6 + 2\cos \theta = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} a^{-n} (A_{n} \cos n\theta + B_{n} \sin n\theta)
$$
The boundary condition has no dependence on sine, and so I conclude that $B_{n}=0$ for all $n$. I will use coefficient matching to solve for $A_{n}$:
$$
6 = \frac{1}{2}A_{0} \implies A_{0}=12
$$
$$
2 \cos \theta = a^{-1} A_{1} \cos \theta \implies 2 = \frac{1}{a} A_{1} \implies A_{1} = 2a
$$
This fully satisfies the boundary condition, and so I conclude that all other coefficients $A_{n}$ are 0. The full solution can therefore be written:
$$
u(r, \theta) = \frac{1}{2}A_{0} + r^{-1}A_{1} \cos \theta = 6 + \frac{2a}{r} \cos \theta
$$
### Question 4
Recall Green's first identity:
$$
\iiint_{D} v\Delta u \, d\vec{x} = \iint_{\partial D} v \frac{ \partial u }{ \partial n } \, dS - \iiint_{D} \nabla v\cdot \nabla u \, d\vec{x}
$$
Which is valid for any two functions $u$ and $v$. Define $v=1$ and therefore $\nabla v=\vec{0}$. Green's first identity becomes:
$$
\iiint_{D} \Delta u \, d\vec{x} = \iint_{\partial D} \frac{ \partial u }{ \partial n } \, dS - \iiint_{D} \vec{0}\cdot \nabla u \, d\vec{x} = \iint_{\partial D} \frac{ \partial u }{ \partial n } \, dS
$$
Applying the Neumann conditions, where $\Delta u=f$ and $\frac{ \partial u }{ \partial n }=h$,
$$
\iiint_{D} f \, d\vec{x} = \iint_{\partial D} h \, dS
$$
As required.
