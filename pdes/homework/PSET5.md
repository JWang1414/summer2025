### Question 1
I recognise this as the wave equation with homogeneous Neumann boundary conditions.

Recall, on the finite line, the full solution for this problem is:
$$
u(x, t) = \frac{c_{0}}{2} + \frac{d_{0}}{2}t + \sum_{n=1}^{\infty} \left[ c_{n} \cos\left( \frac{n\pi ct}{l} \right) + d_{n} \sin\left( \frac{n\pi ct}{l} \right) \right] \cos\left( \frac{n\pi x}{l} \right)
$$
With the initial conditions:
$$
\phi(x) = \frac{c_{0}}{2} + \sum_{n=1}^{\infty} c_{n} \cos\left( \frac{n\pi x}{l} \right)
$$
$$
\psi(x) = \frac{d_{0}}{2} + \sum_{n=1}^{\infty} d_{n} \left( \frac{n\pi c}{l} \right) \cos\left( \frac{n\pi x}{l} \right)
$$
From our conditions, we have:
$$
\begin{align}
u(x, 0) = \phi(x) =0 &  & u_{t}(x, 0) = \psi(x) = \cos ^{2}(x) &  & l=\pi
\end{align}
$$
Substituting this into the initial conditions:
$$
\phi(x) = \frac{c_{0}}{2} + \sum_{n=1}^{\infty} c_{n} \cos\left( \frac{n\pi x}{l} \right) =0
$$
From which I can see $c_{n}=0$ for all $n$. A trigonometric identity to the given $\psi(x)$ function:
$$
\begin{align}
\psi(x) & = \cos ^{2}(x) = \frac{1}{2} + \frac{1}{2} \cos(2x) \\
 & = \frac{d_{0}}{2} + \sum_{n=1}^{\infty} d_{n} \left( \frac{n\pi c}{l} \right) \cos\left( \frac{n\pi x}{l} \right) \\
 & = \frac{d_{0}}{2} + \sum_{n=1}^{\infty} d_{n} (nc) \cos(nx)
\end{align}
$$
Matching the coefficients, I find that $d_{0}=1$ and $d_{2}=1 /4c$. All other values of $d_{n}=0$. Therefore, the full solution can be written out as:
$$
u(x, t) = \frac{1}{2}t + \frac{1}{4c} \sin(2ct) \cos(2x)
$$
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
Pretty sure this is just the wave equation on the half-line with Neumann conditions. Since $v(r=0)$ must be finite and $v_{r}(r=0)$ must be zero in order for it to be symmetric around $r=0$.

However, the question is worded a little strangely and so I don't know if this is what I'm supposed to do

The rest of this question looks pretty straight forward
### Question 3



### Question 4
---
a.
Define the separated equation: $u(x, y) = X(x)Y(y)$. The problem is now:
$$
u_{xx} + u_{yy} = X''(x)Y(y) + X(x)Y''(y) =0
$$
Which yields the eigenvalue problem:
$$
\frac{X''}{X} = -\frac{Y''}{Y} = -\lambda
$$
For some constant $\lambda$. Written out as a series of equations:
$$
\begin{align}
X'' + \lambda X=0 \\
Y'' - \lambda Y =0
\end{align}
$$
---
b.
Start with the equation in terms of $Y$.

Check for $\lambda=0$
$$
Y'' =0 \implies C+Dy=0
$$
From boundary conditions:
$$
Y(0) = C =0 \qquad Y(b) = Db =0
$$
Therefore $C=D=0$ and 0 is not an eigenvalue.

Check for $\lambda=\beta^{2}>0$
$$
Y'' - \beta^{2}Y =0 \implies Y = C \cosh(\beta y) + D\sinh(\beta y) =0
$$
From boundary conditions:
$$
Y(0) = C \cosh(0) + D \sinh(0) = C =0
$$
$$
Y(b) = D \sinh(\beta b) =0 \implies D=0
$$
Therefore $C=D=0$ and there are no positive eigenvalues.

Check for $\lambda=-\gamma^{2}<0$
$$
Y'' + \gamma^{2}Y =0 \implies Y = C \cos(\gamma y) + D \sin(\gamma y) =0
$$
From boundary conditions:
$$
Y(0) = C \cos(0) + D \sin(0) = C =0
$$
$$
Y(b) = D \sin (\gamma b) =0
$$
Which implies that $\gamma b$ must be an integer multiple of $\pi$.
$$
\gamma b = n\pi \implies \gamma = \frac{n\pi}{b}
$$
Where $n=1, 2, 3, \dots$

Therefore, we have the eigenvalues:
$$
\lambda_{n} = - \left( \frac{n\pi}{b} \right) ^{2}
$$
With the eigenfunctions:
$$
Y_{n}(y) = \sin\left( \frac{n\pi y}{b} \right)
$$
For the other variable, the problem to solve is:
$$
X'' + \lambda X = X'' - \gamma^{2} X =0
$$
Which has solutions:
$$
X = A \cosh(\gamma_{n}x) + B \sinh(\gamma_{n}x)
$$
From the boundary conditions:
$$
X(0) = A \cosh(0) + B \sinh(0) = A =0
$$
$$
X(a) = B \sinh(\gamma_{n}a) = f(y) \implies B = \frac{\sinh(\gamma_{n}a)}{f(y)}
$$
Resulting in the corresponding eigenfunction:
$$
X_{n}(x) = \frac{1}{f(y)} \sinh\left( \frac{n\pi a}{b} \right) \sinh\left( \frac{n\pi x}{b} \right)
$$
---
c.
$$
u(x, y) = \sum_{n=1}^{\infty} \frac{A_{n}}{f(y)} \sinh\left( \frac{n\pi a}{b} \right) \sinh\left( \frac{n\pi x}{b} \right) \sin\left( \frac{n\pi y}{b} \right)
$$
---
d.
