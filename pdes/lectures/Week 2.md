### Review
We analysed the PDE
$$
a(x,y)u_{x}+b(x,y)u_{y}=0
$$
Our strategy was to reduce the solutions to the ODE
$$
\frac{dy}{dx}=\frac{b(x, y)}{a(x, y)}
$$
Example in the temporal perspective
- Until now, we have exclusively been considering the spatial perspective
$$
\begin{align}
u_{t} + cu_{x} = 0,  &  & u(x, 0) = g(x)
\end{align}
$$
This can be rewritten as
$$
\begin{bmatrix}
c \\
1
\end{bmatrix} \cdot \begin{bmatrix}
u_{x} \\
u_{t}
\end{bmatrix} = 0
$$
The line parallel to this is
$$
u(x, t) = f(x-ct)
$$
Based on the boundary condition, we obtain
$$
u(x,0) = f(x)=g(x)\Rightarrow u(x, t)=g(x-ct)
$$
Which is often called the "transport equation", because it simply shifts the function $g$ to the left or right

**Try a more complex example.**
$$
a(x, y)u_{x}+b(x,y)u_{y}+u=0
$$
Define $\alpha=ax+by$ and $\eta=bx-ay$. Using the chain rule, we can obtain
$$
\begin{align}
u_{x} & =\frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial x } +\frac{ \partial u }{ \partial \eta } \frac{ \partial \eta }{ \partial x } =au_{\alpha}+bu_{\eta} \\
u_{y} & =bu_{\alpha}-au_{\eta}
\end{align}
$$
Substituting back into the original equation, we have:
$$
(a^2+b^2)u_{\alpha}=-u\to \frac{u_{\alpha}}{u} = -\frac{1}{a^2+b^2}
$$
This is an ODE we can solve
$$
\ln u = \frac{-\alpha}{a^2+b^2} + g(\eta)
$$
Solving for $u$ to obtain a general equation
$$
u=f(\eta)e^{ -\alpha/(a^2+b^2) }
$$
Putting it back in terms of $x$ and $y$
$$
u(x,y) = f(bx-ay)e^{ -\frac{ax+by}{a^2+b^2} }
$$

**Another example**
$$
u_{x}+u_{y}=5
$$
Use
$$
\begin{align}
\alpha=x+y &  & \eta=x-y
\end{align}
$$
Apply the chain rule again
$$
(u_{\alpha}+u_{\eta})+(u_{\alpha}-u_{\eta})=5\Rightarrow u_{\alpha}=\frac{5}{2}
$$
We can solve this resulting ODE
$$
u=\frac{5}{2}\alpha + f(\eta) \Rightarrow u(x, y) = \frac{5}{2}(x+y) + f(x-y)
$$
### Second-order quadratic equations
$$
Ax^2+Bxy+Cy^2 + Dx + Ey + F=0
$$
In accordance with conic classifications of functions, we can use the determinant to claim that the shape of this function is:
$$
\begin{align}
B^2-4AC<0,  &  & \text{equation is an ellipse} \\
B^2-4AC=0,  &  & \text{equation is a parabola} \\
B^2-4AC>0,  &  & \text{equation is a hyperbola}
\end{align}
$$
For PDEs, we instead use the equation
$$
au_{xx}+bu_{xy} + cu_{yy} + du_{x} + eu_{y} + fu=0
$$
Where similarly at least one of $a$ to $c$ is non-zero. We use the same conic equations and classifications for PDEs
- That is, the classifications use the same equation, and share the same name
- However, this does not mean that the PDEs behave similarly to their conic counterparts

Theorem:
Consider any general PDE of the form given above, where $a,b,c$ are not all 0. Then there exists a linear change of variables $\xi(x, y), \eta(x,y)$ such that the new coordinates $(\xi, \eta)$, the PDE is transformed as follows:
$$
\begin{align}
b^2-4ac<0 & \implies u_{\xi \xi} + u_{\eta \eta} + F(u_{\xi}, u_{\eta}, u)=0 \\
b^2-4ac=0 & \implies u_{\eta \eta} + F(u_{\xi}, u_{\eta}, u)=0 \\
b^2-4ac>0 & \implies u_{\xi \eta} + F(u_{\xi}, u_{\eta}, u)=0
\end{align}
$$
Where $F$ is some linear function of 3 variables
### Intro to the Wave Equation

