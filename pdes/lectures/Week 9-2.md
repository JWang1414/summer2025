Example:
Check the validity of the maximum principle for the harmonic function
$$
u(x, y) = \frac{1-x^{2}-y^{2}}{1-2x+x^{2}+y^{2}}
$$
In the disc $\bar{D}=\{ x^{2}+y^{2}\leq 1 \}$. Try factoring:
$$
u(x, y) = \frac{1-x^{2}-y^{2}}{(1-x)^{2}+y^{2}}
$$
And so, by observation, we can tell that $(x, y)\to(1,0)$ does not exist and therefore $u$ is not continuous at one of the points in $\bar{D}$. So, the maximum principle does not apply.

---

### Circles, Wedges, and Annuli
Define a wedge:
$$
\{ 0<\theta<\beta, 0<r<a \}
$$
Exterior of a circle:
$$
\{ a<r<\infty \}
$$
Annulus:
$$
\{ 0<a<r<b \}
$$
All of which may have Dirichlet, Neumann, and Robin boundary conditions

Let us first try with a small triangular shaped wedge. homogeneous Dirichlet conditions on the straight sides, and inhomogeneous Neumann conditions on the curved side.
$$
\begin{cases}
u(r, 0)=u(r, \beta)=0 \\
\frac{ \partial u }{ \partial r } (a, \theta) = h(\theta)
\end{cases}
$$
Begin the separation of variables:
$$
u(r, \theta) = R(r)\Theta(\theta)
$$
With the Laplacian:
$$
u_{rr} + \frac{1}{r}u_{r} + \frac{1}{r^{2}} + u_{\theta\theta} =0
$$
Which gives us:
$$
R''\Theta + \frac{1}{r}R'\Theta + \frac{1}{r^{2}} R\Theta''
$$
Divide the whole thing by $R\Theta$ and multiply by $r^{2}$
$$
r^{2} \frac{R''}{R} + r \frac{R'}{R} + \frac{\Theta''}{\Theta} =0
$$
From which we extract the two ODEs:
$$
\begin{align}
\Theta'' + \lambda\Theta & =0 \\
r^{2} R'' + rR' - \lambda R & =0
\end{align}
$$
From the homogeneous conditions:
$$
\Theta(0) = \Theta(\beta) =0
$$
Looking at the angular equation, we notice that we have previously solved this problem before. It has the solution:
$$
\lambda _{n} = \left( \frac{n\pi}{\beta} \right)^{2} \qquad \Theta_{n}(\theta) = \sin\left( \frac{n\pi \theta}{\beta} \right)
$$
Where $n=1, 2, 3,\dots$

Now, for the radial portion, we attempt to see if the solutions are similar to $r^{\alpha}$
$$
\begin{align}
r^{2} R'' + rR' - \lambda R & =0 \\
r^{2}\alpha(\alpha-1)r^{\alpha-2} + r\alpha r^{\alpha-1} - \lambda r^{\alpha} & =0 \\
\alpha^{2}-\lambda & =0
\end{align}
$$
And so we have the eigenvalues:
$$
\alpha=\pm \sqrt{ \lambda } = \pm \frac{n\pi}{\beta}
$$
With the associated eigenfunctions:
$$
R_{n}(r) = C_{n} r^{n\pi/\beta} + D_{n} r^{-n\pi/\beta}
$$
Remember, at the origin, the solutions must be finite. And so we conclude $r^{-n\pi/\beta}$ cannot be a solution.

Collecting the admissible solutions into an infinite sum:
$$
u(r, \theta) = \sum_{n=1}^{\infty} A_{n} r^{n\pi/\beta} \sin\left( \frac{n\pi \theta}{\beta} \right)
$$
Use the inhomogeneous boundary condition to find:
$$
\sum_{n=0}^{\infty} A_{n} \left( \frac{n\pi}{\beta} \right) a^{(n\pi/\beta) -1} \sin\left( \frac{n\pi \theta}{\beta} \right) =h(\theta)
$$
Which is now a Fourier sin series on the interval $[0, \beta]$. Solving for the coefficients, we have:
$$
A_{n} \left( \frac{n\pi}{\beta} \right)a^{(n\pi/\beta)-1} = \frac{2}{\beta} \int_{0}^{\beta} h(\theta) \sin\left( \frac{n\pi\theta}{\beta} \right) \, d\theta
$$
$$
A_{n} = a^{1-n\pi/\beta} \left( \frac{2}{n\pi} \right) \int_{0}^{\beta} h(\theta) \sin\left( \frac{n\pi\theta}{\beta} \right) \, d\theta
$$
---
Example:
Find the harmonic function $u$ in the semi-disc $\{ r<1, 0<\theta<\pi \}$ with $u$ vanishing on the diameter $(\theta=0, \pi)$ and,
$$
u = \pi \sin \theta-\sin(2\theta)
$$
on $r=1$.

We have just solved this problem, but with $\beta=0$, except the inhomogeneous condition on the curved side is Dirichlet.

The portion of the previous solution that is still valid is:
$$
u(r, \theta) = \sum_{n=1}^{\infty} A_{n} r^{n\pi/\pi} \sin\left( \frac{n\pi\theta}{\pi} \right) = \sum_{n=1}^{\infty} A_{n} r^{n} \sin(n\theta)
$$
Now, use the given boundary condition:
$$
u(1, \theta) = \pi \sin\theta - \sin(2 \theta) = \sum_{n=1}^{\infty} A_{n} \sin(n\theta)
$$
Matching the coefficients we have $A_{1}=\pi$, $A_{2}=-1$, and $A_{n}=0$ for all other $n$. And therefore the full answer is:
$$
u(r, \theta) = \pi r \sin\theta - r^{2} \sin(2\theta)
$$
---

Now for the exterior of a circle.
$$
\begin{cases}
u_{xx} + u_{yy} =0 & x^{2}+y^{2}>a^{2} \\
u = h(\theta) & x^{2}+y^{2}=a^{2}
\end{cases}
$$
Furthermore, we require that solutions are bounded as $r\to \infty$. Since we are going around in a full circle, the typical periodic boundary conditions also apply.

Notice that, in this problem, the progress we made for the circle solution still works. We just need to exclude the correct functions.

Instead of dropping $r^{-n}$, we drop $r^{n}$ instead. So our solutions are:
$$
u(r, \theta) = \frac{1}{2} A_{0} + \sum_{n=1}^{\infty} r^{-n} (A_{n} \cos(n\theta) + B_{n} \sin(n\theta))
$$
Applying the boundary condition $r=a$
$$
h(\theta) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} a^{-n} (A_{n} \cos n\theta + B_{n} \sin n\theta)
$$
Which is the same thing as the full Fourier series. It has known coefficients:
$$
\begin{align}
A_{n} & = \frac{a^{n}}{\pi} \int_{0}^{2\pi} h(\theta) \cos n\theta \, d\theta  \\
B_{n} & = \frac{a^{n}}{\pi} \int_{0}^{2\pi} h(\theta) \sin n\theta \, d\theta 
\end{align}
$$
---
Example:
Solve $u_{xx}+u_{yy}=0$ in the exterior $\{ r>a \}$ of a disc with boundary conditions
$$
u = 1+3\sin\theta
$$
on $r=a$

