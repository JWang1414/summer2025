Example:
Find the solutions that depend only on $r$ of:
$$
u_{xx} + u_{yy} + u_{zz} = k^{2}u, \qquad k \text{ is a positive constant}
$$
That is, we seek the solution $u(r, \theta, \phi) = u(r)$. Additionally, note that $u = k /r$
$$
u_{rr} + \frac{2}{r}u_{r}=k^{2}u
$$
Let $v=ru$
$$
v_{r}=ru_{r} + u, \qquad v_{rr}=ru_{rr}+2u_{r}
$$
$$
u_{r}= \frac{v_{r}}{r} - \frac{u}{r} = \frac{v_{r}}{r} - \frac{v}{r^{2}}
$$
$$
u_{rr} = \frac{v_{rr}}{r} - \frac{2u_{r}}{r} = \frac{v_{rr}}{r} - \frac{2v_{r}}{r^{2}} + \frac{2v}{r^{3}}
$$
$$
u_{rr} + \frac{2}{r}u_{r} = \frac{v_{rr}}{r} - \frac{2v_{r}}{r^{2}} + \frac{2v}{r^{3}} + 2
\frac{v_{r}}{r^{2}} - \frac{2v}{r^{3}} = \frac{v_{rr}}{r}
$$
$$
\frac{v_{rr}}{r} = k^{2} \left( \frac{v}{r} \right) \Rightarrow v_{rr} = k^{2}v
$$
$$
v = A \cosh(kr) + B\sinh(kr)
$$
Final answer:
$$
u = \frac{1}{r} (A\cosh(kr) + B\sinh(kr))
$$
---

### Rectangles
- Certain geometries can be solved via separation of variables
- The general procedure for rectangles is similar to chapter 4

1. Look for separated solutions to the PDE
2. Put in homogeneous boundary conditions to get eigenvalues
3. Sum the series
4. Put in homogeneous (initial) boundary conditions to get coefficients

Let $D$ be the rectangle $\{ 0<x<a : 0<y<b \}$. Lets solve $u_{xx}+u_{yy}=0$ in $D$ with boundary conditions..
- There is a drawing of the boundary conditions over here, but I can't really read it quickly

Separate variables: $u(x, y) = X(x)Y(y)$
$$
\begin{align}
X''Y + XY'' & =0 \\
\frac{X''}{X} + \frac{Y''}{Y} & =0 \\
\frac{X''}{X} = -\frac{Y''}{Y} & =-\lambda
\end{align}
$$
Therefore we have two ODEs $X''+\lambda X=0$ and $Y''-\lambda Y=0$ for some constant $\lambda$

We will begin with the boundary conditions: $u(0, y)=0$ and $u_{x}(a, y)=0$
$$
X(0)=0, X'(a)=0
$$
Check for $\lambda=0$
$$
X''=0\Rightarrow X(x) = C+Dx
$$
From the boundary conditions:
$$
X(0)=C=0, \qquad X'(a)=D=0
$$
And so 0 is not an eigenvalue

Check for $\lambda=-\gamma^{2}<0$
- Recall we have a theorem to check for negative eigenvalues now, but we will try to do it the normal way

We obtain the ODE
$$
X''=\gamma^{2}X \Rightarrow X(x) = C \cosh(\gamma x) + D \sinh(\gamma x)
$$
From the boundary conditions:
$$
X(0)=C=0 \Rightarrow \begin{cases}
X(x) = D \sinh(\gamma x) \\
X'(x) = \gamma D \cosh(\gamma x)
\end{cases}
$$
$$
X'(a) = \gamma D \cosh(\gamma a) = 0
$$
Which implies that $D=0$, so there are no negative eigenvalues

Check for $\lambda=\beta^{2}>0$

We obtain the ODE:
$$
X''=-\beta^{2}X \Rightarrow X(x) = C \cos(\beta x) + D \sin(\beta) \Rightarrow X'(x) = -C\beta \sin(\beta x) + \beta D \cos(\beta x)
$$
From the boundary conditions:
$$
X(0)=C=0, \qquad X'(a) = \beta D \cos(\beta a)=0
$$
Which gives us the condition that $\cos(\beta a)=0$ and therefore
$$
\beta a = \left( n+\frac{1}{2} \right)\pi
$$
Where $n=0, 1, 2, \dots$

Therefore, we have the eigenvalues:
$$
\lambda_{n} = \left[ \frac{(n + 1 /2)\pi}{a} \right] ^{2}
$$
With the eigenfunctions
$$
X_{n}(x) = \sin\left( \frac{(n+1 /2)\pi x}{a} \right)
$$
Where $n=0, 1, 2, \dots$

