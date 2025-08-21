### Question 1
This is the Neumann problem for the homogeneous wave equation on a finite line. The solution is in the form:
$$
u(x, t) = \frac{1}{2} c_{0} + \frac{1}{2} d_{0}t + \sum_{n=1}^{\infty} \left( c_{n} \cos\left( \frac{n\pi ct}{l} \right) + d_{n} \sin\left( \frac{n\pi ct}{l} \right) \right)\cos\left( \frac{n\pi x}{l} \right)
$$
The derivative of this function is:
$$
u_{t}(x, t) = \frac{1}{2}d_{0} + \sum_{n=1}^{\infty} \frac{n\pi c}{l} \left( -c_{n} \sin\left( \frac{n\pi ct}{l} \right) + d_{n} \cos\left( \frac{n\pi ct}{l} \right) \right)\cos\left( \frac{n\pi x}{l} \right)
$$
From the initial conditions, $u(x, 0)=0$ implies that $c_{n}=0$ for all values of $n$. From the second initial condition:
$$
u_{t}(x, 0) = \frac{1}{2}d_{0} \sum_{n=1}^{\infty} \frac{n\pi c}{l} d_{n} \cos\left( \frac{n\pi x}{l} \right) = \cos ^{2}(x) = \frac{1}{2} + \frac{1}{2} \cos(2x)
$$
Via coefficient matching, I find that:
$$
\frac{1}{2}d_{0} = \frac{1}{2} \implies d_{0}=1
$$
$$
\frac{n\pi c}{l} d_{n} \cos\left( \frac{n\pi x}{l} \right) = 2c d_{2} \cos(2x) = \frac{1}{2} \cos(2x) \implies 2cd_{2} = \frac{1}{2} \implies d_{2} = \frac{1}{4c}
$$
All other coefficients $d_{n}$ are zero. The full solution can be written out as:
$$
u(x, t) = \frac{t}{2} + \frac{1}{4c} \sin(2ct) \cos(2x)
$$
### Question 2
---
a.
Take derivatives of $v(r, t)$
$$
v_{t}(r, t) = r u_{t}(r, t)
$$
$$
v_{tt}(r, t) = r u_{tt}(r, t)
$$
$$
v_{r}(r, t) = u(r, t) + ru_{r}(r, t)
$$
$$
v_{rr}(r, t) = u_{r}(r, t) + u_{r}(r, t) + r u_{rr}(r, t)
$$
Rearrange to solve for $u_{tt}$ and $u_{rr}$
$$
u_{tt} = \frac{v_{tt}}{r}
$$
$$
ru_{rr} = v_{rr} - 2u_{r} \implies u_{rr} = \frac{1}{r} (v_{rr} - 2u_{r})
$$
Substitute into the original equation:
$$
u_{tt} = c^{2} \left( u_{rr} + \frac{2}{r} u_{r} \right) \implies \frac{v_{tt}}{r} = c^{2} \left( \frac{v_{rr}}{r} - \frac{2}{r}u_{r} + \frac{2}{r}u_{r} \right) = \frac{c^{2}}{r} v_{rr}
$$
Which yields the equation:
$$
v_{tt} - c^{2} v_{rr} =0
$$
As needed.

---
b.
This is the wave equation on the full line. Which has solutions in the form:
$$
u(x, t) = f(x+ct) + g(x-ct)
$$
In this case:
$$
v(r, t) = f(r+ct) + g(r-ct)
$$
---
c.
Directly from the definition of $v$ we have:
$$
v(r, 0) = ru(r, 0) = rf(r)
$$
And,
$$
v_{t}(r, 0) = ru_{t} (r, 0) = rg(r)
$$
---
d.
In spherical coordinates, we require our function to be bounded at $r=0$.

From the general solution for $v$, in combination with the boundary conditions, we obtain the system of equations:
$$
\begin{cases}
v(r, 0) = f(r) + g(r) = rf(r) \\
v_{t}(r, 0) = cf'(r) - cg'(r) = rg(r)
\end{cases}
$$
Integrating both sides of the second function,
$$
cf(r) - cg(r) = G(r)
$$
Where I have defined the new function:
$$
G(r) = \int rg(r)
$$
Multiplying the top equation by $c$, we obtain a new system of equations:
$$
\begin{cases}
cf(r) + cg(r) = crf(r) \\
cf(r) - cg(r) = G(r)
\end{cases}
$$
Adding together and subtracting these equations from each other to solve for $f$ and $g$:
$$
2cf(r) = crf(r) + G(r) \implies (2c-cr)f(r) = G(r) \implies f(r) = \frac{G(r)}{2c-cr}
$$
$$
2cg(r) = crf(r) - G(r) \implies
$$
- Reading over this more, I honestly have no idea what's happening, read over the solutions later
---
### Question 3
From the hint I will search for terms depending on $r$ only. In this case, the Laplacian reduces to:
$$
u_{rr} + \frac{2}{r}u_{r}
$$
And so we have the problem:
$$
u_{xx} + u_{yy} + u_{zz} = \Delta u = u_{rr} + \frac{2}{r}u_{r} = (r^{2}u_{r})_{r} = 1
$$
Solving this ODE,
$$
r^{2} u_{r} = r+A \implies u_{r} = \frac{1}{r} + \frac{A}{r^{2}} \implies u = \ln r -\frac{A}{r} + B
$$
Where $A,B$ are two constants. Applying the boundary conditions, we have:
$$
\begin{align}
\ln a - \frac{A}{a} + B & =0 \\
\ln b - \frac{A}{b} + B & =0
\end{align}
$$
Isolating for $B$ we have:
$$
\begin{align}
B & = \frac{A}{a} - \ln a \\
B & = \frac{A}{b} - \ln b
\end{align}
$$
Solving for $A$:
$$
\frac{A}{a} - \ln a = \frac{A}{b} - \ln b \implies \frac{A}{a} - \frac{A}{b} = A \left( \frac{1}{a} - \frac{1}{b} \right) = \ln a - \ln b
$$
Therefore,
$$
A = \frac{ab}{b-a} \ln\left( \frac{a}{b} \right)
$$
Plugging into one of the equations for $B$ we have:
$$
B = \frac{1}{a} \left( \frac{ab}{b-a}\ln\left( \frac{a}{b} \right) \right) - \ln a = \frac{b}{b-a} \ln\left( \frac{a}{b} \right) - \ln a
$$
- I solved the ODE incorrectly but everything else is correct
### Question 4
---
a.
Assume that the solution will be in the form $X(x)Y(y)$. Then, we have:
$$
X''Y + Y''Y =0 \implies \frac{X''}{X} = - \frac{Y''}{Y} = \lambda
$$
Which yields the eigenvalue problem:
$$
\begin{align}
X'' - \lambda X =0 \\
Y'' + \lambda Y =0
\end{align}
$$
For some constant $\lambda$.