For the boundary condition we have:
$$
u(a, \theta) = \frac{1}{2} A_{0} + \sum_{n=1}^{\infty} a^{-n} (A_{n}\cos n\theta + B_{n} \sin n\theta)
$$
Coefficient matching, we have: $A_{0}=2$, $B_{1}=3a$ and $A_{n}=B_{n}=0$ for all the rest. The solution is therefore:
$$
u(r, \theta) = 1 + \frac{3a}{r} \sin \theta
$$
---

Now for the annulus. Define the Dirichlet problem:
$$
\begin{cases}
u_{xx} + u_{yy} =0 & 0<a^{2}<x^{2}+y^{2}<b^{2} \\
u = g(\theta) & x^{2}+y^{2} =a^{2} \\
u = h(\theta) & x^{2}+y^{2}=b^{2}
\end{cases}
$$
Separated solutions match the solutions for discs. However, we now require everything in the annulus to be finite. Recall that the solutions were in the form:
$$
u(r, \theta) = \frac{1}{2} (C_{0}+D_{0}\log r) + \sum_{n=1}^{\infty} (C_{n}r^{n} + D_{n}r^{-n})\cos(n\theta) + (A_{n}r^{n} + B_{n}r^{-n})\sin(n\theta)
$$
We cannot throw away these values because they are all finite on the annulus.

For the boundary conditions $g(\theta)$ and $h(\theta)$, you would simply substitute $r=a$ and $r=b$ into the above equation. This is very long so I didn't write it out.

However, for the coefficients, you will find they look like:
$$
A_{n}a^{n} + B_{n} a^{-n} = \frac{1}{\pi} \int_{0}^{2\pi} g(\theta)\sin n\theta \, d\theta
$$
$$
C_{n}a^{n} + D_{n} a^{-n} = \frac{1}{\pi} \int_{0}^{2\pi} g(\theta)\cos n\theta \, d\theta
$$
$$
A_{n}b^{n} + B_{n} b^{-n} = \frac{1}{\pi} \int_{0}^{2\pi} h(\theta)\sin n\theta \, d\theta
$$
$$
C_{n}b^{n} + D_{n} b^{-n} = \frac{1}{\pi} \int_{0}^{2\pi} h(\theta)\cos n\theta \, d\theta
$$
Which is a system of four equations with four unknowns. You will find, for $n=0$:
$$
\begin{cases}
\frac{1}{2}(C_{0}+D_{0} \log a) = \frac{1}{\pi}\int_{0}^{2\pi} g(\theta) \, d\theta  \\
\frac{1}{2}(C_{0}+D_{0} \log R \frac{1}{\pi}\int_{0}^{2\pi} h(\theta) \, d\theta
\end{cases}
$$
---
Example:
Solve the Dirichlet problem:
$$
\begin{cases}
u_{xx} + u_{yy} =0 & 1<r<2 \\
u = \sin ^{2}\theta  & r=1 \\
u=0 & r=2
\end{cases}
$$
We obtain:
$$
u(2, \theta) = \frac{1}{2} (C_{0}+D_{0} \log_{2}) + \sum_{n=1}^{\infty} (C_{n} 2^{n} + D_{n}2^{-n})\cos n\theta + (A_{n}2^{n} + B_{n}2^{-n})\sin n\theta =0
$$
Which gives us the equalities:
$$
C_{0}+D_{0} \log 2 =0 \qquad D_{n} = -4^{n}C_{n} \qquad B_{n} = -4^{n} A_{n}
$$
Furthermore the other condition gives us:
$$
u(1, \theta) = \frac{D_{0}}{2} \log\left( \frac{1}{2} \right) + \sum_{n=1}^{\infty} (1-4^{n})(C_{n} \cos n\theta + A_{n} \sin n\theta) = \sin ^{2}\theta = \frac{1}{2} - \frac{1}{2} \cos(2\theta)
$$
Solving for the coefficients, you should find:
$$
u(r, \theta) = \frac{1}{2} \left( 1 - \frac{\log r}{\log 2} \right) + \frac{1}{30} (r^{2} - 16 r^{-2}) \cos(2\theta)
$$