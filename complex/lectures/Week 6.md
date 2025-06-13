Example:
Let $\gamma$ be a circle $|z-a|=r$. Compute $\int_{\gamma} 1 /(z-a)^n$ where $n \in \mathbb{Z}$

Parametrize $\gamma$
$$
\gamma(t)=re^{ it }+a, t\in[0, 2\pi)
$$
Take the derivative of $\gamma(t)$
$$
\gamma'(t)=rie^{ it }
$$
Define the bounds and differential for the integral
$$
\int_{0}^{2\pi} \frac{rie^{ it }}{((re^{ it }+a)-a)^n} \, dt = i \int_{0}^{2\pi} (re^{ it })^{1-n} \, dx
$$
Which yields, two cases, when $n=1$ and when $n\neq 1$

Case 1: $n=1$
$$
2\pi i
$$
Case 2: $n\neq 1$
$$
\frac{ir^{1-n}e^{ it(1-m) }}{i(1-m)} \bigg|^{2\pi}_{0} = 0
$$
---
- Discussing Cauchy's integral theorem
- Call piece-wise smooth curves contours
- Domain $\Omega$ is called simply connected if the region inside every simple, closed contour in $\Omega$ is also inside $\Omega$
- Discussing Cauchy's integral formula
- A bunch of examples applying these theorems

Theorem:
> Let $f$ be analytic on the simple connected domain $\Omega$. Then all derivatives $f^{(k)}(z)$ where $k\in Z^{>0}$ exist and:
$$
f^{(k)}(a) = \frac{k!}{2\pi i} \int_{\gamma} \frac{f(z)}{(z-a)^{k+1}} \, dz
$$> Where $\gamma$ is any simple, closed, contour containing $a$
