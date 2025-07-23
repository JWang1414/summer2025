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
### Question 3
In spherical coordinates, the Laplacian becomes:
$$
\Delta = \frac{1}{r^{2}} \frac{ \partial  }{ \partial r } \left( r^{2} \frac{ \partial  }{ \partial r } \right) + \frac{1}{r^{2} \sin \theta} \frac{ \partial  }{ \partial \theta } \left( \sin \theta \frac{ \partial  }{ \partial \theta }  \right) + \frac{1}{r^{2} \sin ^{2}\theta} \frac{ \partial^{2} }{ \partial \phi^{2} }
$$
Assuming the solution depends only on $r$, this simplifies into:
$$
\Delta = \frac{1}{r^{2}} \frac{ \partial  }{ \partial r } \left( r^{2} \frac{ \partial  }{ \partial r }  \right) = \frac{ \partial^{2} }{ \partial r^{2} }  + \frac{2}{r} \frac{ \partial  }{ \partial r }
$$
Based on the solution function $u$ define the new function $v=u_{r}$. The above has become an ODE:
$$
u_{xx} + u_{yy} + u_{zz} = \Delta u = u_{rr} + \frac{2}{r}u_{r} = v_{r} + \frac{2}{r} v =1
$$
Which has the solution:
$$
v(r) = \frac{A}{r^{2}} + \frac{1}{3}r \implies u(r) = \int \frac{A}{r^{2}} + \frac{r}{3} \, dr = C-\frac{A}{r} + \frac{r^{2}}{6}
$$
Where $C$ is the integration constant. Apply the boundary conditions:
$$
\begin{cases}
u(a) = C - \frac{A}{a} + \frac{a^{2}}{6} = 0 \\
u(b) = C - \frac{A}{b} + \frac{b^{2}}{6} =0
\end{cases}
$$
Solve for $A$ by equating these two equations:
$$
-\frac{A}{a} + \frac{a^{2}}{6} = -\frac{A}{b} + \frac{b^{2}}{6} \implies A\left( \frac{1}{b} - \frac{1}{a} \right) = \frac{1}{6} (b^{2}-a^{2}) \implies A = -\frac{1}{6} ab(a+b)
$$
The new boundary conditions are:
$$
\begin{cases}
u(a) = C + \frac{1}{6}b(a+b) + \frac{a^{2}}{6} =0 \\
u(b) = C + \frac{1}{6}a(a+b) + \frac{b^{2}}{6} =0
\end{cases}
$$
Solve for $C$ by adding these two equations together:
$$
2C + \frac{1}{6}b(a+b) + \frac{1}{6}a(a+b) + \frac{a^{2}}{6} + \frac{b^{2}}{6} =0 \implies C = \frac{1}{6}(a^{2}+ab+b^{2})
$$
And therefore the solution is:
$$
u(r) = C - \frac{A}{r} + \frac{r^{2}}{6} = \frac{1}{6}(a^{2}+ab+b^{2}+r^{2}) + \frac{1}{6r}(a^{2}b + ab^{2})
$$
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
Resulting in the corresponding eigenfunction:
$$
X_{n}(x) = \sinh\left( \frac{n\pi x}{b} \right)
$$
---
c.
Combining the $X_{n}(x)$ and $Y_{n}(y)$ terms into a summation results in:
$$
u(x, y) = \sum_{n=1}^{\infty} A_{n} \sinh\left( \frac{n\pi x}{b} \right) \sin\left( \frac{n\pi y}{b} \right)
$$
---
d.
Applying the final boundary condition:
$$
u(a, y) = f(y) = \sum_{n=1}^{\infty} A_{n} \sinh\left( \frac{n\pi a}{b} \right)\sin\left( \frac{n\pi y}{b} \right)
$$
Which reduces the series expansion into a Fourier sine series. This has the coefficients:
$$
\begin{align}
A_{n} \sinh\left( \frac{n\pi a}{b} \right) & = \frac{2}{b} \int_{0}^{b} f(y)\sin\left( \frac{n\pi y}{b} \right) \, dy \\
A_{n} & = \frac{2}{b} \sinh ^{-1}\left( \frac{n\pi a}{b} \right) \int_{0}^{b} f(y) \sin\left( \frac{n\pi y}{b} \right) \, dy 
\end{align}
$$