$$
u_{tt} - c^2 u_{x x} = 0
$$
Where $t$ is time and the spatial variable $x$ is valid on the interval $-\infty<x<\infty$

The operator for this equation can be factored, transforming the equation into
$$
\left( \frac{ \partial  }{ \partial t } -c \frac{ \partial  }{ \partial x }  \right)\left( \frac{ \partial  }{ \partial t } +c \frac{ \partial  }{ \partial x }  \right)u=0
$$
Which has the general solution:
$$
u(x, t) = f(x+ct) + g(x-ct)
$$
- Visualise this as the sum of a left moving and right moving transport. Both of these transport functions are moving at the same speed
- This tells us that the wave equation is built from interference between two waves
### Initial Value Problems
Now, we are interested in solving the wave equation with the initial conditions $u(x,0)=\phi(x)$ and $u_{t}(x,0)=\psi(x)$
- $u(x, 0) = \phi(x)$ which can be imagined as the initial displacement
- $u_{t}(x, 0) = \psi(x)$ which can be imagined as the initial velocity
The solution for this initial value problem is specified by d'Alembert's formula
$$
u(x,t) = \frac{1}{2} \left[ \phi(x+ct) + \phi(x-ct) \right]  + \frac{1}{2C} \int_{x-ct}^{x+ct} \psi(s) \, ds 
$$
- If we assume that $\phi$ has a continuous second derivative, and $\psi$ has a continuous first derivative, then we can conclude $u$ has continuous second partial derivatives in $x$ and $t$.
	- This makes it a full solution for the wave equation and specified initial conditions
- I'm not sure what $s$ is, but in the textbook it's used as a dummy variable used to replace $x$

Example: Plucked string
- For a vibrating string, the speed is $c=\sqrt{ T / \rho }$, where $T$ is the tension, and $\rho$ is the mass density
Consider an infinitely long string with initial position
$$
\phi(x) = \begin{cases}
b-\frac{b|x|}{a} & \text{for } |x|<a \\
0 & \text{for } |x|>a
\end{cases}
$$
- Initial velocity $\psi(x)\equiv 0$ for all $x$

Using d'Alembert's formula, the general solution is
$$
\frac{1}{2} \left[ \phi(x+ct) + \phi(x-ct) \right]
$$
- This is effectively the sum of two triangle functions, one moving to the right, and one to the left

When specifying the functions with values, one must take care to evaluate within the given conditions. For example, for $x<-\frac{3}{2}a$ and $x> \frac{3}{2}a$, for $t=a /2c$, then both $\phi$ functions will evaluate to zero.
$$
u(x, t) = \frac{1}{2}\left[ \phi\left( x+\frac{1}{2}a \right) + \phi\left( x-\frac{1}{2}a \right) \right] \to 0
$$
Otherwise, if $-3a /2<x<-a /2$ or $a /2<x<3a /2$, then only one function will evaluate, and the other will simplify to zero.

The only case where both evaluate is when $|x|<a /2$
$$
u(x,t) = \frac{1}{2}\left[ \phi\left( x+\frac{1}{2}a \right) + \phi\left( x-\frac{1}{2}a \right) \right] = \frac{1}{2}\left[ b-\frac{b\left( x+\frac{1}{2}a \right)}{a}+b-\frac{b\left( \frac{1}{2}a-x \right)}{a} \right] =\frac{1}{2}b
$$
### Causality
Going back to the example with the vibrating string, the effect of an initial velocity $\psi$ is a wave spreading out at speed $\leq c$. The maximum speed at which the string can vibrate is specified by $c$. This equivalently means that no part of the string can go faster than $c$. This concept is known as the *principle of causality*, and is expressed with either the domain of *influence* or *dependence*.

