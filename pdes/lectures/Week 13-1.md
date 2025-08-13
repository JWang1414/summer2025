Example:
$$
\begin{cases}
u_{tt} = c^{2} u_{xx} & 0<x<l \\
u(0, t)=u(l, t)=0 \\
u(x, 0)=\sin\left( \frac{\pi x}{l} \right) & u_{t}(x, 0)=-\sin\left( \frac{\pi x}{l} \right)
\end{cases}
$$
Let $F(x, s)$ denote the $\mathcal{L}$ transform of $u$ with respect to $t$
$$
s^{2} F(x, s) - su(x, 0) - u_{t}(x, 0) = c^{2} F_{xx}(x, s)
$$
$$
s^{2} F(x, s) - s \sin\left( \frac{\pi x}{l} \right) + \sin \left( \frac{\pi x}{l} \right) = c^{2} F_{xx}
$$
$$
s^{2} F(x, s) + (1-s)\sin\left( \frac{\pi x}{l} \right) = c^{2} F_{xx}(x, s)
$$
With boundary conditions:
$$
F(0, s) = F(l, s)=0
$$
Solution has the form $A(s)=\sin\left( \frac{\pi x}{l} \right)$.
$$
s^{2} A(s) \sin\left( \frac{\pi x}{l} \right) + (1-s) \sin\left( \frac{\pi x}{l} \right) = -c^{2} A(s) \frac{\pi^{2}}{l^{2}} \sin\left( \frac{\pi x}{l} \right)
$$
From which we get that:
$$
A(s) =
$$
$$
F(x, s) = \left( \frac{s-1}{s^{2}+\frac{c^{2}\pi^{2}}{l^{2}}} \right) \sin\left( \frac{\pi x}{l} \right)
$$
Use Laplace inversion formula:
$$
u(x, t) = \sin\left( \frac{\pi x}{l} \right) \cos\left( \frac{c\pi}{l}t \right) - \frac{l}{c\pi} \sin\left( \frac{\pi x}{l} \right) \sin\left( \frac{c\pi}{l}t \right)
$$
$$
= \sin\left( \frac{\pi x}{l} \right)\left[ \cos\left( \frac{c\pi t}{l} -\frac{l}{c\pi} \sin\left( \frac{c\pi t}{l} \right) \right) \right]
$$
---
$$
\begin{cases}
u_{t} = ku_{xx} & \text{in }(0, l) \\
u(0, t)=u(l, t)=1 \\
u(x, 0)=1+\sin\left( \frac{\pi x}{l} \right)
\end{cases}
$$
Use $F$ to denote the Laplace transform $\mathcal{L}\{ u \}$.
$$
s F(x, s) - u(x, 0) = k F_{xx}(x, s)
$$
Boundary condition:
$$
F(0, s)=F(l, s)=\frac{1}{s}
$$
We have:
$$
sF(x, s) - \left( 1+\sin\left( \frac{\pi x}{l} \right) \right) = kF_{xx}
$$
Which is an ODE in $x$. This is the same ODE we just solved. If you solve it, the solution should be:
$$
F(x, s) = \frac{1}{s} + \frac{1}{s+\frac{k\pi^{2}}{l^{2}}} \sin\left( \frac{\pi x}{l} \right)
$$
After Laplace inversion:
$$
u(x, t) = 1 + e^{ -k\pi^{2}t/l^{2} } \sin\left( \frac{\pi x}{l} \right)
$$
---
Example:
$$
\begin{cases}
u_{tt} = c^{2} u_{xx} + \cos(\omega t) \sin(\omega x) & 0<x<1 \\
u(0, t)=u(1, t) = u(x, 0) = u_{t}(x, 0) = 0
\end{cases}
$$
Assume $\omega>0$, and be careful when $\omega=c\pi$. Begin with Laplace transforms:
$$
s^{2} F(x, s) - su(x, 0) - u_{t}(x, 0) = c^{2} F_{xx}(x, s) + \frac{s}{s^{2}+\omega^{2}} \sin(\pi x)
$$
Boundary conditions:
$$
F(0, s) = F(1, s) =0
$$
$$
F(x, s) = \frac{s}{(s^{2}+\omega^{2})(s^{2}+c^{2}\pi^{2})} \sin(\pi x)
$$
If $\omega \neq c\pi$ we have:
$$
\frac{s}{(s^{2}+\omega^{2})(s^{2}+c^{2}\pi^{2})} = \frac{1}{c^{2}\pi^{2}-\omega^{2}} \left( \frac{s}{s^{2}+\omega^{2}} - \frac{s}{s^{2}+c^{2}\pi^{2}} \right)
$$
Which is a known cosine transform, and so after Laplace inversion, we have:
$$
u(x, t)= \frac{1}{c^{2}\pi^{2} -\omega^{2}} \left( \cos(\omega t) - \cos(c\pi t) \right)  \sin(\pi x)
$$
If $\omega=c\pi$ we have:
$$
\frac{s}{(s^{2}+c^{2}\pi^{2})^{2}}
$$
And therefore:
$$
F(x, s) = \frac{s}{(s^{2}+c^{2}\pi^{2})^{2}} \sin(\pi x) = -\frac{1}{2} \frac{d}{ds} \left[ \frac{1}{s^{2}+c^{2}\pi^{2}} \right] \sin(\pi x)
$$
Invert the Laplace transform:
$$
u(x, t) = \frac{1}{2\pi c} t \sin(\pi ct) \sin(\pi x)
$$
---
Example:
$$
\begin{cases}
u_{t} = \kappa u_{xx} + \mu u_{x} & -\infty<x<\infty \\
u(x, 0) = \phi(x)
\end{cases}
$$
Where we require $u(x, t)$ to be bounded and $\kappa>0$.
- The term with $\mu$ is called the convection term

Fourier transform the problem,
$$
\begin{cases}
\hat{u}_{t}(k, t) = \kappa (ik)^{2} \hat{u} + \mu(ik)\hat{u}(k, t) \\
\hat{u}(k, 0) = \hat{\phi}(k)
\end{cases}
$$
Which gives us the problem:
$$
\hat{u}_{t} = (-\kappa k^{2} + i\mu k)\hat{u}
$$
Which is an ODE. It has the solution:
$$
\hat{u}(k, t) = \hat{\phi}(k)\exp \left\{ (-\kappa k^{2}+i\mu k)t \right\}
$$
Take the Fourier inversion:
$$
\begin{align}
u(x, t) & = \mathcal{F}^{-1}\{ \hat{\phi}(k) \exp \{ (-\kappa k^{2}+i\mu k)t \} \} = (\phi*g)(x)
\end{align}
$$
Where we have applied the convolution of Fourier transforms. However, we do not know the inverse Fourier transform of the exponential here. We need to calculate it:
$$
\begin{align}
g  & = \frac{1}{2\pi} \int_{-\infty}^{\infty} \exp \left[ (-\kappa k^{2}+i\mu k)t + ikx \right]  \, dk  \\
 & = \frac{1}{\sqrt{ 4\pi \kappa t }} \exp \left[ -\frac{(\mu t+x)^{2}}{}4\kappa t \right] 
\end{align}
$$
And so we conclude:
$$
u(x, t) = \frac{1}{\sqrt{ 4\pi \kappa t }} \int_{-\infty}^{\infty} \exp \left[ - \frac{(\mu t+x-y)^{2}}{4\kappa t} \right] \phi(y) \, dy
$$
