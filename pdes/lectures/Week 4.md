Recall the half-line Dirichlet problem
$$
\begin{align}
v_{t} & =kv_{xx},  &  & 0<x<\infty, t>0 \\
v(x,0) & =\phi(x) \\
v(0,t) & =0
\end{align}
$$
And the Neumann problem
$$
\begin{align}
w_{t} & =kw_{xx},  &  & 0<x<\infty, t>0 \\
w(x,0) & =\phi(x) \\
w_{x}(0,t) & =0
\end{align}
$$
- Both the Dirichlet and Neumann problems were solve in the previous week. Read there for the process and results

> Example: Dirichlet problem with $\phi(x)=0$

Define a new function $v(x,t)=u(x,t)-1$, which is still a solution to the original PDE (by superposition). However, notice that
$$
\begin{align}
v(x,0) & =u(x,0)-1=0-1=-1 \\
v(0,t) & =u(x, t)-1=1-1=0
\end{align}
$$
Explicitly solve this with the solution formula:
$$
v(x, t)=\frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \left[ e^{ -(x-y)^{2}/4kt }-e^{ -(x+y)^{2}/4kt } \right] (-1) \, dy
$$
Splitting this integral, and using the substitution $p=(x-y) /\sqrt{ 4kt }$, $q=(x+y) /\sqrt{ 4kt }$, we find the solution to be:
$$
-\frac{1}{\sqrt{ \pi }} \left[ \int_{-\infty}^{0} e^{ -p^{2} } \, dp +\int_{0}^{x /\sqrt{ 4kt }} e^{ -p^{2} } \, dp  \right] +\frac{1}{\sqrt{ \pi }} \left[ \int_{0}^{\infty} e^{ -q^{2} } \, dq -\int_{0}^{x /\sqrt{ 4kt }} e^{ -q^{2} } \, dq  \right]
$$
Or,
$$
-\mathcal{E}rf\left( \frac{x}{\sqrt{ 4kt }} \right)
$$
Now that we know the solution to $v$, we can solve for the solution to $u$
$$
v=u-1\Rightarrow u=v+1=1-\mathcal{E}rf\left( \frac{x}{\sqrt{ 4kt }} \right)
$$
### Wave Equation on the Half-line
$$
\begin{align}
v_{tt} & =c^{2}v_{xx},  &  & 0<x<\infty, t>0 \\
v(x,0) & =\phi(x),  &  & v_{t}(x,0)=\psi(x) \\
v(0,t) & =0
\end{align}
$$
Apply the same approach used on the diffusion equation. Use extensions of the initial functions to the whole line $\phi _\text{odd}(x)$, $\psi _\text{odd}(x)$. For these initial conditions, $u(x, t)$ will therefore be the solution to the IVP on the whole lin $(-\infty, \infty)$.

$u(x, t)$ will be an odd function of $x$. And so the boundary condition with $x=0$ is automatically satisfied.

Define the function $v(x, t)=u(x, t)$ as the restriction on $0<x<\infty$

From our previous knowledge, we know that
$$
u(x, t)=\frac{1}{2}\left[ \phi _\text{odd}(x+ct)+\phi _\text{odd}(x-ct) \right]  + \frac{1}{2c}\int_{x-ct}^{x+ct} \psi _\text{odd}(y) \, dy
$$

Now, look at the behaviour of difference intervals. For $x>ct$, only positive arguments occur, and so
$$
v(x, t)=\frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right]  + \frac{1}{2c}\int_{x-ct}^{x+ct} \psi (y) \, dy
$$
For $0<x<ct$. Try using the substitution $\omega=-y$
$$
\begin{align}
v(x, t) & =\frac{1}{2}\left[ \phi(x+ct)-\phi(ct-x) \right]  + \frac{1}{2c}\int_{x-ct}^{0} -\psi(-y) \, dy +\frac{1}{2c}\int_{0}^{x+ct} \psi(y) \, dy  \\
 & =\frac{1}{2}\left[ \phi(x+ct)-\phi(ct-x) \right]  + \frac{1}{2c}\int_{ct-x}^{x+ct} \psi(y) \, dy
\end{align}
$$
And the full solution is the combination of these two cases
$$
v(x, t) = \begin{cases}
\frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right]  + \frac{1}{2c}\int_{x-ct}^{x+ct} \psi (y) \, dy  &  & x>ct \\
\frac{1}{2}\left[ \phi(x+ct)-\phi(ct-x) \right]  + \frac{1}{2c}\int_{ct-x}^{x+ct} \psi(y) \, dy &  & 0<x<ct
\end{cases}
$$
### Neumann Problem for the Wave Equation
$$
\begin{align}
w_{tt} & =c^{2}w_{xx},  &  & 0<x<\infty, t>0 \\
w(x,0) & =\phi(x),  &  & w_{t}(x,0)=\psi(x) \\
w_{x}(0,t) & =0
\end{align}
$$
Define the same things with $\phi _\text{even}$ and $\psi _\text{even}$. For these initial conditions, call the solution $u$. Now, $w(x, t)=u(x, t)$ on the restriction $0<x<\infty$

The only interesting case is the one for $x<ct$
$$
\begin{align}
w & =\frac{1}{2}\left[ \phi(x+ct)+\phi(ct-x) \right] +\frac{1}{2c}\int_{x-ct}^{0} \psi(-y) \, dy +\frac{1}{2c}\int_{0}^{x+ct} \psi(y) \, dy  \\
 & = \frac{1}{2}\left[ \phi(x+ct)+\phi(ct-x) \right] + \frac{1}{2c}\int_{0}^{ct-x} \psi(y) \, dy +\frac{1}{2c}\int_{0}^{x+ct} \psi(y) \, dy 
\end{align}
$$
Where the same $\omega=-y$ substitution has been used to evaluate one of the integrals. The full solution can be similarly written out in cases:
$$
w(x, t)= \begin{cases}
\frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right] +\frac{1}{2c}\int_{x-ct}^{x+ct} \psi(y) \, dy  &  & x>ct \\
\frac{1}{2}\left[ \phi(x+ct)+\phi(ct-x) \right] + \frac{1}{2c}\int_{0}^{ct-x} \psi(y) \, dy +\frac{1}{2c}\int_{0}^{x+ct} \psi(y) \, dy  &  & 0<x<ct
\end{cases}
$$

> Example: Neumann problem with $\phi(x)=\sin x$ and $\psi(x)=e^{ x }$

For $x>ct$
$$
w=\frac{1}{2}\left[ \sin(x+ct)+\sin(x-ct) \right] +\frac{1}{2c}\left[ e^{ x+ct }-e^{ x-ct } \right]
$$
Which can be simplified into
$$
w=\cos(ct)\sin x + \frac{e^{ x }}{c}\sinh(ct)
$$

Now, for $x<ct$
$$
w=\frac{1}{2}\left[ \sin(x+ct)+\sin(x-ct) \right] +\frac{1}{2c}\left[ e^{ x+ct }-1 \right] +\frac{1}{2c}\left[ e^{ ct-x }-1 \right]
$$
Which once again can be simplified into
$$
w=\cos x \sin(ct)-\frac{1}{c}+\frac{1}{c}e^{ ct }\cosh x
$$
Fully piece-wise defined:
$$
w=(x, t)=\begin{cases}
\cos(ct)\sin x + \frac{e^{ x }}{c}\sinh(ct) &  & x>ct \\
\cos x \sin(ct)-\frac{1}{c}+\frac{1}{c}e^{ ct }\cosh x &  & x<ct
\end{cases}
$$