---
b.
Due to the more defined boundary conditions, I will first focus on the problem in the $Y$. The boundary conditions are:
$$
u(x, 0) = Y(0) =0 \qquad u(x, b) = Y(b) =0
$$
Check if the boundary conditions are symmetric. Define two functions $X_{1}$ and $X_{2}$, both of which follow the boundary conditions:
$$
\begin{align}
\left[ X_{1}'X_{2} - X_{1}X_{2}' \right] ^{b}_{0} & = \left[ X_{1}'(b)X_{2}(b) - X_{1}(b)X_{2}'(b) \right] - \left[ X_{1}'(0)X_{2}(0) - X_{1}(0)X_{2}'(0) \right]  \\
 & = (0-0) - (0-0) \\
 & = 0
\end{align}
$$
Therefore, these boundary conditions are symmetric. I will attempt to use the "negative eigenvalue" theorem on the function $X$, which I define to fit the boundary conditions:
$$
\left[ XX' \right] ^{b}_{0} = X(b)X'(b) - X(0)X'(b) = 0-0 \leq 0
$$
So there are no negative eigenvalues.

Check for $\lambda=0$. Then, the eigenvalue problem becomes:
$$
Y'' + \lambda Y = Y'' =0 \implies Y(y) = A+By
$$
From the boundary conditions:
$$
A+B(0) = A =0
$$
$$
A+B(b) = 0 + Bb \implies B=0
$$
Where I have assumed $b>0$ in the second line. I conclude 0 is not an eigenvalue.

Check for $\lambda=\beta^{2}>0$.
$$
Y'' + \beta^{2}Y  =0 \implies Y'' =-\beta^{2}Y \implies Y(y) = A \cos(\beta y) + B \sin(\beta y)
$$
From the boundary conditions:
$$
Y(0) = A \cos(0) + B \sin(0) = A =0
$$
$$
Y(b) = B \sin(\beta b) =0 \implies \sin(\beta b) =0
$$
For this to be true, $\beta b$ must be a multiple of $\pi$.
$$
\beta b = n\pi \implies \beta = \frac{n\pi}{b}
$$
Where $n\in \mathbb{N}$. I conclude that the positive eigenvalues are:
$$
\lambda_{n} = \beta^{2} = \left( \frac{n\pi}{b} \right)^{2}
$$
With the associated eigenfunctions:
$$
Y_{n}(y) = \sin\left( \frac{n\pi y}{b} \right)
$$
Turning my attention to the $X$ part. The eigenvalue problem to solve is:
$$
X'' - \lambda X =0 \implies X'' = \lambda X \implies X(x) = A \cosh(\sqrt{ \lambda }x) + B \sinh(\sqrt{ \lambda }x)
$$
From the boundary conditions:
$$
u(0, y) = X(0) = A \cosh(0) + B \sinh(0) = A =0
$$
Therefore, the eigenfunctions are:
$$
X_{n}(x) = \sinh\left( \frac{n\pi x}{b} \right)
$$
---
c.
Expressing the admissible solutions as a series expansion:
$$
u(x, y) = \sum_{n=1}^{\infty} A_{n} \sinh\left( \frac{n\pi x}{b} \right)\sin\left( \frac{n\pi y}{b} \right)
$$
---
d.
From the last boundary condition, we have:
$$
u(a, y) = \sum_{n=1}^{\infty} A_{n} \sinh\left( \frac{n\pi a}{b} \right)\sin\left( \frac{n\pi y}{b} \right) = f(y)
$$
Which is a Fourier sine series. Therefore, the coefficients are:
$$
\begin{align}
A_{n} \sinh\left( \frac{n\pi a}{b} \right) & = \frac{2}{b} \int_{0}^{b} f(y) \sin\left( \frac{n\pi y}{b} \right) \, dy \\
A_{n} & = \frac{2}{b} \sinh ^{-1}\left( \frac{n\pi a}{b} \right) \int_{0}^{b} f(y) \sin\left( \frac{n\pi y}{b} \right) \, dy 
\end{align}
$$