**Domain of Influence**
An initial condition at the point $(x_{0},0)$ can affect the solution for $t>0$ only in the marked shaded sector. This shaded sector is what is called the domain of influence of the point $(x_{0},0)$
- The domain of influence appears to be the possible changes that can happen based on the different initial conditions defined at some point

**Domain of Dependence**
Alternatively, given a fixed point $(x,t)$ with $t>0$, how is another value $u(x,t)$ determined from the initial data $\phi$, $\psi$? It depends on the values of $\phi$ at the two points $x\pm ct$ and the values of $\psi$ within the interval $[x-ct, x+ct]$. The interval $(x-ct, x+ct)$ is the interval of dependence, of the point $(x,t)$ on $t=0$. The shaded region is the domain of dependence of the point $(x,t)$
- I think this is supposed to the be the region of points that can be affected by the initial values at the given point?
### Energy
Define an infinite string with constants $\rho$, $T$, and $c=\sqrt{ T /\rho }$. Then, the wave equation turns into
$$
u_{tt} = c^2u_{xx} = \frac{T}{\rho}u_{xx} \Rightarrow \rho u_{tt} = Tu_{xx}
$$
Which remains defined over $-\infty<x<\infty$. We will define the kinetic energy as
$$
KE = \frac{1}{2}\rho \int u^{2}_{t} \, dx
$$
Furthermore, we will assume that $\phi(x)$ and $\psi(x)$ converge on the interval from $-\infty$ to $\infty$. This is not unreasonable to claim, since from causality, they should vanish outside of some interval $\{ |x|\leq R \}$.

Now, differentiating the kinetic energy by time, we get
$$
\frac{d}{dt}KE = \rho \int_{-\infty}^{\infty} u_{t}u_{tt} \, dx = T\int_{-\infty}^{\infty} u_{t}u_{xx} \, dx = Tu_{t}u_{xx}|^\infty_{-\infty}-T\int_{-\infty}^{\infty} u_{tx}u_{x} \, dx
$$
Where I have used the version of the wave equation previously defined in this section, and then used integration by parts. We have previously established that $Tu_{t}u_{x}$ will vanish at $x=\pm \infty$, and so we are left with
$$
\frac{d}{dt}KE= -T\int_{-\infty}^{\infty} u_{tx}u_{x} \, dx = -\frac{d}{dt}\int_{-\infty}^{\infty} \frac{1}{2}Tu^{2}_{x} \, dx
$$
If we define the potential energy as $\frac{1}{2}T\int u^{2}_{x}\, dx$ and the total energy as $E=KE+PE$ then we have established:
$$
\frac{d}{dt}KE=-\frac{d}{dt}PE\implies \frac{d}{dt}E=0
$$
And furthermore,
$$
E=\frac{1}{2}\int_{-\infty}^{\infty} (\rho u^{2}_{t}+Tu^{2}_{x}) \, dx
$$
is constant independent of time $t$. Unsurprisingly, we have established that, within the realm of the wave equation, energy is conserved.
- Sometimes the definition $E$ will be modified by some constant factor, but energy is still conserved
- $E$ must be positive

Example: Energy of a plucked string
$$
E=\frac{1}{2}T\int_{-\infty}^{\infty} \phi^{2}_{x} \, dx =\frac{1}{2}T\left( \frac{b}{a} \right)^2 (2a)= \frac{Tb^2}{a}
$$
### Relation to Physics
In Maxwell's equations, the electric and magnetic fields satisfy the 3-D wave equation, where $c$ is instead the speed of light.

The principle of causality is the cornerstone of relativity. A signal at the position $x_{0}$ at the instant $t_{0}$ cannot move faster than the speed of light. And so the domain of influence consists of all the points that can be reach by the signal of speed $c$.
- Curiously, solutions of the 3-D wave equation always travel at speed $c$ and never slower.
### Diffusion on the whole line
The diffusion equation is defined as
$$
u_{t}=ku_{xx}
$$
It is defined for $-\infty<x<\infty$ and $0<t<\infty$. We define the initial conditions $u(x,0)=\phi(x)$

