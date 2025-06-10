### Question 1
I will apply the maximum and minimum principles to determine an upper and lower-bound on the values of $u(x, t)$.

We know that $u(x, t)$ is a solution to the diffusion equation, and so, the max/min principles state that the max/min values will occur at $t=0$, $x=0$, and $x=1$

In the boundary $0<x<1$, at $t=0$, the initial values are $u(x,0)=1-x^{2}$, which has range $[0,1]$.

Furthermore, we know that $u(0,t)=u(1,t)=0$.

Establishing these bounds, we have $0<u(x, t)<1$ for all $t>0$ and $0<x<1$
### Question 2
$$
\frac{d}{dt}E(t) = \frac{d}{dt} \int_{0}^{1} u^{2}(x, t) \, dx = \int_{0}^{1} \frac{ \partial  }{ \partial t } u^{2}(x, t) \, dx
$$
Suppressing the dependence on $x$ and $t$ in $u(x, t)$:
$$
=\int_{0}^{1} 2uu_{t} \, dx = \int_{0}^{1} 2u(ku_{xx}) \, dx = 2k\int_{0}^{1} uu_{xx} \, dx
$$
Performing integration by parts:
$$
=2k\left[ uu_{x}|^1_{0} - \int_{0}^{1} u^{2}_{x} \, dx  \right]
$$
Evaluate the first term in the brackets:
$$
u(x, t)u_{x}(x, t)\big|^{x=1}_{x=0} = u(1, t)u_{x}(1, t) - u(0, t)u_{x}(0, t) = -u^{2}(1, t) = -u^{2}_{x}(1, t)
$$
Therefore:
$$
=-2k\left[ u^{2}(1, t) + \int_{0}^{1} u^{2}_{x} \, dx  \right]
$$
- Idk how to continue from here, or what this means
### Question 3
Define the new equation $v(x, t) = u(x, t)-1$.

$$
\begin{cases}
v_{t}=ku_{xx},  &  & 0<x<\infty, \, t>0 \\
v(x,0) = e^{ -x }-1,  &  & 0<x<\infty \\
v(0,t)=0,  &  & t>0
\end{cases}
$$

This new equation is also a solution to the diffusion equation. Furthermore, the new initial conditions are:
$$
\begin{align}
v(x,0) = u(x,0)-1 = e^{ -x }-1 &  & v(0,t)=u(0,t)-1 = 1-1=0
\end{align}
$$
With these new initial values, the problem has a known solution:
$$
v(x, t) = \int_{0}^{\infty} \left[ S(x-y, t) - S(x+y, t) \right] \phi(y) \, dy
$$
Where $S(x, t)$ is the source function, and $\phi(x)$ is the initial condition for $v(x, 0)$.
$$
\begin{align}
v(x, t) & = \int_{0}^{\infty} \left[ S(x-y, t)-S(x+y, t) \right] (e^{ -y }-1) \, dy  \\
 & =\int_{0}^{\infty} e^{ -y }S(x-y, t) \, dy -\int_{0}^{\infty} e^{ -y }S(x+y, t) \, dy - \int_{0}^{\infty} S(x-y, t) \, dy + \int_{0}^{\infty} S(x+y, t) \, dy 
\end{align}
$$
Solving one of the integrals as an example:
$$
\begin{align}
 & = \int_{0}^{\infty} e^{ -y }S(x-y, t) \, dy   \\
 & = \frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \exp \left[ -y-\frac{(x-y)^{2}}{4kt} \right]  \, dy  \\
 & = \frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \exp \left[ -\frac{1}{4kt}(x^{2}+(4kt-2x)y+y^{2}) \right]  \, dy 
\end{align}
$$
Complete the square:
$$
\begin{align}
 & = y^{2}+(4kt-2x)y+x^{2} \\
 & = (x-2kt-y)^{2}+4(xkt-k^{2}t^{2}) \\
 & \Rightarrow -\frac{1}{4kt}(y^{2}+(4kt-2x)y+x^{2}) \\
 & = -\frac{(x-2kt-y)^{2}}{4kt} +kt-x
\end{align}
$$
Use the substitution $p=(x-2kt-y) /\sqrt{ 4kt }$, then $dy=-\sqrt{ 4kt }dp$
$$
\begin{align}
 & = \frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \exp \left[ -\frac{(x-2kt-y)^{2}}{4kt} +kt-x \right]  \, dy  \\
 & = \frac{(-\sqrt{ 4kt })}{\sqrt{ 4\pi kt }} e^{ kt-x } \int_{0}^{\infty} e^{ -p^{2} } \, dp  \\
 & = -\frac{1}{\sqrt{ \pi }}e^{ kt-x } \left( \frac{\sqrt{ \pi }}{2} \right) = -\frac{1}{2}e^{ kt-x }
\end{align}
$$
Evaluating the other integrals, we get:
$$
\begin{align}
\int_{0}^{\infty} e^{ -y }S(x+y, t) \, dy  & = \frac{1}{2}e^{ kt+x } \\
\int_{0}^{\infty} S(x-y, t) \, dy  & = -\frac{1}{2} \\
\int_{0}^{\infty} S(x+y, t) \, dy  & = \frac{1}{2}
\end{align}
$$
Which yields the final equation:
$$
\begin{align}
v(x, t)  & = -\frac{1}{2}e^{ kt-x } - \frac{1}{2}e^{ kt+x } + \frac{1}{2} + \frac{1}{2}  \\
 & = \frac{e^{ kt }}{2}(e^{ -x }-e^{ x }) + 1 \\
 & = -e^{ kt }\sinh x + 1
\end{align}
$$
Which can be used to solve for $u(x, t)$
$$
v(x, t) = u(x, t) - 1 \Rightarrow u(x, t) = 2-e^{ kt }\sinh x
$$
### Question 4
Neumann problem for the wave equation on the half-line. Solutions are as follows:
$$
u(x, t)= \begin{cases}
\frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right] +\frac{1}{2c}\int_{x-ct}^{x+ct} \psi(y) \, dy  &  & x>ct \\
\frac{1}{2}\left[ \phi(x+ct)+\phi(ct-x) \right] + \frac{1}{2c}\int_{0}^{ct-x} \psi(y) \, dy +\frac{1}{2c}\int_{0}^{x+ct} \psi(y) \, dy  &  & 0<x<ct
\end{cases}
$$
Where, in this case, we have: $u(x,0)=\phi(x)=x$, $u_{t}(x,0)=\psi(x)=0$.

All integrals of $\psi(x)$ evaluate to zero:
$$
\int_{a}^{b} \psi(x) \, dx = \int_{a}^{b} 0 \, dx = 0
$$
Where $a, b\in \mathbb{R}$ are any arbitrary constants.

The solution reduces to:
$$
u(x, t) = \begin{cases}
\frac{1}{2}\left[ \phi(x+ct) + \phi(x-ct) \right]  &  & x>ct \\
\frac{1}{2}\left[ \phi(x+ct) + \phi(ct-x) \right]  &  & 0<x<ct
\end{cases}
$$
$$
u(x, t) = \begin{cases}
\frac{1}{2}\left[ x+ct+x-ct \right] = x &  & x>ct \\
\frac{1}{2}\left[ x+ct+ct-x \right] = ct &  & 0<x<ct
\end{cases}
$$
More clearly written out:
$$
u(x, t)= \begin{cases}
x &  & x>ct \\
ct &  & 0<x<ct
\end{cases}
$$
