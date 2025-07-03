For this section, define $f$ such that $f'$ is a continuous function
- All analytic functions have a continuous derivative
### Cauchy's Theorem
Suppose $f$ is analytic on a domain $D$. Let $\gamma$ be a piece-wise smooth simple closed curve in $D$ whose inside $\Omega$ also lies in $D$. Then:
$$
\int _{\gamma} f(z) \, dz =0
$$
- A piece-wise smooth curve is also called a *contour*

Definition:
> A domain $D$ is *simply-connected* if, whenever $\gamma$ is a simple closed curve in $D$, the inside of $\gamma$ is also a subset of $D$
- This can be visualised as: $D$ has no holes in it

Let $D$ be a simply-connected domain and $\Gamma$ a closed curve in $D$ that is composed of a finite number of horizontal and vertical line segments. If $f$ is analytic in $D$, then
$$
\int _{\Gamma}f(\xi) \, d\xi
$$
![[Pasted image 20250630135844.png]]
The above theorem states that the integral evaluated along this curve would be zero

If $f$ is analytic in a simply-connected domain $D$, then there is an analytic function $F$ on $D$ with $F'=f$ throughout $D$
- That is, the integral of such functions will always exist
### Cauchy's Formula
Suppose that $f$ is analytic on a domain $D$ and that $\gamma$ is a piece-wise smooth, positively oriented simple closed curve in $D$ whose inside $\Omega$ also lies in $D$. Then:
$$
f(z) = \frac{1}{2\pi i} \int _{\gamma} \frac{f(\xi)}{\xi-z} \, d\xi \text{ for all } z\in \Omega
$$
Suppose $f$ is analytic on the simply-connected domain $\Omega$. Then, all derivative $f^{(k)}(z)$ where $k\in \mathbb{Z}^{>0}$ exist and:
$$
f^{(k)}(a) = \frac{k!}{2\pi i} \int _{\gamma} \frac{f(z)}{(z-a)^{k+1}} \, dz
$$
Where $\gamma$ is any simple closed contour containing $a$
### Worked Examples
---
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
