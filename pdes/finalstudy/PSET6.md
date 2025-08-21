### Question 1
This problem has been solved in class. The solutions are in the form:
$$
u(r, \theta) = \sum_{n=1}^{\infty} A_{n} r^{n\pi/\beta} \sin\left( \frac{n\pi \theta}{\beta} \right)
$$
And, from the in-homogeneous boundary condition, we have:
$$
\sum_{n=0}^{\infty} A_{n} \left( \frac{n\pi}{\beta} \right) a^{(n\pi/\beta) -1} \sin\left( \frac{n\pi \theta}{\beta} \right) = \theta
$$
Which is a Fourier sine series on the interval $[0, \beta]$. The coefficients are therefore:
$$
A_{n} \left( \frac{n\pi}{\beta} \right) a^{(n\pi/\beta)-1} = \frac{2}{\beta} \int_{0}^{\beta} \theta \sin \left( \frac{n\pi\theta}{\beta} \right) \, d\theta
$$
Evaluate this integral:
$$
\int_{0}^{\beta} \theta \sin\left( \frac{n\pi\theta}{\beta} \right) \, d\theta  = \frac{\beta^{2}(\sin \pi n - \pi n \cos \pi n)}{\pi^{2}n^{2}}
$$
Since $n\in \mathbb{Z}$, $\sin \pi n=0$ for all values, and $\cos \pi n=(-1)^{n}$.
$$
= \frac{\beta^{2}(-\pi n)(-1)^{n}}{\pi^{2}n^{2}} = -\frac{(-1)^{n}\beta^{2}}{\pi n}
$$
Substituting back into the coefficient equation, and solving for $A_{n}$:
$$
\begin{align}
A_{n} & = \left( \frac{\beta}{\pi n} \right) a^{1-(n\pi/\beta)} \left( \frac{2}{\beta} \right) \left( -\frac{(-1)^{n}\beta^{2}}{n\pi} \right) \\
 & = \frac{2(-1)^{n+1}}{n^{2}\pi^{2}} \beta^{2} a^{1-n\pi/\beta}
\end{align}
$$
### Question 2
---
a.
Using $\lambda=0$,
$$
X'' =0 \implies X(x) = A+Bx
$$
It has derivative:
$$
X'(x) = B
$$
From the boundary conditions,
$$
X(0) = A+B(0) = A=0
$$
$$
X'(l) + X(l) = B + B(l) = B(l+1) =0 \implies B=0
$$
Where I have used the fact that $l>0$ in the second line. I conclude that 0 is not an eigenvalue.

---
b.
I intend to use the "negative eigenvalue" theorem to verify this. First, I will check if the boundary conditions are symmetric.

Define two functions $X_{1}$ and $X_{2}$, both of which satisfy the boundary conditions:
$$
\left[ X_{1}'X_{2} - X_{1}X_{2}' \right] ^{l}_{0} = (X_{1}'(l)X_{2}(l) - X_{1}(l)X_{2}'(l)) - (X_{1}'(0)X_{2}(0) - X_{1}(0)X_{2}'(0))
$$
From the boundary conditions, we have:
$$
X'(l) + X(l) =0 \implies X'(l) =- X(l)
$$
Therefore we have:
$$
= \left[ -X_{1}(l)X_{2}(l) + X_{1}(l)X_{2}(l) \right] - \left[ 0-0 \right] = 0-0 =0
$$
So these boundary conditions are symmetric. Define another function $X$ that fits the boundary conditions. Now,
$$
\left[ XX' \right] ^{l}_{0} = X(l)X'(l) - X(0)X'(0) = -X^{2}(l) -0 \leq 0
$$
Since $X^{2}(l)$ will always be a positive value, this is always less than or equal to zero. By the "negative eigenvalue" theorem, there are no negative eigenvalues.

---
c.
Look for positive eigenvalues $\lambda=\beta^{2}>0$. Then,
$$
X'' + \beta^{2}X =0 \implies X(x) = A \cos(\beta x) + B \sin(\beta x)
$$
Which has the derivative:
$$
X'(x) = -A\beta \sin(\beta x) + B \beta \cos(\beta x)
$$
From the boundary conditions:
$$
X(0) = A\cos(0) + B \sin(0) = A =0
$$
And,
$$
B\beta \cos(\beta l) + B \sin(\beta l) =0 \implies \beta \cos(\beta l) =-\sin(\beta l) \implies \beta = - \tan(\beta l)
$$
- I have graphed this before, so I won't graph it again.

Since $\tan(x)$ has asymptotes at $(n+1 /2)\pi$ where $n\in \mathbb{Z}$, there will never be an intersection between these two functions that those points. In this case, the asymptotes will be at:
$$
\beta l = \left( n+\frac{1}{2} \right)\pi \implies \beta = \left( n+\frac{1}{2} \right) \frac{\pi}{l}
$$
Furthermore, I conclude that the interval each eigenvalue will be found is,
$$
\left( \left( n-\frac{1}{2} \right) \frac{\pi}{l} , \left( n+\frac{1}{2} \right) \frac{\pi}{l} \right)
$$
The corresponding eigenfunctions are:
$$
X_{n}(x) = \sin(\beta x)
$$
---
d.
From part B, I have already proven that the boundary conditions are symmetric. A theorem states that,
> For symmetric boundary conditions, any two eigenfunctions that correspond to distinct eigenvalues are orthogonal.

As needed.
### Question 3
This problem has already been solved in class. The solutions are in the form:
$$
u(r, \theta) = \frac{1}{2} A_{0} + \sum_{n=1}^{\infty} r^{-n} (A_{n} \cos(n\theta) + B_{n} \sin(n\theta))
$$
From the boundary condition:
$$
6 + 2 \cos\theta = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} a^{-n} (A_{n} \cos n\theta + B_{n} \sin n\theta)
$$
I will determine the coefficients via coefficient matching.
$$
6 = \frac{1}{2}A_{0} \implies A_{0} = 12
$$
$$
2 \cos \theta = a^{-n} A_{n} \cos n\theta = a^{-1} A_{1} \cos \theta \implies 2=a^{-1} A_{1} \implies A_{1} = 2a
$$
There are no other cosine terms, and there are no sine terms. I conclude that all other coefficients $A_{n}$ and $B_{n}$ are zero. The full series is therefore,
$$
u(r, \theta) = \frac{1}{2} A_{0} + r^{-1} A_{1} \cos \theta = 6 + \frac{2a}{r} \cos \theta
$$
### Question 4
Green's first identity is:
$$
\iiint_{D} v\Delta u \, d\vec{x} = \iint_{\partial D} v \frac{ \partial u }{ \partial n } \, dS - \iiint_{D} \nabla v\cdot \nabla u \, d\vec{x}
$$
Where $u$ and $v$ are any two arbitrary functions defined on the domain $D$.

I will choose $v=1$. Note that:
$$
\nabla v = \left( \frac{ \partial  }{ \partial x } + \frac{ \partial  }{ \partial y } + \frac{ \partial  }{ \partial z }  \right)(1) =0
$$
Green's first identity collapses to:
$$
\iiint_{D} \Delta u \, d\vec{x} = \iint _{\partial D} \frac{ \partial u }{ \partial n } \, dS - 0
$$
Substitute in the properties of $u$ stated in the question:
$$
\iiint _{D} f \, d\vec{x} = \iint_{\partial D} h \, dS
$$
As needed.