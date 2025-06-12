### Curves
Defined as a continuous complex-valued function $\gamma(t)$ on some interval $[a, b]$ in the real axis. It begins at $\gamma(a)$ and ends at $\gamma(b)$. The reverse orientation is denoted $-\gamma$.
- A positively-oriented circle would go counter-clockwise.

Definition:
> A curve is called *simple* if $\gamma(t_{1})\neq \gamma(t_{2})$ when $a\leq t_{1}<t_{2}<b$

Definition:
> A curve is called *closed* if $\gamma(a)=\gamma(b)$

Jordan Curve Theorem:
> The complement of the range of a curve that is both simple and closed consists of two disjoint, open, connected sets. The one inside the curve is bounded, and the one outside the curve is unbounded.
- Think of the inside and outside of a circle

Define some curve $\gamma(t)=x(t)+iy(t)$, where $a\leq t\leq b$ such that $x(t)$ and $y(t)$ are real-valued functions. If both functions are differentiable at $t_{0}$, then, we define the derivative to be:
$$
\gamma'(t_{0})=x'(t_{0})+iy'(t_{0})
$$
Definition:
> If $\gamma'(t)$ exists and is continuous on $[a, b]$, then $\gamma$ is called *smooth*

Definition:
> If $\gamma$ is composed of a finite number of smooth curves, one coinciding with the beginning of the next, then it is called *piece-wise smooth*

The same curve can be represented in numerous different ways. This is known as having an identical *parametrization*. For example $t$ on $[0,1]$ is the same as $2t$ on $[0, 1 /2]$.

Let $z,w\in \mathbb{C}$, the straight line from $z$ to $w$ has parametrization
$$
\gamma(t) = (1-t)z+tw\text{, with }t\in[0,1]
$$
A circle is parametrized as:
$$
\gamma(t) = e^{ it }\text{, with }t\in[0,2\pi]
$$
### Complex Integration
For some function $f : [a, b]\to \mathbb{C}$ be $f(t)=u(t)+iv(t)$. Then,
$$
\int_{a}^{b} f(t) \, dt = \int_{a}^{b} u(t) \, dt +i \int_{a}^{b} v(t) \, dt
$$
Given a smooth curve $\gamma$, and that $u$ is continuous in the range of $\gamma$, the line integral is defined as:
$$
\int_{\gamma} u(z) \, dz = \int_{a}^{b} u(\gamma(t))\gamma'(t) \, dt
$$
For a piece-wise smooth curve, we instead have
$$
\int_{\gamma}u(z) \, dz = \sum_{j=0}^{n-1} \int_{t_{j}}^{t_{j+1}} u(\gamma(s))\gamma'(s) \, ds
$$
Where the points $t_{0},t_{1},\dots,t_{n}$ are the points of discontinuity over the interval.
### Integral Properties
A line integral on the curve $-\gamma$ is:
$$
\int_{-\gamma}u(z) \, dz = -\int_{\gamma}u(z) \, dz
$$
Define two curves $\gamma_{1}$ and $\gamma_{2}$ with intervals $[a_{1}, b_{1}]$ and $[a_{2}, b_{2}]$. If $\gamma_{1}(b_{1})=\gamma_{2}(a_{2})$ then,
$$
\int_{\gamma_{1}+\gamma_{2}}u(z) \, dz = \int_{\gamma_{1}} u(z) \, dz + \int_{\gamma_{2}} u(z) \, dz
$$
For some complex-valued, continuous function $g$ on $[a, b]$:
$$
\left| \int_{a}^{b} g(t) \, dt  \right| \leq \int_{a}^{b} \left| g(t) \right|  \, dt 
$$
Let $p$ and $q$ be two distinct points on the plane. Suppose that $\gamma_{1}$ and $\gamma_{2}$ are two piece-wise smooth curves from $p$ to $q$. Then, $\gamma=\gamma_{1}-\gamma_{2}$ is a closed piece-wise smooth curve. For $m=0, 1, 2, \dots$
$$
\int_{\gamma} z^m \, dz = \int_{\gamma_{1}} z^m \, dz - \int_{\gamma_{2}} z^m \, dz = 0
$$
This is to say that the integral of $z^m$ along any curve joining $p$ and $q$ doesn't depend on the curve, but only on $p$, $q$, and $m$. Furthermore, we can claim that the value of an integral does not depend on our choice of parametrization.