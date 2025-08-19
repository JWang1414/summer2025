### Question 1
Define the new coordinate system $y=x-at$ and $s=t$. Then, from chain rule:
$$
u_{t} = \frac{ \partial u }{ \partial y } \frac{ \partial y }{ \partial t } + \frac{ \partial u }{ \partial s } \frac{ \partial s }{ \partial t } = -au_{y} + u_{s}
$$
$$
u_{x} = \frac{ \partial u }{ \partial y } \frac{ \partial y }{ \partial x } + \frac{ \partial u }{ \partial s } \frac{ \partial s }{ \partial x } = u_{y}
$$
$$
u_{xx} = \frac{ \partial u_{x} }{ \partial y } \frac{ \partial y }{ \partial x } + \frac{ \partial u_{x} }{ \partial s } \frac{ \partial s }{ \partial x } = u_{yy}
$$
Substitute back into the original equation:
$$
u_{t} - u_{xx} + au_{x} = -au_{y} + u_{s} - u_{yy} + au_{y} =0 \implies u_{s} = u_{yy}
$$
Which is the diffusion equation $u_{t}=ku_{xx}$ on the whole line with $k=0$. This has the known solution:
$$
u(x, t)=\int_{-\infty}^{\infty} S(x-y)\phi(y) \, dy
$$
Where the initial conditions are $u(x, 0)=\phi(x)$ and $S$ is the source function:
$$
S(x, t) = \frac{1}{\sqrt{ 4\pi kt }} e^{ -x^{2}/4kt }
$$
So, the solution to the problem $u_{s}=u_{yy}$ can be written out as:
$$
u(y, s) = \int_{-\infty}^{\infty} S(y-w)\phi(w) \, dw = \frac{1}{\sqrt{ 4\pi s }} \int_{-\infty}^{\infty} \exp \left\{  -\frac{(y-w)^{2}}{4s}  \right\}\phi(w) \, dw
$$
Returning to the original coordinate system:
$$
u(x, t) = \frac{1}{\sqrt{ 4\pi t }} \int_{-\infty}^{\infty} \exp \left\{  -\frac{(x-at-w)^{2}}{4t}  \right\}\phi(w) \, dw
$$
### Question 2
This is the in-homogeneous wave equation on the whole line. The solutions are in the form:
$$
u(x, t) = \frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right]  + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi(y) \, dy + \frac{1}{2c}\iint_{D} f(y, s) \, dyds
$$
Where the functions $\phi(x)=u(x, 0)$, $\psi(x)=u_{t}(x, 0)$, and $f(x, t)$ is the in-homogeneous source. In this case,
$$
u(x, 0) = e^{ x } = \phi(x) \qquad u_{t}(x, 0) = x = \psi(x) \qquad f(x, t) = t \sin x
$$
I will evaluate the solution in several smaller parts. The first portion is:
$$
\frac{1}{2} \left[ \phi(x+ct) + \phi(x-ct) \right] = \frac{1}{2} \left[ e^{ x+ct } + e^{ x-ct } \right] = \frac{e^{ x }}{2} (e^{ ct } + e^{ -ct }) = e^{ x } \cosh(ct)
$$
The second portion, with the first integral, is
$$
\begin{align}
\frac{1}{2c} \int_{x-ct}^{x+ct} \psi(y) \, dy  & = \frac{1}{2c} \int_{x-ct}^{x+ct} y \, dy = \frac{1}{2c} \frac{y^{2}}{2} \bigg|^{x+ct}_{x-ct} \\
 & = \frac{1}{4c} \left[ (x+ct)^{2} - (x-ct)^{2} \right] \\
 & = \frac{1}{4c} (4ctx) = tx
\end{align}
$$
The third, and last portion, with the second integral, is:
$$
\begin{align}
\frac{1}{2c} \iint_{D} f(y, s) \, dy \, ds & = \int_{0}^{t} \int_{x-c(t-s)}^{x+c(t-s)} f(y, s) \, dy  \, ds  \\
 & = \int_{0}^{t} \int_{x-c(t-s)}^{x+c(t-s)} s \sin y \, dy  \, ds \\
 & = \int_{0}^{t} s \left[ -\cos y \right] ^{x+c(t-s)}_{x-c(t-s)} \, ds  \\
 & = - \int_{0}^{t} s \left[ \cos(x+c(t-s)) - \cos(x-c(t-s)) \right]  \, ds  \\
 & = - \int_{0}^{t} s\left[ -2\sin x \sin(c(t-s)) \right]  \, ds  \\
 & = 2 \sin x \int_{0}^{t} s \sin(c(t-s)) \, ds
\end{align}
$$
I will evaluate this integral separately:
$$
\begin{align}
\int_{0}^{t} s \sin(c(t-s)) \, ds  & = \int_{0}^{t} s \left[ -\cos ct \sin cs + \cos cs \sin ct \right]  \, ds \\
 & = - \cos ct  \int_{0}^{t} s \sin cs \, ds + \sin ct \int_{0}^{t} s \cos cs \, ds  \\
 & = - \cos ct \left[ \frac{\sin ct - ct \cos ct}{c^{2}} \right]  + \sin ct \left[ \frac{ct \sin ct + \cos ct -1}{c^{2}} \right]  \\
 & = \frac{1}{c^{2}} \left[ ct \cos ^{2}ct + ct\sin ^{2}ct - \sin ct \right]  \\
 & = \frac{1}{c^{2}} (ct - \sin ct) = \frac{t}{c} - \frac{\sin ct}{c^{2}}
