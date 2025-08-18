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
\frac{1}{2c} \iint_{D} f(y, s) \, dy \, ds
$$
