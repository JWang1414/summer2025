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
### Linear and Homogeneous PDEs
The typical PDE is structured as
$$
\mathcal{L}(u) = g(\vec{x})
$$
Where $\mathcal{L(u)}$ is all terms containing $u$ and its derivatives. $\mathcal{L}$ is some operator composed of derivatives. $g(\vec{x})$ is a stand in for all terms involving only the independent variables

Examples of $\mathcal{L}$:
- $\mathcal{L} = \frac{ \partial  }{ \partial x } + \frac{ \partial  }{ \partial y }$
- $\mathcal{L} = \frac{ \partial ^2 }{ \partial x \partial y }$

The PDE $\mathcal{L}(u) = g$ is considered *linear* if $\mathcal{L}$ is linear in $u$
- $\mathcal{L}(u_{1}+u_{2}) = \mathcal{L}(u_{1}) + \mathcal{L}(u_{2})$
- $\mathcal{L}(cu_{1}) = c\mathcal{L}(u_{1})$
Otherwise, the PDE is considered non-linear

If, in a typical PDE, $g \equiv 0$ then the PDE is homogeneous. Otherwise, it is in-homogeneous

Examples:
- $(\cos x y^2)u_{x} - y^2 u_{y} = \tan(x^2+y^2)$
	- Linear, in-homogeneous
- $u_{tt} - u_{x x} + u^3 = 0$
	- Nonlinear (cubic), homogeneous

### Superposition principle
For homogeneous PDEs
- If $u$ and $v$ are both solutions to the homogeneous PDE $\mathcal{L}(u)=0$, then $u+v$ is also a solution
- Generally speaking, if $u_{1}, \dots, u_{n}$ are both solutions, then any linear combination $c_{1}u_{1}+\dots+c_{n}u_{n}$ is also a solution

For a in-homogeneous, linear PDE $\mathcal{L}(u) = g$
- If we have the solution $u_{1}$ to $\mathcal{L}(u) = g_{1}$ and $u_{2}$ to $\mathcal{L}(u)=g_{2}$ then $au_{1}+bu_{2}$ is a solution to $\mathcal{L}(u) = ag_{1}+bg_{2}$

Worked example
$$
u_{xy} = 0
$$
First, take the integral with respect to $x$
$$
u_{y} = f(y)
$$
Then, take the integral with respect to $y$
$$
u(x, y) = F(y) + g(x)
$$
Where $F'=f$
- This PDE is supplemented by an *auxiliary condition*. This idea will appear often in PDEs
- There are two natural classes of auxiliary conditions. They lead to *initial value problems* (IVPs) and *boundary value problems* (BVPs)
- Independent variables can sometimes be specified. Such as using $t=0$
- If, for example, all the independent variables are spatial, we often look for a solution in some region $\Omega$ of space where the solution is specified for the boundary $\partial \Omega$
	- This gives rise to a BVP
### First-order Linear Equations
Lets start with a constant coefficient equation $au_{x}+bu_{y}=0$ where $a,b\in \mathbb{R}$

Notice that, using a gradient and dot product, we have
$$
\begin{bmatrix}
a \\
b
\end{bmatrix} \cdot \nabla u = 0
$$
- On any line parallel to $(a, b)$, the solution is constant

Lines parallel to $(a,b)$ can be written as: $bx-ay =c$ for some constant $c$. The solution takes on a different form depending on the value of $c$. Therefore, $u(x, y)$ depends only on $bx-ay$, so the general solution is
$$
u(x, y) = f(bx-ay)
$$

Example: $3u_{x}+2u_{y} = 0$ with $u(x, 0) = x^3$

In this case, the general solution is: $u(x, y) = f(2x-3y)$

Implemented the auxiliary equation:
$$
u(x, 0) = f(2x) = x^3 \Rightarrow f(w) = \frac{1}{8}w^3
$$
Where $w=2x$. The full equation for $f$ is therefore
$$
u(x, y) = f(2x-3y) = \frac{1}{8}(2x-3y)^3
$$
### Change of variables/coordinates
Note about notation:
- $u(x, y)$ denotes a input-output machine which takes two real numbers, and outputs one real number
- We would like to describe $u$ in terms of different input variables, $\alpha$ and $\eta$, which are in terms of functions of $x$ and $y$

For example, $u(x, y) = (4x+y)^2 + (x-y)^2 \to \alpha^2 + \eta^2$ where $\alpha=4x+y$ and $\eta=x-y$. We should not write this down as $u(\alpha, \eta)$, but it is standard to do so

Lets return to the example with $au_{x} + bu_{y}=0$. We will define $\alpha=ax+by$ and $\eta=bx-ay$

Solve for $u_{x}$ and $u_{y}$ with the chain rule
$$
\begin{align}
u_{x}  & = \frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial x } + \frac{ \partial u }{ \partial \eta } \frac{ \partial \eta }{ \partial x } = au_{\alpha} + bu_{\eta} \\
u_{y}  & = bu_{\alpha}-au_{\eta}
\end{align}
$$
Substitute this back into the full equation
$$
au_{x} + bu_{y} = a(au_{\alpha}+bu_{\eta}) + b(bu_{\alpha} - au_{\eta}) = (a^2+b^2)u_{\alpha} = 0
$$
$a,b\in \mathbb{R}$ and $a,b\neq 0$. Which means that $a^2+b^2>0$. We can therefore conclude that $u_{\alpha}=0$. This simplifies out equation and gives us $u(\alpha, \eta) = f(\eta)$ or $u(x, y) = f(bx-ay)$, which is the same as before
### Variable Coefficient Equation
Define the linear, homogeneous equation $u_{x}+yu_{y}=0$. Which carried the properties
$$
\begin{bmatrix}
1 \\
y
\end{bmatrix}\cdot \nabla u=0
$$
The direction specified by this coefficient changes over the $xy$-plane. The solution will be constant along these curves.

At any point $(x, y(x))$ we require its tangent vector $\left( 1, \frac{dy}{dx} \right)$ to be parallel to $(1, y)$.
$$
\frac{dy}{dx} = y \Rightarrow \int \frac{1}{y} \, dy=\int dx \Rightarrow \ln y = x+C \Rightarrow y=Ce^{ x }
$$
Two points $(x_{1},y_{1})$  and $(x_{2},y_{2})$ lie on the same characteristic iff, they correspond to the same value of $C$
$$
y_{1}e^{ -x_{1} } = y_{2}e^{ -x_{2} }
$$
So the general solution can be written
$$
u(x, y) = f(ye^{ -x })
$$

Example: $u_{x} + 2xy^2u_{y}=0$

Solve for the characteristic curves
$$
\frac{dy}{dx} = 2xy^2 \Rightarrow \int y^{-2} \, dy = 2\int x \, dx \Rightarrow -\frac{1}{y} = x^2-C \Rightarrow y = \frac{1}{C-x^2}
$$
Solve for $C$ from the previous
$$
C = \frac{1}{y} + x^2
$$
And therefore the general solution is
$$
u = f(c) = f\left( x^2+\frac{1}{y} \right)
$$
- For any PDE $a(x, y)u_{x} + b(x, y)u_{y}=0$, the method of characteristics works nicely because it reduces the solution of the PDE to a simpler ODE $\frac{dy}{dx} = \frac{b(x, y)}{a(x, y)}$
