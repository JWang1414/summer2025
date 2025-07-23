Theorem 29: Argument Principle
> Let $\Omega$ be a simply connected domain $f:\Omega\to \mathbb{C}$ such that $f$ is analytic except at finitely many poles. Let $\gamma$ be a simple closed contour that doesn't go through poles or zeroes of $f$. Then
$$
\frac{1}{2\pi i} \int _{\gamma} \frac{f'(z)}{f(z)} \, dz = \text{No. of zeroes in }\gamma - \text{No. of poles in }\gamma
$$
> For the function $f$

Note that the number of zeroes is counted with multiplicity. For example, if $f$ has a pole of order 2 and a zero of order 5, we get $5-2=3$.

Furthermore, another thing to note:
$$
\frac{1}{2\pi i} \int _{\gamma} \frac{f'(z)}{f(z)} \, dz = \frac{1}{2\pi} (\text{Change in arg}(f) )_{\gamma}
$$
This is the change in the argument of $f$ as $z$ goes around $\gamma$. For example, for the function $f(z)=z^{2}$ and $\gamma$ as the unit circle, after the transformation $f(\gamma)$ the unit circle now goes around the origin twice. So the change in the argument is $4\pi$.

---
Example:
$$
f(z)=z
$$
With $\gamma$ as the unit circle, oriented counterclockwise.
$$
\frac{1}{2\pi i} \int _{\gamma} \frac{f'}{f} \, dz = \frac{1}{2\pi i} \int _{\gamma} \frac{1}{z} \, dz = \frac{1}{2\pi} (\Delta \text{arg}(f))_{\gamma} = \frac{1}{2\pi} (2\pi) = 1
$$
---
Example:
$$
f(z) = z^{k}
$$
Where $k\in \mathbb{Z}$ and $\gamma$ is the unit circle.
$$
\frac{1}{2\pi i} \int _{\gamma} \frac{f'}{f} \, dz = \frac{1}{2\pi i} \int _{\gamma} \frac{kz^{k-1}}{z^{k}} \, dz
$$
By observation, $\Delta \text{arg}(f)=2\pi k$. This can be imagined as the number of times $f(\gamma)$ "winds around" $z=0$. Therefore, we conclude:
$$
\frac{1}{2\pi i} \int _{\gamma} \frac{f'}{f} \, dz = \frac{1}{2\pi} (\Delta \text{arg}(f))_{\gamma} = \frac{1}{2\pi} (2\pi k) = k
$$
---
Example:
Find the number of zeroes of $f(z)=z^{3}-2z^{2}+4$ in the first quadrant.

Defined $\gamma_{R}$ to be the quarter circle enclosing the first quadrant. By observation, $f$ has no poles. Hence, the number of zeroes (with multiplicity) is:
$$
\lim_{ R \to \infty } \frac{1}{2\pi i} \int_{\gamma_{R}} \frac{f'}{f} = \lim_{ R \to \infty } (\Delta \text{arg}(f))_{\gamma_{R}}
$$
Solve for the change in arg$(f)$.
...
