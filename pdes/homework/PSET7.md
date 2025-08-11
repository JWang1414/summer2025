### Question 2
This function is the Gaussian multiplied by a polynomial. Recall that for any arbitrary function $h(x)$,
$$
\mathcal{F}\{ xh(x) \} = i \frac{d\hat{h}(k)}{dk}
$$
Define the function $g(x)=e^{ -ax^{2}/2 }$, then,
$$
f(x) = xe^{ -ax^{2}/2 } = xg(x) \implies \hat{f}(k) = \mathcal{F}\{ xg(x) \} = i \frac{d\hat{g}(k)}{dk}
$$
$g(x)$ is simply a Gaussian function, which is invariant under the Fourier transform. I will apply the property:
$$
h(x) = e^{ -\alpha x^{2} } \implies \hat{h}(k) = \sqrt{ \frac{\pi}{\alpha} } e^{ -k^{2}/4\alpha }
$$
For any arbitrary constant $\alpha>0$. For the function $g(x)$, $\alpha=a /2$, valid since $a>0$. Therefore,
$$
\hat{g}(k) = \sqrt{ \frac{\pi}{(a /2)} } e^{ -k^{2}/4(a /2) } = \sqrt{ \frac{2\pi}{a} } e^{ -k^{2}/2a }
$$
I conclude that the Fourier transform of $f(x)$ is:
$$
\hat{f}(k) = i \frac{d\hat{g}(k)}{dk} = i \sqrt{ \frac{2\pi}{a} } \frac{d}{dk} e^{ -k^{2}/2a } = -\frac{\sqrt{ 2\pi }ik}{a^{3/2}} e^{ -k^{2}/2a }
$$
### Question 3
Expand the Laplace operator:
$$
\begin{cases}
u_{xx} + u_{yy} =0 \\
u(x, 0) = g(x)
\end{cases}
$$
Take the Fourier transform of both side in terms of $x$. Start with the PDE:
$$
\widehat{u_{xx}} + \widehat{u_{yy}} = (ik)^{2} \hat{u} + \hat{u}_{yy} = -k^{2} \hat{u} + \hat{u}_{yy} =0
$$
Now, the boundary conditions:
$$
\hat{u}(k, 0) = \hat{g}(k)
$$
Which has the solution:
$$
\hat{u}(k, y) = A(k) e^{ -|k|y } + B(k) e^{ |k|y }
$$
We are interested in a bounded solution for $u(x, y)$, and therefore $B(k)=0$. From the boundary conditions:
$$
\hat{u}(k, 0) = A(k) e^{ 0 } = A(k) = \hat{g}(k)
$$
Invert the function:
$$
\mathcal{F}^{-1}\left\{ \hat{g}(k)e^{ -|k|y } \right\} = (g*f)(x, y) = (f*g)(x, y)
$$
Since, under the Fourier transform, convolution is:
$$
\widehat{(a*b)}(k) = \hat{a}(k)\hat{b}(k)
$$
For any two arbitrary functions $a$ and $b$. Furthermore, I have defined the function:
$$
\hat{f} = e^{ -|k|y } \implies f = \mathcal{F}^{-1} \left\{ e^{ -|k|y } \right\} = \frac{1}{2\pi} \frac{2y}{y^{2}+x^{2}} = \frac{y}{\pi(x^{2}+y^{2})}
$$
Hence,
$$
u(x, y) = (f*g)(x, y) = \frac{1}{\pi} \int_{-\infty}^{\infty} \frac{y}{y^{2}+(x-z)^{2}} g(z) \, dz
$$
### Question 1
---
a.
Assume solutions are in the form $u=R(r)\Theta(\theta)$. The Laplace equation becomes:
$$
R''\Theta + \frac{1}{r} R'\Theta + \frac{1}{r^{2}} R\Theta'' =0 \implies r^{2} \frac{R''}{R} + r \frac{R'}{R} + \frac{\Theta''}{\Theta} =0
$$
Eigenvalue problem:
$$
\begin{align}
\Theta'' + \lambda\Theta & =0 \\
r^{2} R'' + rR' - \lambda R & =0
\end{align}
$$
---
b.
I will begin with the comparatively simpler eigenvalue problem for $\theta$.

Check for $\lambda=0$. The problem becomes:
$$
\Theta'' =0 \implies \Theta(\theta) = A\theta + B
$$
According to the boundary conditions:
$$
\Theta(0) = \Theta(\pi) =0
$$
Therefore,
$$
A(0) + B = B=0
$$
$$
A(\pi) + B = A\pi =0 \implies A=0
$$
I conclude 0 is not an eigenvalue.

Check for $\lambda=-\gamma^{2}<0$. The problem becomes:
$$
\Theta'' - \gamma^{2} \Theta =0 \implies \Theta(\theta) = A \cosh(\gamma\theta) + B \sinh(\gamma\theta)
$$
From the boundary conditions:
$$
\Theta(0) = A \cosh(0) + B \sinh(0) = A =0
$$
$$
\Theta(\pi) = A \cosh(\gamma\pi) + B \sinh(\gamma\pi) = B \sinh(\gamma\pi) =0 \implies B=0
$$
Where I have assumed $\gamma \neq 0$. I conclude there are no negative eigenvalues.

