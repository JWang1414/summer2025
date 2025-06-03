### Question 1
---
a.
Re-write the PDE as a dot product
$$
3u_{x} + 8u_{y} = \begin{bmatrix}
3 \\
8
\end{bmatrix} \cdot \nabla u = 0
$$
Characteristic curves will be along $bx-ay=c$ for some constant $c$. We have:
$$
\begin{bmatrix}
a \\
b
\end{bmatrix} = \begin{bmatrix}
3 \\
8
\end{bmatrix} \implies bx-ay = 8x-3y = c
$$
The general solution is:
$$
u(x, y) = f(8x-3y)
$$
---
b.
Define two new variables, $\alpha$ and $\beta$. Both will be functions of $x$ and $y$.
$$
\begin{align}
\alpha & = ax+by = 3x+8y \\
\beta & = bx-ay = 8x-3y
\end{align}
$$
In-terms of these new variables, use the chain rule to determine the derivatives $u_{x}$ and $u_{y}$:
$$
\begin{align}
u_{x} & = \frac{ \partial u }{ \partial x } = \frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial x } + \frac{ \partial u }{ \partial \beta } \frac{ \partial \beta }{ \partial x } = 3 \frac{ \partial u }{ \partial \alpha } + 8 \frac{ \partial u }{ \partial \beta } = 3u_{\alpha} + 8u_{\beta} \\
u_{y} & = \frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial y } + \frac{ \partial u }{ \partial \beta } \frac{ \partial \beta }{ \partial y } = 8u_{\alpha} - 3u_{\beta}
\end{align}
$$
Substitute these derivatives back into the original equation
$$
3u_{x} + 8u_{y} = 3(3u_{\alpha}+8u_{\beta}) + 8(8u_{\alpha}-3u_{\beta}) = 9u_{\alpha}+24u_{\beta}+64u_{\alpha}-24u_{\beta} = 73u_{\alpha} = 0
$$
We conclude that $u_{\alpha}=0$ and the solution will be a function of only $\beta$:
$$
f(\beta) = f(8x-3y)
$$
---
c.
Implementing the auxiliary conditions, we have:
$$
u(0,y) = f(-3y) = \cos y
$$
Use the substitution $w=-3y$,
$$
f(w) = \cos\left( -\frac{w}{3} \right) = \cos\left( \frac{w}{3} \right)
$$
Where, in the last step, I have used the fact that $\cos$ is an even function. Now, the full equation for $f$ can be written out as:
$$
u(x, y) = f(8x-3y) = \cos\left( \frac{8x-3y}{3} \right) = \cos\left( \frac{8}{3}x-y \right)
$$
### Question 2
---
a.
This homogeneous equation can be re-written as:
$$
u_{t} + tu_{x} = \begin{bmatrix}
1 \\
t
\end{bmatrix} \cdot \nabla u = 0
$$
- DRAW THE CHARACTERISTIC CURVES HERE

---
b.
Therefore, at any point $(t, x)$ we require the tangent vector $(1, dx /dt)$ to be parallel to $(1, t)$
$$
\frac{dx}{dt} = t \implies \int dx = \int t \, dt \implies x = \frac{t^{2}}{2} + C
$$
The characteristic curves are defined for each $C$.
$$
x = \frac{1}{2}t^{2} + C \implies C = x-\frac{1}{2}t^{2}
$$
So the general solution is:
$$
u(x, t) = f\left( x-\frac{1}{2}t^{2} \right)
$$
---
c.
Substituting the initial conditions into the found solution,
$$
u(x,0) = f(x) = \sin x \implies f(w) = \sin w
$$
I have replaced $x$ with a dummy variable $w$ to avoid confusion. Substituting the original values back into the new formula $w = x-t^{2} /2$,
$$
u(x, t) = f\left( x-\frac{1}{2}t^{2} \right) = \sin\left( x-\frac{1}{2}t^{2} \right)
$$
Which is the solution with the auxiliary condition.
### Question 3
---
I will attempt to solve this question with change of variables. I will first define the two variables $\alpha$ and $\beta$:
$$
\begin{align}
\alpha = ax+by &  & \beta=bx-ay
\end{align}
$$
Applying the chain rule, the existing derivatives in terms of $\alpha$ and $\beta$ are:
$$
\begin{align}
u_{x}  & = \frac{ \partial u }{ \partial \alpha } \frac{ \partial \alpha }{ \partial x } + \frac{ \partial u }{ \partial \beta } \frac{ \partial \beta }{ \partial x } = au_{\alpha} + bu_{\beta} \\
u_{y} & =bu_{\alpha} - au_{\beta}
\end{align}
$$
Substituting these back into the original PDE, I obtain a solvable ODE.
$$
\begin{align}
au_{x} + bu_{y}  & = a(au_{\alpha} + bu_{\beta}) + b(bu_{\alpha} - au_{\beta})  \\
 & = a^{2}u_{\alpha} + abu_{\beta} + b^{2}u_{\alpha} - abu_{\beta}  \\
 & = a^{2}u_{\alpha} + b^{2}u_{\alpha} \\
(a^{2}+b^{2})u_{\alpha} & = 6
\end{align}
$$
Since $a\neq 0$ and $b\neq 0$ are constants, I can be certain that $a^{2}+b^{2} \neq 0$. Dividing both sides by this, and then solving the ODE I obtain:
$$
\frac{ \partial u }{ \partial \alpha } = \frac{6}{a^{2}+b^{2}} \implies u = \frac{6\alpha}{a^{2}+b^{2}} + f(\beta) = \frac{6(ax+by)}{a^{2}+b^{2}} + f(bx-ay)
$$
Which is the general solution. Stated again here:
$$
u(x, y) = \frac{6}{a^{2}+b^{2}} (ax+by) + f(bx-ay)
$$
### Question 4
---
a.
Extracting values of interest from the original equation, I define:
$$
\begin{align}
a=1 &  & b=2 &  & c=-8
\end{align}
$$
Calculating the determinant:
$$
b^{2}-4ac=2^{2}-4(1)(-8) = 36>0
$$
And so this equation is hyperbolic.

---
b.
Factor the original equation into:
$$
\left( \frac{ \partial  }{ \partial x } + 4\frac{ \partial  }{ \partial t }  \right)\left( \frac{ \partial  }{ \partial x } - 2\frac{ \partial  }{ \partial t }  \right)u=0
$$
The problem has now been split into two identical PDEs. I will solve both of these with the geometric method, using $c\in \mathbb{R}$ has some arbitrary constant
$$
u_{x} + cu_{t} = \begin{bmatrix}
1 \\
c
\end{bmatrix} \cdot \nabla u = 0
$$
$$
\begin{bmatrix}
a \\
b
\end{bmatrix} = \begin{bmatrix}
1 \\
c
\end{bmatrix} \implies bx-at = cx-t
$$
And so the general solution can be expressed as:
$$
u(x, t) = f(4x-t) + g(-2x-t)
$$
