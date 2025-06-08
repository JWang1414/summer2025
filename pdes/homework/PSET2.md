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