Properties of the diffusion equation
1. The translate of any solution $u(x-y, t)$ of any solution $u(x, t)$ is another solution, for any fixed $y$
2. Any derivative $(u_{x}, u_{t}, u_{xx},\dots)$ of a solution is another solution
3. Any linear combination of solutions is another solution
4. An integral of solutions is another solution
	1. If $S(x, t)$ is a solution, then $S(x-y, t)$ is another solution, and so is $v(x, t) = \int_{-\infty}^{\infty} S(x-y, t)g(y) \, dy$ for any given function $g(y)$
	2. This is valid so long as the above integral converges
5. If $u(x, t)$ is a solution, then so is the dilated function $u(\sqrt{ a }x, at)$ for any $a>0$
	1. This is roughly because, in essence, this dilation is linear
	2. Taking a derivative of the dilated function, you can show that the resulting function is just the original derivative multiplied by a constant

Define $Q(x,t)$ a particular solution of the diffusion equation for the initial conditions:
- $Q(x, 0)=1$ for $x>0$
- $Q(x, 0)=0$ for $x<0$
These initial conditions have been arbitrarily chosen because they simplify the problem

Skipping over the details, we have:
$$
Q(x, t)=\frac{1}{2}+\frac{1}{\sqrt{ \pi }}\int_{0}^{x /\sqrt{ 4kt }} e^{ -p^{2} } \, dp
$$
For $t>0$. Where $p=x /\sqrt{ 4kt }$

Now, define $S=\partial Q /\partial x$. By property 2, this is also a solution. Furthermore, define the function
$$
u(x, t)=\int_{-\infty}^{\infty} S(x-y)\phi(y) \, dy
$$
For $t>0$. For any function $\phi$, this is another solution. Furthermore, it is possible to prove that $u$ is a unique solution to the diffusion equation.

These functions, explicitly are:
$$
\begin{align}
S=\frac{ \partial Q }{ \partial x }  & = \frac{1}{2\sqrt{ \pi kt }}e^{ -x^{2}/4kt } \\
u(x,t) & =\frac{1}{\sqrt{ 4\pi kt }}\int_{-\infty}^{\infty} e^{ -(x-y)^{2}/4kt }\phi(y) \, dy 
\end{align}
$$
$S(x, t)$ is called the source function, Green's function, fundamental solution, propagator of the diffusion equation, or diffusion kernel.
- It gives the solution for any initial $\phi$
- Valid for $t>0$. $t=0$ makes no sense
### Properties of the Source Function
- Define for all real $x$ and $t>0$
- Positive and even in $x$
- For small $t$ it becomes a spike, for large $t$ it becomes a wide Gaussian

Normalised integral
$$
\int_{-\infty}^{\infty} S(x,t) \, dx = \frac{1}{\sqrt{ \pi }} \int_{-\infty}^{\infty} e^{ -q^{2} } \, dq =1
$$
Where $q=x /\sqrt{ 4kt }$
- Without the central spike, the area of the remaining function tends to zero

The value of the solution $u(x,t)$ resembles a weighted average of the initial values around $x$
$$
u(x,t) = \int_{-\infty}^{\infty} S(x-y, t)\phi(y) \, dy \approx \sum _{t} S(x-y_{i}, t)\phi(y_{i}) \Delta y_{i}
$$
- This is the average of the solutions $S(x-y_{i}, t)$ with weights $\phi(y_{i})$

It will be useful to define the error function, which integrals may often be defined relative to
$$
\mathcal{E}rf(x) = \frac{2}{\sqrt{ \pi }} \int_{0}^{x} e^{ -p^2 } \, dp
$$
For some $p$. $\mathcal{E}rf(0)=0$ and $\lim_{ x \to \infty }\mathcal{E}rf(x)=1$

