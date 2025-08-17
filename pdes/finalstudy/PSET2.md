### Question 1
Recall that Maximum principle for the diffusion equation:
$$
u_{t} = ku_{xx}
$$
> If $u(x,t)$ satisfies the diffusion equation in a rectangle in space-time, then the maximum value of $u(x, t)$ is assumed either initially, $t=0$, or on the lateral sides $x=0, l$

Furthermore, the minimum principle is identical, stating that the minimum value is assumed either initially, $t=0$, or on the lateral sides $x=0,l$.

In this case, this means both the minimum and maximum points can be found when $l=0, 1$ and $t=0$. We have:
$$
u(0, t)=u(1, t)=0 \qquad u(x, 0) = 1-x^{2}
$$
Within the interval $x \in(0, 1)$ the value of $u(x, 0)$ ranges between $(0, 1)$. So I conclude that the maximum of the solution is 1, and the minimum of the solution is 0.

Since the maximum and minimum are different, I can be confident that the solution $u(x, t)$ is not constant. Implying that within the domain $\{ 0<x<1, 0<t<\infty \}$ there are no points equivalent to the minimum, $u(x, t)=0$. 

Hence, I conclude that, for all $t>0$ and $0<x<1$ the solution $u(x, t)>)$. As needed.
### Question 2
Compute the derivative of $E(t)$:
$$
E'(t) := \frac{d}{dt} \int_{0}^{1} u^{2}(x, t) \, dx = \int_{0}^{1} \frac{d}{dt} u^{2}(x, t) \, dx = \int_{0}^{1} 2u(x, t)u_{t}(x, t) \, dx
$$
Directly substituting in the diffusion equation:
$$
= 2 \int_{0}^{1} u(x, t) \left[ ku_{xx}(x, t) \right]  \, dx = 2k \int_{0}^{1} u(x, t)u_{xx}(x, t) \, dx
$$
Using integration by parts:
$$
= 2k \left[ u(x, t)u_{x}(x, t)\big|_{x=0}^{x=1} - \int_{0}^{1} u^{2}_{x}(x, t) \, dx  \right]
$$
Evaluating the first portion separately:
$$
u(x, t)u_{x}(x, t) \big|_{x=0}^{x=1} = u(1, t)u_{x}(1, t) - u(0, t)u_{x}(0, t) = -u^{2}(1, t) = -u^{2}_{x}(1, t)
$$
Substituting back into the original equation:
$$
E'(t) := -2k \left[ u^{2}_{x}(1, t) + \int_{0}^{1} u^{2}_{x}(x, t) \, dx  \right]
$$
All quantities within the square brackets are squared, so this is a purely positive quantity. So, the general behaviour of $E'(t)$ is determined solely by $k$.
$$
\begin{cases}
k<0 & E'(t)\text{ is positive} \\
k=0 & E'(t)\text{ is zero} \\
k>0 & E'(t)\text{ is negative}
\end{cases}
$$
From this, I conclude:
$$
\begin{cases}
k<0 & E(t)\text{ is increasing} \\
k=0 & E(t)\text{ is constant} \\
k>0 & E(t)\text{ is decreasing}
\end{cases}
$$
- It might be possible that $k$ cannot be 0 or negative, but I may be misremembering.
---
### Question 3
This is the diffusion equation on the half-line. The solutions follow the form:
$$
u(x, t) = \int_{0}^{\infty} \left[ S(x-y, t) - S(x+y, t) \right] \phi(y) \, dy
$$
Where $S$ is the source function:
$$
S(x) = \frac{1}{\sqrt{ 4\pi kt }} \exp \left\{  -\frac{x^{2}}{4kt}  \right\}
$$
And $\phi$ represents the initial conditions when $t=0$. In this case,
$$
\phi(x) = e^{ -x }
$$
Therefore,
$$
\begin{align}
u(x, t) & = \frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \left[ \exp \left\{  -\frac{(x-y)^{2}}{4kt}  \right\} - \exp \left\{  -\frac{(x+y)^{2}}{4kt}  \right\} \right] e^{ -y } \, dy \\
 & = \frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \exp \left\{  -\frac{(x-y)^{2}}{4kt}-y  \right\} \, dy - \frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \exp \left\{  -\frac{(x+y)^{2}}{4kt} -y \right\} \, dy 