Now move onto the other variable $y$. We have the equation $Y''=\lambda Y$ with $\lambda$ as above.
$$
Y(y) = A \cosh(\beta_{n}y) + B \sinh(\beta_{n}y)
$$
We have the boundary conditions:
$$
u_{y}(x, 0) + u(x, 0)=0 \Rightarrow Y'(0) + Y(0)=0
$$
Which gives us:
$$
B \beta_{n} + A=0 \Rightarrow B = -\frac{A}{\beta_{n}}
$$
And solutions:
$$
u(x, y) = \sum_{n=0}^{\infty} A_{n}\sin(\beta_{n}x) \left[ \beta_{n} \cosh(\beta_{n}y) - \sinh(\beta_{n}y) \right]
$$
Our final, remaining condition is that $u(x, b)=g(x)$
$$
g(x) = \sum_{n=0}^{\infty} A_{n} \left( \beta_{n} \cosh(\beta_{n}b) - \sinh(\beta_{n}b) \right) \sin(\beta_{n}x)
$$
Notice that $b$ is a constant, so the entire portion at the front is a coefficient. We have:
$$
A_{n} \left[ \beta_{n}\dots \right] = \frac{2}{a} \int_{0}^{a} g(x) \sin(\beta_{n}x) \, dx
$$
---
Example: Find a harmonic function in the square $D=\{ 0<x<\pi , 0<y<\pi \}$ with boundary conditions:
$$
\begin{cases}
u_{y}(x, 0) = u_{y}(x, \pi)=0 \\
u(0, y) =0 \\
u(\pi, y) = \frac{1}{2}(1+\cos(2y))
\end{cases}
$$
Through the same separation of variables technique, we obtain:
$$
u(x, y) = X(x)Y(y) \Rightarrow X''=\lambda X \text{ and }Y''=-\lambda Y
$$
Now, plugging in the $Y$ equations for the boundary conditions:
$$
\begin{cases}
Y'(0) = Y'(\pi) =0 \\
Y'' = -\lambda Y
\end{cases}
$$
We have seen these boundary conditions before, and we know the solution is:
$$
\lambda_{n} = \left( \frac{n\pi}{\pi} \right)^{2}=n^{2}
$$
$$
Y_{n}(y) = \cos\left( \frac{n\pi y}{\pi} \right) = \cos ny
$$
Where $n \in \mathbb{N}$. Now check for $X$. Substitute the eigenvalues into the ODE:
$$
X'' = n^{2}X \Rightarrow X(x) = A \cosh(nx) + B \sinh(nx)
$$
Use the boundary condition $u(0, y)=0 \Rightarrow X(0)=0$
$$
X(0)=A=0 \Rightarrow X_{n}(x) = \sinh(nx)
$$
And for the eigenvalue 0:
$$
X''=0 \Rightarrow X(x) = Ax+B
$$
$$
X(0)=B=0 \Rightarrow X_{0}(x)=x
$$
Therefore we have the expansion
$$
u(x, y) = A_{0}x + \sum_{n=1}^{\infty} A_{n} \sinh(nx) \cos(ny)
$$
Apply the final boundary condition:
$$
u(\pi, y) = \frac{1}{2} (1+\cos(2y))
$$
Which gives us:
$$
A_{0} \pi = \frac{1}{2} \Rightarrow A_{0} = \frac{1}{2\pi}
$$
$$
A_{2} \sinh(2\pi) = \frac{1}{2} \Rightarrow A_{2} = \frac{1}{2\sinh(2\pi)}
$$
And all other $A_{n}=0$. Final answer:
$$
u(x, y) = \frac{1}{2\pi}x + \frac{1}{2\sinh(2\pi)} \sinh(2x) \cos(2y)
$$
### Poisson's Formula
Dirichlet problem for a circle
$$
\begin{cases}
u_{xx} + u_{yy} = 0 & \text{for }x^{2}+y^{2}<a^{2} \\
u=h(0) & \text{for }x^{2}+y^{2}=a^{2}
\end{cases}
$$
Separation of variables: $u(r, \theta) = R(r)\Theta(\theta)$