Check for $\lambda=\beta^{2}>0$. The problem becomes:
$$
\Theta'' + \beta^{2} \Theta =0 \implies \Theta(\theta) = A \cos(\beta\theta) + B \sin(\beta\theta)
$$
From the boundary conditions:
$$
\Theta(0) = A \cos(0) + B \sin(0) = A =0
$$
$$
\Theta(\pi) = A \cos(\beta \pi) + B \sin(\beta \pi) = B \sin(\beta \pi) =0 \implies \sin(\beta \pi) =0
$$
$\sin(\beta \pi)=0$ implies that $\beta \in \mathbb{N}$, and so the positive eigenvalues are $\lambda=n^{2}$ where $n\in \mathbb{N}$. With the associated eigenfunctions:
$$
\Theta_{n}(\theta) = \sin(n\theta)
$$
For the radial portion, check for solutions in the for $r^{\alpha}$:
$$
\begin{align}
r^{2} R'' + r R' - \lambda R & =0 \\
r^{2} \alpha(\alpha-1)r^{\alpha-2} + r\alpha r^{\alpha-1} - \lambda r^{\alpha} & =0 \\
\alpha(\alpha-1)r^{\alpha} + \alpha r^{\alpha} - \lambda r^{\alpha} & =0 \\
\alpha^{2} - \lambda & =0
\end{align}
$$
And so the eigenvalues are:
$$
\alpha^{2} = \lambda \implies \alpha = \pm \sqrt{ \lambda } = \pm \sqrt{ n^{2} } = \pm n
$$
With the associated eigenfunctions:
$$
R_{n}(r) = C_{n} r^{n} + D_{n}r^{-n}
$$
Where I have introduced the two arbitrary constants $C_{n}$ and $D_{n}$. From the first radial boundary condition:
$$
u(1, \theta)  =0 \implies R_{n}(1) = C_{n}1^{n} + D_{n}1^{-n} = C_{n} + D_{n} =0 \implies C_{n} =-D_{n}
$$
And so the eigenfunctions can be simplified into:
$$
R_{n}(r) = C_{n} \left( r^{n} - r^{-n} \right)
$$
---
c.
Collecting the admissible solutions into a series expansion:
$$
u(r, \theta) = \sum_{n=1}^{\infty} R_{n}(r)\Theta_{n}(\theta) = \sum_{n=1}^{\infty} C_{n} \left( r^{n} - r^{-n} \right) \sin(n\theta)
$$
---
d.
Using the last boundary condition:
$$
u(2, \theta) = \sum_{n=1}^{\infty} C_{n} \left( 2^{n}- 2^{-n} \right) \sin(n\theta) = \pi-\theta
$$
Which is now a Fourier sine series on the interval $[0, \pi]$. Which has the known coefficients:
$$
C_{n} \left( 2^{n}-2^{-n} \right) = \frac{2}{\pi} \int_{0}^{\pi} (\pi-\theta) \sin(n\theta) \, d\theta
$$
This integral can be solved analytically. First, by linearity:
$$
\int_{0}^{\pi} (\pi-\theta) \sin(n\theta) \, d\theta = \pi \int_{0}^{\pi} \sin(n\theta) \, d\theta - \int_{0}^{\pi} \theta \sin(n\theta) \, d\theta
$$
Use integration by parts on the second integral:
$$
\begin{align}
 & = \pi \int_{0}^{\pi} \sin(n\theta) \, d\theta - \left[ -\frac{\theta}{n} \cos(n\theta) \bigg|_{0}^{\pi}  + \frac{1}{n} \int_{0}^{\pi}  \cos(n\theta) \, d\theta  \right]  \\
 & = \pi \int_{0}^{\pi} \sin(n\theta) \, d\theta + \frac{\theta}{n} \cos(n\theta)\bigg|_{0}^{\pi}  - \frac{1}{n} \int_{0}^{\pi} \cos(n\theta) \, d\theta
\end{align}
$$
This first integral is:
$$
\int_{0}^{\pi} \sin(n\theta) \, d\theta = -\frac{1}{n} \cos(n\theta) \bigg|_{0}^{\pi} = \frac{1-\cos(\pi n)}{n}
$$
The second is:
$$
\int_{0}^{\pi} \cos(n\theta) \, d\theta = \frac{1}{n} \sin)(n\theta) \bigg|_{0}^{\pi}  = \frac{\sin(\pi n)}{n}
$$
Therefore,
$$
\begin{align}
\int_{0}^{\pi} (\pi-\theta) \sin(n\theta) \, d\theta  & = \pi \left[ \frac{1-\cos(\pi n)}{n} \right] + \frac{\pi}{n} \cos(\pi n) -0 - \frac{1}{n} \left[ \frac{\sin(\pi n)}{n} \right]  \\
 & = \frac{\pi}{n} - \frac{\pi}{n} \cos(\pi n) + \frac{\pi}{n} \cos(\pi n) - \frac{\sin(\pi n)}{n^{2}} \\
 & = \frac{\pi}{n} - \frac{\sin(\pi n)}{n^{2}}
\end{align}
$$
Since $n\in \mathbb{N}$, $\sin(\pi n)=0$ for all $n$, and so I conclude:
$$
\int_{0}^{\pi} (\pi-\theta) \sin(n\theta) \, d\theta = \frac{\pi}{n}
$$
Substituting this back into the coefficient formula,
$$
C_{n} \left( 2^{n}-2^{-n} \right) = \frac{2}{\pi} \left[ \frac{\pi}{n} \right]  = \frac{2}{n} \implies C_{n} = \frac{2}{n(2^{n}-2^{-n})}
$$
