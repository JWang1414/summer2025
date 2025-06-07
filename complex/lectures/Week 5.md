### Complex Integration
For some function $f : [a, b]\to \mathbb{C}$ be $f(t)=u(t)+iv(t)$. Then,
$$
\int_{a}^{b} f(t) \, dt := \int_{a}^{b} u(t) \, dt +i \int_{a}^{b} v(t) \, dt
$$
---
Example:
Let $\lambda \in \mathbb{C}$, compute:
$$
\int_{0}^{1} (1+\lambda t)^{2} \, dt = \int_{0}^{1} 1+2\lambda t+\lambda^{2}t^{2} \, dt = 1+\lambda+\frac{\lambda^{2}}{3}
$$
---
A complex curve is some $\gamma : [a, b]\to \mathbb{C}$
- It has starting point $\gamma(a)$ and ending point $\gamma(b)$
- $\gamma$ is a curve or the image $\gamma([a, b])$ is a curve

INSERT DIAGRAM HERE

Note that numerous different curves can project the same image into another space. This is known as numerous curves having an identical *parameterization*

INSERT DIAGRAM HERE

Let $z,w\in \mathbb{C}$, the straight line from $z$ to $w$ has parameterization
$$
\gamma(t) = (1-t)z+tw\text{, with }t\in[0,1]
$$
A circle is parameterized as:
$$
\gamma(t) = e^{ it }\text{, with }t\in[0,2\pi]
$$
> A curve is *simple* if for all $t\neq s$, $\gamma(t)\neq \gamma(t)$, except possibly at the endpoints

> A curve is *closed* if $\gamma(a)=\gamma(b)$

- I can't read this part, something about functions being smooth

Let $f:\Omega \in \mathbb{C}\to \mathbb{C}$ be piece-wise continuous on a piece-wise smooth curve $\gamma(:[a, b])\to C$. Then:
$$
\int_{\gamma} f(z) \, dz := \int_{a}^{b} f(\gamma(t))\gamma'(t) \, dt
$$
- Defined regardless of parameterization

Properties of the line integral:
- It is linear
- $\int_{-\gamma}f=-\int_{\gamma}f$ if we defined $-\gamma$ as $\gamma$ with the opposite orientation
- $\int_{\gamma}f = \sum_{i=1}^{N}\int_{\gamma_{i}}f$

If no orientation is specified for a closed curve, we assume it is counterclockwise, or positive.

---
Example: Let $\gamma$ be a semi-circle from 1 to -1 in the top-half of the plane. Compute
$$
\int_{\gamma} |z|+\ln z \, dz
$$
Parameterize $\gamma(t)=e^{ 2i\pi t }$ on $t\in[0,1 /2]$

Compute $\gamma'=2\pi ie^{ 2\pi it }$

Integrate:
$$
\int_{\gamma} |z|+\ln z \, dx = \int_{0}^{1 /2} \left[ |e^{ 2\pi it } + \ln|e^{ 2\pi it }| \right] (2\pi ie^{ 2\pi it }) \, dt
$$
- Everything from here is computations
---
Example: Let $\gamma$ be a straight line from $i$ to $\pi+i$. Compute
$$
\int_{\gamma}\cos ^{2}z \, dz
$$
Parameterize $\gamma(t)=(1-t)i+t(\pi+i) = i-it+t\pi+ti = i+t\pi$ for $t\in[0,1]$

Compute $\gamma'=\pi$

Integrate:
$$
\int_{\gamma}\cos ^{2}z \, dz = \pi \int_{0}^{1} \cos ^{2}(i+t\pi) \, dt = \frac{\pi}{2}
$$
---