Furthermore:
$$
u_{xx} + u_{yy} = u_{rr} + \frac{1}{r}u_{r} + \frac{1}{r^{2}}u_{\theta \theta} = 0
$$
$$
R''\Theta + \frac{1}{r}R'\Theta + \frac{1}{r^{2}}R\Theta''
$$
Divide by $R\Theta$, multiply by $r^{2}$
$$
r^{2} \frac{R''}{R} + \frac{rR'}{R} + \frac{\Theta''}{\Theta} = 0
$$
$$
r^{2} \frac{R''}{R} + r \frac{R'}{R} = -\frac{\Theta''}{\Theta} = \lambda
$$
Which gives us two ODEs:
$$
\begin{cases}
\Theta'' + \lambda\Theta =0 \\
r^{2} R'' + rR' - \lambda R=0
\end{cases}
$$
Hidden boundary conditions, because of the interpretation of $\theta$
$$
\Theta(0) = \Theta(2\pi) \qquad \Theta'(0) = \Theta'(2\pi)
$$
Applying the "negative eigenvalue theorem" we can conclude there are no negative eigenvalues

Check for $\lambda=0$

Therefore $\Theta''=0 \Rightarrow \Theta(\theta) = C+D\theta$
$$
C = c+D(2\pi) \Rightarrow D=0
$$
$$
\Theta'(0) = \Theta'(2\pi) = 0
$$
Which means we have any arbitrary choice of $C$. Hence, 0 is an eigenvalue, and the eigenfunctions are any constant.

Check for $\lambda = \beta^{2}>0$
$$
\Theta'' = -\beta^{2}\Theta \Rightarrow \begin{cases}
\Theta(\theta) = C \cos(\beta \theta) + D \sin(\beta \theta) \\
\Theta'(\theta) = -\beta C \sin(\beta\theta) + \beta D \cos(\beta\theta)
\end{cases}
$$
$$
\begin{align}
C  & = C \cos(2\pi \beta) + D \sin(2\pi \beta) \\
\beta D  & = -\beta C \sin(2\pi \beta) + \beta D \cos(2\pi \beta)
\end{align}
$$
Which gives us
$$
\cos(2\pi \beta)=1 \qquad \sin(2\pi \beta)=0
$$
Where $\beta=n$ and $n\in \mathbb{Z}^{>0}$. We therefore have the eigenvalues and eigenfunctions:
$$
\lambda_{n} = n^{2}, \Theta_{n}(\theta) = A_{n} \cos(n\theta) + B_{n} \sin(n\theta)
$$
$$
\lambda_{0}=0, \Theta_{0}(\theta) = A_{0}
$$
---
Aside: The Euler Equation
$y = y(x)$ has the general form $ax^{2}y'' + bxy' + cy=0$

Guess the solution has the form $y=x^{m}$ and solve for $m$

Try it for $x^{2}y'' - xy' - 3y=0$

Now, substitute $y=x^{m}$ into this ODE:
$$
x^{2} m(m-1)x^{m-2} - xmx^{(m-1)} - 3x^{m}= m(m-1)x^{m} - mx^{m} - 3x^{m}=0
$$
And therefore we obtain:
$$
m^{2}-2m-3 = (m-3)(m+1)=0
$$
So $m=3, -1$

The general solution is given by $y(x) = c_{1}x^{3} + c_{2}x ^{-1}$

---

For $n\in \mathbb{Z}^{>0}$, the radial part becomes:
$$
r^{2} R'' + r R' - n^{2} R =0
$$
Test the solution $R(r) = r^{\alpha}$ and from this we obtain:
$$
\alpha^{2}=n^{2} \Rightarrow \alpha = \pm n
$$
And hence the general solution is:
$$
R_{n}(r) = C_{n}r^{n} + D_{n} r^{-n}
$$
Hidden boundary conditions from $R$:
- Solutions are finite for $r=0$

Because $r^{-n}\to \infty$ as $r\to 0$ this cannot be part of the solution and $D_{n}=0$

For $n=0$ / $\lambda=0$
$$
r^{2} R'' + r R' =0
$$
Which has the solution
$$
R_{0}(r) = C_{0} + D_{0} \ln(r)
$$
Note that $\ln$ blows up at 0 so $D_{0}=0$

Collecting all of this and combining the two separated solutions:
$$
u(r, \theta) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} r^{n} (A_{n} \cos(n\theta) + B_{n} \sin(n\theta))
$$
And finally apply the second given boundary equation. The one at $r=a$
$$
h(\theta) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} a^{n} (A_{n} \cos(n\theta) + B_{n} \sin(n\theta))
$$
Which we recognize as is the full Fourier series for $h(\theta)$
$$
\begin{align}
A_{n}  & = \frac{1}{a^{n}\pi} \int_{0}^{2\pi} h(\phi) \cos(n\phi) \, d\phi \\
B_{n} & = \frac{1}{a_{n}\pi} \int_{0}^{2\pi} h(\phi ) \sin(n\phi) \, d\phi 
\end{align}
$$
Curiously, if we directly plug in these integral representations of $A_{n}$ and $B_{n}$ into $u(r, \theta)$:
$$
u(r, \theta) = \frac{a^{2}-r^{2}}{2\pi} \int_{0}^{2\pi} \frac{h(\phi)}{a^{2} - 2ar \cos(\theta_{0}\phi) + r^{2}} \, d\phi
$$
This is Poisson's formula
- Expresses any harmonic function inside a circle in terms of its boundary values
- Exact, without any summations
