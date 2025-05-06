THINGS TO KNOW
- 1st order linear ODEs
- 2nd order linear ODEs
- Boundary value problems for both

Examples

1.

Solve IVP $y'+2y=te^{ -2t }, y(1)=0$

$y'+p(x)y=g(t)$

$\mu = e^{ \int p } = e^{ 2t }$

$y = \frac{1}{\mu} \left[ \int \mu g + C\right] = e^{ -2t }\left[ e^{ 2t } t e^{ -2t } + C \right] = \left( \frac{t^2}{2} + C \right)e^{ -2t }$

$y(1) = \left( \frac{1}{2} + C \right) e^{ -2 } = 0\Rightarrow C=-\frac{1}{2}$

2.

$y'' + 5y'1 + 6y=0$

$y = C_{1} e^{ -2t } + C_{2}e^{ -3t }$

3.

$y'' + y=0$, $y(0)=0$, $y'(\pi/2)=1$

We have $y = C_{2} \sin x$ and $y' = C_{2} \cos x$

You will find that the boundary conditions are incompatible with each other

### Introduction
As opposed to ODEs, there will be more than one independent variable in PDEs $(x,y,z, \dots)$
- This should come as no surprise
- The solution, or dependent variable, is a function $u(x, y, z, \dots)$
	- Satisfies the equation, at least in some region of the $(x, y, z, \dots)$ variables
The *order* of a PDE is the order of the highest derivative which appears in the question
- $u_{x} + u_{y} = 0$ is of order 1
- $u_{x x} + u_{yy} = 0$ is of order 2
Subscript notation:
$$
\begin{align}
\frac{ \partial u }{ \partial x } = u_{x} &  & \frac{ \partial u }{ \partial y } = u_{y}
\end{align}
$$
The typical PDE is structured as
$$
\mathcal{L}(u) = g(x, y, z, \dots)
$$
Where $\mathcal{L(u)}$ is all terms containing $u$ and its derivatives. $\mathcal{L}$ is some operator composed of derivatives. $g(x, y, z, \dots)$ is a stand in for all terms involving only the independent variables

Examples of $\mathcal{L}$:
- $\mathcal{L} = \frac{ \partial  }{ \partial x } + \frac{ \partial  }{ \partial y }$
- $\mathcal{L} = \frac{ \partial ^2 }{ \partial x \partial y }$

The PDE $\mathcal{L}(u) = g$ is considered *linear* if $\mathcal{L}$ is linear in $u$
- $\mathcal{L}(u_{1}+u_{2}) = \mathcal{L}(u_{1}) + \mathcal{L}(u_{2})$
- $\mathcal{L}(cu_{1}) = c\mathcal{L}(u_{1})$
Otherwise, the PDE is considered non-linear