\end{align}
$$
Therefore,
$$
\frac{1}{2c} \iint_{D} f(y, s) \, dy \, ds = 2 \sin x \left[ \frac{t}{c} - \frac{\sin ct}{c^{2}} \right] = \frac{2}{c^{2}} \sin x (ct-\sin ct)
$$
Substituting these back into the original function:
$$
u(x, t) = e^{ x } \cosh(ct) + tx + \frac{2}{c^{2}} \sin x (ct-\sin ct)
$$
### Question 3
Define the new function $v(x, t)=u(x, t)-(t^{2}+\sin t)$. Then,
$$
v_{t} = u_{t} - (2t+\cos t)
$$
$$
v_{xx} = u_{xx}
$$
$$
v(x, 0) = u(x, 0) -0 = e^{ -x }
$$
$$
v(0, t) = u(0, t) - (t^{2}+\sin t) = t^{2}+\sin t - (t^{2}+\sin t) =0
$$
Transforming the problem into:
$$
\begin{cases}
v_{t} - ku_{xx} = 2t + \cos t - (2t+\cos t) =0 \\
v(x, 0) = e^{ -x } \\
v(0, t) =0
\end{cases}
$$
And so this problem is now the Dirichlet problem for the homogeneous diffusion equation on the half-line. The solution for this problem is:
$$
v(x,t)=\int_{0}^{\infty} \left[ S(x-y, t)-S(x+y, t) \right] \phi(y) \, dy
$$
Where $\phi$ is the initial data $v(x, 0)$, and $S$ is the source function:
$$
S(x, t) = \frac{1}{\sqrt{ 4\pi kt }} e^{ -x^{2}/4kt }
$$
Solve for $v$:
$$
v(x, t) = \int_{0}^{\infty} \left[ S(x-y, t) - S(x+y, t) \right] e^{ -y } \, dy
$$
- I really do not want to do all this algebra again. But you're just supposed to complete the square, solve the integrals, and then you swap from $v$ back to $u$
### Question 4
This is the Dirichlet problem for the wave equation on the finite line. This problem has already been solved in class for a line of any arbitrary length $l$.

The solution takes the form:
$$
u(x, t) = \sum_{n=1}^{\infty} \left[ c_{n} \cos\left( \frac{n\pi ct}{l} \right) + d_{n} \sin\left( \frac{n\pi ct}{l} \right) \right] \sin\left( \frac{n\pi x}{l} \right)
$$
With the coefficients:
$$
c_{n} = \frac{2}{l} \int_{0}^{l} \phi(x)\sin\left( \frac{n\pi x}{l} \right) \, dx
$$
$$
d_{n} = \frac{2}{n\pi c} \int_{0}^{l} \psi(x) \sin\left( \frac{n\pi x}{l} \right) \, dx
$$
In this case, we have:
$$
l=2 \qquad \phi(x) = u(x, 0) = x^{2} \qquad \psi(x) = u_{t}(x, 0) = x \qquad c=1
$$
The solution is therefore:
$$
u(x, t) = \sum_{n=1}^{\infty} \left[ c_{n} \cos\left( \frac{n\pi t}{2} \right) + d_{n} \sin\left( \frac{n\pi t}{2} \right) \right] \sin\left( \frac{n\pi x}{2} \right)
$$
Solve for the coefficients.
$$
c_{n} = \frac{2}{2} \int_{0}^{2} x^{2} \sin\left( \frac{n\pi x}{2} \right) \, dx = \frac{16\pi n \sin(\pi n) + (16-8\pi^{2}n^{2})\cos(\pi n) -16}{\pi^{3}n^{3}}
$$
$$
d_{n} = \frac{2}{n\pi} \int_{0}^{2} x \sin\left( \frac{n\pi x}{2} \right) \, dx = \frac{2}{n\pi} \left[ \frac{4(\sin \pi n - \pi n \cos \pi n)}{\pi^{2}n^{2}} \right]
$$
Since $n\in \mathbb{N}$, $\sin \pi n=0$ for all values of $n$. Furthermore, $\cos \pi n$ alternates between the values 1 and -1.
$$
c_{n} = \frac{(16-8\pi^{2}n^{2})(-1)^{n} -16}{\pi^{3}n^{3}} = \begin{cases}
-8 /\pi n & n \text{ is even} \\
(8\pi^{2}n^{2}-32) /\pi^{3}n^{3} & n\text{ is odd}
\end{cases}
$$
$$
d_{n} = -\frac{8(-1)^{n}}{\pi^{2}n^{2}} = \begin{cases}
-8 /\pi^{2}n^{2} & n\text{ is even} \\
8 /\pi^{2}n^{2} & n\text{ is odd}
\end{cases}
$$