\end{align}
$$
I will first evaluate the first integral. Complete the square of the function within the exponential:
$$
\begin{align}
-\frac{(x-y)^{2}}{4kt}-y & = -\frac{y^{2}}{4kt} - y + \frac{xy}{2kt} - \frac{x^{2}}{4kt} = -\frac{1}{4kt}y^{2} + y \left( \frac{x}{2kt}-1 \right) - \frac{x^{2}}{4kt} \\
 & = -\frac{1}{4kt} (y-x+2kt)^{2} + (kt-x)
\end{align}
$$
Now, using the substitution $u=(y-x+2kt) /\sqrt{ 4k t }$ and $dy=\sqrt{ 4kt }\, du$ the integral becomes:
$$
\begin{align}
\frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \exp \left\{  -\frac{1}{4kt}(y-x+2kt)^{2}+kt-x  \right\} \, dy & = \frac{1}{\sqrt{ 4\pi kt }} e^{ kt-x } (\sqrt{ 4kt }) \int_{0}^{\infty} e^{ -u^{2} } \, du \\
 & = \frac{1}{\sqrt{ \pi }} e^{ kt-x } \left( \frac{\sqrt{ \pi }}{2} \right) \\
 & = \frac{1}{2} e^{ kt-x }
\end{align}
$$
The second integral is much the same. First complete the square.
$$
\begin{align}
-\frac{(x+y)^{2}}{4kt} -y & = -\frac{x^{2}}{4kt} - \frac{xy}{2kt} - \frac{y^{2}}{4kt} - y = -\frac{1}{4kt}y^{2} - y\left( \frac{x}{2kt}+1 \right) - \frac{x^{2}}{4kt} \\
 & = -\frac{1}{4kt} (y + x+2kt)^{2} + (kt+x)
\end{align}
$$
Use the substitution $u=(y+x+2kt) /\sqrt{ 4kt }$ and $dy=\sqrt{ 4kt } \, du$. The integral becomes:
$$
\begin{align}
\frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \exp \left\{ -\frac{1}{4kt} (y + x+2kt)^{2} + (kt+x) \right\}  \, dy & = \frac{1}{\sqrt{ 4\pi kt }} e^{ kt+x } (\sqrt{ 4kt }) \int_{0}^{\infty} e^{ -u^{2} } \, du  \\
 & = \frac{1}{\sqrt{ \pi }} e^{ kt+x } \left( \frac{\sqrt{ \pi }}{2} \right) \\
 & = \frac{1}{2} e^{ kt+x }
\end{align}
$$
Substituting these results back into the original integral:
$$
u(x, t) = \frac{1}{2} e^{ kt-x } - \frac{1}{2}e^{ kt+x } = \frac{e^{ kt }}{2} (e^{ -x }-e^{ x }) = -e^{ kt } \sinh(x)
$$
From the boundary conditions:
$$
u(0, t) = -e^{ kt } \sinh(0) = 0=1
$$
- I don't really know where I went wrong here
### Question 4
This is the Neumann problem for the wave equation. Solutions follow the form:
$$
w(x, t)= \begin{cases}
\frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right] +\frac{1}{2c}\int_{x-ct}^{x+ct} \psi(y) \, dy  &  & x>ct \\
\frac{1}{2}\left[ \phi(x+ct)+\phi(ct-x) \right] + \frac{1}{2c}\int_{0}^{ct-x} \psi(y) \, dy +\frac{1}{2c}\int_{0}^{x+ct} \psi(y) \, dy  &  & 0<x<ct
\end{cases}
$$
Where $u(x, 0)=\phi(x)$ and $u_{t}(x, 0)=\psi(x)$. In this case, we have:
$$
\phi(x) = x \qquad \psi(x)=0
$$
In the case when $x>ct$ we have:
$$
\frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right] +\frac{1}{2c}\int_{x-ct}^{x+ct} \psi(y) \, dy = \frac{1}{2} \left[ x+ct+x-ct \right] + \frac{1}{2c} (0) = x
$$
in the case when $0<x<ct$ we have:
$$
\begin{align}
 & = \frac{1}{2}\left[ \phi(x+ct)+\phi(ct-x) \right] + \frac{1}{2c}\int_{0}^{ct-x} \psi(y) \, dy +\frac{1}{2c}\int_{0}^{x+ct} \psi(y) \, dy \\
 & = \frac{1}{2} \left[ x+ct +ct-x \right]  + \frac{1}{2c} (0) + \frac{1}{2c} (0) \\
 & = ct
\end{align}
$$
Therefore the full solution can be expressed as:
$$
u(x, t) = \begin{cases}
x & x>ct \\
ct & 0<x<ct
\end{cases}
$$
