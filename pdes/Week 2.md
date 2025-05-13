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
We can check the shape of this function with the determinant
$$
\begin{align}
B^2-4AC<0,  &  & \text{equation is an ellipse} \\
B^2-4AC=0,  &  & \text{equation is a parabola} \\
B^2-4AC>0,  &  & \text{equation is a hyperbola}
\end{align}
$$
This has an analog in PDEs. Define $a,b,c,d,e,f$ all as functions of $(x, y)$
- The classifications above still hold, just with the functions instead of the variables. The names are all the same
- We call them elliptic, parabolic, and hyperbolic PDEs
### Intro to the Wave Equation
$$
u_{tt} - c^2 u_{x x} = 0
$$
Where $t$ is time and the spatial variable $x$ is valid on the interval $-\infty<x<\infty$

Allow us to rewrite the equation as:
$$
(\partial_{tt} - c^2\partial_{x x})u= (\partial_{t}-c \partial_{x})(\partial_{t} + c \partial_{x})u=0
$$
- That's a really strange and interesting thing you can do with derivatives

Theorem (not really): the general solution to the wave equation above is
$$
u(x, t) = f(x+ct) + g(x-ct)
$$
- Visualise this as the sum of a left moving and right moving transport. Both of these transport functions are moving at the same speed
- This tells us that the wave equation is built from interference between two waves