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
