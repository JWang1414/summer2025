### Diffusion equation, in-homogeneous, half-line
- Now, we will try to solve the diffusion equation on the half-line, with Dirichlet boundary conditions
$$
\begin{cases}
u_{t} - ku_{xx} = f(x, t) &  & 0<x<\infty, t>0 \\
u(x,0)=\phi(x) \\
u(0,t)=0
\end{cases}
$$
Since we're doing Dirichlet boundary conditions, we choose to define the odd extensions $\phi _\text{odd}$ and $f_\text{odd}$ with respect to $x=0$
$$
\begin{cases}
u_{t}-ku_{xx} = f_\text{odd}(x, t) &  & -\infty<x<\infty, t>0 \\
u(x,0) = \phi _\text{odd}(x)
\end{cases}
$$
The solution to this will be the solution we already solved for (diffusion with a source).
- $v(0,t)=0$ is automatically satisfied, because it is an odd function
- The solution will be the restriction $u=v$ for $x>0$
$$
u(x, t) = \int_{-\infty}^{0} S(x-y)\phi _\text{odd}(y) \, dy + \int_{0}^{\infty} \dots \, dy + \int_{0}^{t} \left[ \int_{-\infty}^{0} S(x-y, t-s)f_\text{odd}(y, s) \, dy + \int_{0}^{\infty} \dots \, dy  \right]  \, ds
$$
Skipping over the intermediate steps, we get:
$$
\int_{0}^{\infty} \left[ S(x-y, t)-S(x+y, t) \right] \phi(y) \, dy + \int_{0}^{t} \int_{0}^{\infty} \left[ S(x-y, t-s)-S(x+y, t-s) \right] f(y, s) \, dy  \, ds
$$
---
Now, lets try the same problem with $u(0,t)=h(t)$.

Define a new function $v(x, t) = u(x, t)-h(t)$.

Then, we have $u_{t} = u_{t}-h'$, $v_{xx} = u_{xx}$.
$$
\begin{cases}
v_{t}-kv_{xx}=f(x, t) - h',  &  & 0<x<\infty, t>0 \\
v(x,0) = u(x,0)-h(0) = \phi(x)-h(0) \\
v(0,t) = u(0,t) - h(t) = h(t)-h(t)=0
\end{cases}
$$
Now, the final condition is once again 0, so we can just repeat the same derivation above.

---
Try it for the Neumann problem

$$
\begin{cases}
u_{t}-ku_{xx} = f(x, t) &  & 0<x<\infty, t>0 \\
u(x,0)=\phi(x) \\
u_{x}(0,t) = 0
\end{cases}
$$
Since this is the Neumann problem, we will use an even extension. This is a pretty familiar problem, so I won't write it down. The solution is the same as the Dirichlet problem, with a slight change of sign
$$
\int_{0}^{\infty} \left[ S(x-y, t)+S(x+y, t) \right] \phi(y) \, dy + \int_{0}^{t} \int_{0}^{\infty} \left[ S(x-y, t-s)+S(x+y, t-s) \right] f(y, s) \, dy  \, ds
$$
---
Now, what about the Neumann problem with $u_{x}(0,t) = h(t)$?

Define a new function $v(x, t) = u(x, t) - xh(t)$

Which gives us
$$
\begin{align}
v_{t}=u_{t}-xh'(t),  &  & v_{xx}=u_{xx}
\end{align}
$$
And the problem changes to
$$
\begin{cases}
v_{t}-kv_{xx}=f(x, t) = f(x, t)-xh'(t),  &  & 0<x<\infty, t>0 \\
v(x,0) = u(x,0) - xh(0) = \phi(x) - xh(0) \\
v_{x}(0,t) = u_{x}(0,t) - h(t) = h(t)-h(t) = 0
\end{cases}
$$
So now, we can go back again to the solution we have already found, and use it for this modified problem.
### Transport Equation
Recall that the solution to the homogeneous version:
$$
\begin{cases}
u_{t} + cu_{x} = 0 \\
u(x,0) = \phi(x)
\end{cases}
$$
Is the general equation $g(x-ct)$. So now, we will use Duhammel's equation to solve for
$$
\begin{cases}
u_{t}+cu_{x} = f(x, t) \\
u(x,0) = \phi(x)
\end{cases}
$$
Define the new equations:
$$
\begin{align}
u & =u^h+u^p \\
 & =\phi(x-ct) + \int_{s=0}^{s=t} w(x, t;s) \, ds 
\end{align}
$$
Where $w$ solves
$$
\begin{cases}
w_{t} + cw_{x} = 0, -\infty<x<\infty, t>s \\
w(x,s;s) = f(x, s)
\end{cases}
$$
$w$ will be the original solution to the transport equation, but shifted by some $s$:
$$
w = f(x-c(t-s))
$$
Which we can substitute back into the formula above:
$$
u = \phi(x-ct) + \int_{0}^{t} f(x-c(t-s)) \, ds
$$
### Finite Line
These are the lines were $0<x<L$. Doing away with the $\pm \infty$ bounds.
- This is a lot more physically relevant
- The key topic to study here will be separation of variables
