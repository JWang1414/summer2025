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
### Waves with a Source
Start with an in-homogeneous equation on the whole line
$$
u_{tt} -c^{2} u_{xx} = f(x,t)
$$
We defined this function over $-\infty<x<\infty$, $t>0$. With initial conditions
$$
\begin{align}
u(x,0)=\phi(x) &  & u_{t}(x,0)=\psi(x)
\end{align}
$$
- We are starting with in-homogeneous solutions because then we can derive the homogeneous and half-line solutions from it
- We will solve this with something called Duhammel's principle

We will claim that the solution to this is a modified version of d'Alembert's formula:
$$
u(x, t) = \frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right]  + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi(y) \, dy + \frac{1}{2c}\iint_{D} f(y, s) \, dyds
$$
Where $D$ is the "characteristic triangle" or "domain of dependence" associated with $(x, t)$

However, this domain is very defined, and so we can try to write it as an iterated integral
$$
\int_{0}^{t} \int_{x-c(t-s)}^{x+c(t-s)} f(y, s) \, dy  \, ds
$$
- Proved this principle in class. Try searching for it in the textbook for review
---
Example:
$$
\begin{cases}
u_{tt} = c^{2}u_{xx}=\cos x &  & -\infty<x<\infty, t>0 \\
u(x,0)=\sin x,  &  & u_{t}(x,0)=1+x
\end{cases}
$$
Substitute directly into the solution formula:
$$
\frac{1}{2}\left[ \sin(x+ct) + \sin(x-ct) \right]  + \frac{1}{2c} \int_{x-ct}^{x+ct} (1+y) \, dy + \frac{1}{2c} \int_{0}^{t} \int_{x-c(t-s)}^{x+c(t-s)} \cos y \, dy  \, ds
$$
Explicitly write out all the values, and solve:
$$
\frac{1}{2}\left[ 2 \cos ct \sin x \right]  + \frac{1}{2c} \left[ x+ct + \frac{(x+ct)^{2}}{2} -(x-ct)-\frac{(x-ct)^{2}}{2}\right] + \frac{1}{2c} \int_{0}^{t} \left[ \sin(x+c(t-s))-\sin(x-c(t-s)) \right]  \, ds
$$
After evaluating everything, simplify the formula:
$$
\cos ct\sin x + \frac{1}{2}\left[ 2ctx + 2ct \right] +\frac{1}{2c^{2}}\left[ \cos(x+c(t-s))+\cos(x-c(t-s)) \right] ^t_{0}
$$
This can be simplified all the way down to:
$$
\sin x\cos ct+t(x+t)+\frac{1}{c^{2}}\cos x(1-\cos ct)
$$
---
Example:
$$
\begin{cases}
u_{tt}-4u_{xx}=t\cos x,  &  & -\infty<x<\infty, t>0 \\
u(x,0)=e^{ -x },  &  & u_{t}(x,0) = \sin x
\end{cases}
$$
$$
u(x, t)=\frac{1}{2}\left[ e^{ -(x+ct)} + e^{ -(x-ct) } \right] + \frac{1}{2c}\int_{x-ct}^{x+ct} \sin y \, dy + \frac{1}{2c} \int_{0}^{t} \int_{x+c(t-s)}^{x+c(t-s)} s \cos y \, dy  \, ds
$$
$$
\frac{1}{2}e^{ -x }\left[ e^{ ct }+e^{ -ct } \right] - \frac{1}{4} \cos y |^{x+ct}_{x-ct} + \frac{1}{4} \int_{0}^{t} s \sin y |^{x+c(t-s)}_{x-c(t-s)} \, ds
$$
$$
e^{ -x }\cosh 2t-\frac{1}{4} [\cos(x+ct)-\cos(x-ct)] + \frac{1}{4} \int_{0}^{t} s \sin(x+c(t-s)) - s \sin(x-c(t-s)) \, dx
$$
$$
e^{ -x } \cosh 2t- \frac{1}{4} (-2\sin 2t \sin x) - \frac{1}{2} \int_{0}^{t} s \cos x \sin(2s-2t) \, ds
$$
$$
e^{ -x } \cosh 2t+\frac{1}{2} \sin x\sin 2t - \frac{1}{2} \left[ \cos (x) s \left( -\frac{1}{2}\cos(2s-2t) \right)\bigg|^t_{0} - \cos x \int_{0}^{t} -\frac{1}{2} \cos(2s-2t) \, ds  \right]
$$
$$
e^{ -x }\cosh 2t + \frac{1}{2} \sin x\sin 2t - \frac{1}{2} \left[ \cos (x)t\left( -\frac{1}{2} \right) + \frac{1}{2} \cos x\int_{0}^{t} \cos(2s-2t) \, ds  \right]
$$
$$
e^{ -x }\cosh 2t + \frac{1}{2}\sin x \sin 2t + \frac{t}{4}\cos x - \frac{1}{8} \cos x\sin 2t
$$
### Diffusion with a Source
$$
\begin{cases}
u_{t}-ku_{xx} = f(x, t),  &  & -\infty<x<\infty, t>0 \\
u(x,0)=\phi(x)
\end{cases}
$$
The approach will be the same as what we used before. We will define a new, identical problem with $\phi(x)=0$, then by superposition, add this solution to the homogeneous solution we already know.
- Superposition is required because it tells us the addition of two solutions is also a solution

Going through this process, the final formula is:
$$
u(x, t) = \int_{-\infty}^{\infty} S(x-y, t)\phi(y) \, dy + \int_{0}^{t} \int_{-\infty}^{\infty} S(x-y, t-s)f(y,s) \, dy  \, ds
$$
---
Example:
$$
\begin{cases}
u_{t}-u_{xx}=1,  &  & -\infty<x<\infty & , t>0 \\
u(x,0) = e^{ -x }
\end{cases}
$$
- Notice that we have made $k=1$

$$
u(x, t) = \frac{1}{\sqrt{ 4kt }} \int_{-\infty}^{\infty} \exp \left( -\frac{(x-y)^{2}}{4kt} \right) e^{ -y } \, dy + \int_{0}^{t} \int_{-\infty}^{\infty} \frac{1}{\sqrt{ 4\pi(t-s) }} \exp \left[ -\frac{(x-y)^{2}}{4(t-s)} \right]  \, dy  \, ds
$$
The answer to this equation is simply
$$
e^{ t-x }+t
$$