### Class Notes
Laurent Series
If $f$ is analytic on an annulus $r<|z-z_{0}|<R$ where $r\geq 0$ around $z_{0}$. Then,
$$
f(z) = \sum_{n=-\infty}^{\infty} a_{n}(z-z_{0})^{n}
$$
Where
$$
a_{n} = \frac{1}{2\pi i} \int_{\gamma} \frac{f(\omega)}{(\omega-z_{0})^{n+1}} \, d\omega
$$
The curve $\gamma$ is defined to be one that lies within the annulus and goes around $z_{0}$ once.

Definition:
The residue at $z=z_{0}$ of $f$ (analytic in $r<|z-z_{0}|<R$) is:
$$
\frac{1}{2\pi i} \int _{\gamma}f(\omega) \, d\omega
$$
Where $\gamma$ is in the annulus and goes around $z_{0}$ once.
- Notice that this is equivalent to the -1 term in the Laurent series
- If $f$ is analytic on $D(z_{0})\Rightarrow \text{residue}=0$
