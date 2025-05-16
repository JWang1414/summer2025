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
- The derivation for this formula relies on assuming $\phi$ has a continuous second derivative and $\psi$ have continuous first derivative
- I'm not sure what $s$ is, but in the textbook it's used as a dummy variable used to replace $x$

EVERYTHING BEYOND THIS POINT IS UNEDITED


### Domain of Dependence
Fix $(x_{1},t_{1})$, then, by D'Alembert, $u(x_{1},t_{1})$ depends on initial displacements at $x_{1}-ct_{1}$ and $x_{1}+ct_{1}$ and all the initial velocities between them. So, we are interested in the interval $[x_{1}-ct_{1}, x_{1}+ct_{1}]$

- I have no clue what's going on. Everything beyond this point is probably nonsense

$$
(0<t_{2}<t_{1})\to \left[ x_{1}-c(t_{1}-t_{2}), x_{1}+c(t_{1}-t_{2}) \right]
$$

### Domain of influence
Fix $(x_{0}, 0)$. At a later time $t_{1}>0$, which points are affected by initial data?
$$
\to \left[ x_{0}-ct_{1}, x_{0}+ct_{1} \right]
$$
If $\phi, \psi$ vanish for $|x|>R$, then $u=0$ for $|x|>R+ct$

- He drew some triangular diagrams, I don't know what they mean. I hope they're in the textbook

### Energy (wave equation)
Suppose $u$ is a solution to $u_{tt} = \frac{T}{\rho} u_{x x}$. $C=\sqrt{ T / \rho }$

- This system is typically used to describe a vibrating string
- $T$ is tension, $\rho$ is the mass

Recall that the kinetic energy is
- $\frac{1}{2}mv^2$
- $\frac{1}{2}\rho \int_{-\infty}^{\infty} u_{t}^2 \, dx$
- We will assume that this integral converges

$\phi$ and $\psi$ are smooth with compact support, that is, they are zero outside of some interval.
- $u$ and $u_{t}$ vanish for $|x|>R+ct$

$$
\frac{d}{dt}KE = \rho \int_{-\infty}^{\infty} u_{t}u_{tt} \, dx = \int_{-\infty}^{\infty} u_{t}Tu_{x x} \, dx = T\left[ u_{t}u_{x}|^\infty_{-\infty} - \int_{-\infty}^{\infty} u_{ut}u_{x} \, dx  \right]
$$
Where we have used integration by parts for this last step. Furthermore, the boundary terms inside vanish at infinity, so
$$
=-T\int_{-\infty}^{\infty} u_{tx}u_{x} \, dx  = -T\int_{-\infty}^{\infty} \left( \frac{1}{2}u^{2}_{x} \right) _{t} \, dx
$$
Rearranging this result, we obtain the potential energy
$$
PE = -\frac{d}{dt}\int_{-\infty}^{\infty} \frac{1}{2}Tu^{2}_{x} \, dx
$$
If $E = KE+PE$, then
$$
\frac{d}{dt}E = \frac{d}{dt}(KE+PE) = 0
$$

Because of conservation of energy, $E=\frac{1}{2}\int_{-\infty}^{\infty} (\rho u^{2}_{t} + Tu^{2}_{x}) \, dx$ is constant in time.

Lets take the wave equation with initial values $u(x, 0)=\phi(x)$ and $u_{t}(x,0) = \psi(x)$. Suppose that we have two unique solutions to this IVP. Denote them as $u_{1}$ and $u_{2}$.

We want to prove that this problem has one unique solution. We will define a new solution, by superposition
$$
u=u_{1}-u_{2}
$$
It has initial values $u(x,0)=0$ and $u_{t}(x,0)=0$, because it is the superposition of the the previous two. We need $u=0$ to prove there is a unique solution.
$$
E(0)=0\Rightarrow E(t)=E(0)=0=\frac{1}{2}\int_{-\infty}^{\infty} (u^{2}_{t}+c^2u^{2}_{x}) \, dx
$$
And since the energy on the right side much be greater or equal to zero, the portion inside the integral must be equal to zero
$$
u^{2}_{t}+c^2u^{2}_{x}=0\Rightarrow u^{2}_{t}=u^{2}_{x}=0
$$
Now that we know this we can determine the total function $u$ is constant, and equal to zero because $u(x,0)=0$.
### Diffusion on the whole real line
- The spreading of particles or heat through space
$$
\begin{align}
 & u_{t} = ku_{x x} \\
 & u(x,0)=\phi(x)
\end{align}
$$
Where the interval is defined as $-\infty<x<\infty$ and $t\geq 0$

- WHAT