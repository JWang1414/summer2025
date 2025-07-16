### Class notes
Computing definite integrals with residue theorem.

There are a number of different types of integrals we can compute with residue theorem.

Type 1:
$$
\int_{-\infty}^{\infty} \frac{P(x)}{Q(x)} \, dx
$$
Where $P$ is a polynomial and $Q$ has no real roots such that $\text{deg}(Q)\geq \text{deg}(P)+2$. We also require that $\lim_{ x \to \infty } \frac{P}{Q}$ can be evaluated, and the indefinite integral converges.

In this case, the full integral is equal to:
$$
2\pi i \sum_{z_{i}\in \Omega}\text{Res}\left( \frac{P}{Q}, z_{i} \right)
$$
Where $z_{i}$ are the roots of $Q$, and $\Omega$ is the upper half plane

---
Example:
$$
\int_{-\infty}^{\infty} \frac{1}{(1+x^{2})^{2}} \, dx = \int_{-\infty}^{\infty} \frac{1}{(x+i)^{2}(x-i)^{2}} \, dx
$$
This has one pole at $z=i$ in the upper hemisphere, with order 2

Calculate the summation of residues:
$$
2\pi i \left( \frac{d}{dx} \left( \frac{1}{(x+i)^{2}} \right)_{x=i} \right) = 2\pi i \left( -\frac{2}{(x+i)^{3}} \right)_{x=i} = \frac{\pi}{2}
$$
---

Type 2:
$$
\int_{-\infty}^{\infty} r(x)\sin x \, dx \qquad \int_{-\infty}^{\infty} r(x)\cos x \, dx
$$
Where $r(x)$ is a rational function

The strategy towards evaluating this will be to use:
$$
\int _{\gamma_{R}}r(z)e^{ iz } \, dx = \int _{\gamma_{1}}r(z)e^{ iz } \, dx + \int _{\gamma_{2}} r(z)e^{ iz } \, dx
$$
Where $\gamma_{R}$ is a semicircle enclosing the upper half plane. $\gamma_{1}$ goes along the real axis, and $\gamma_{2}$ goes around.

If $r(x)=p /q$ where $deg(q)\geq deg(p)+2$ then we can repeat the same process for type 1.

---
Example:
$$
\int_{-\infty}^{\infty} \frac{\cos x}{x^{2}+a^{2}} \, dx
$$
Where $a>1$. Then, this is equal to:
$$
\int _{\gamma_{1}} \frac{e^{ iz }}{z^{2}+a^{2}} \, dz = \int _{\gamma_{R}} \frac{e^{ iz }}{z^{2}+a^{2}} \, dz = 2\pi i \text{Res}(f, ia)
$$
Which is:
$$
= 2\pi i \left( \frac{e^{ iz }}{z+ia} \right)_{z=ia} = 2\pi i \left( \frac{e^{ -a }}{2ai} \right) = \frac{\pi}{a} e^{ -a }
$$
---
Example:
$$
\int_{-\infty}^{\infty} \frac{\cos(bx)}{x^{2}+\delta^{2}} \, dx = \frac{\pi}{\delta} e^{ -b\delta }
$$
The proof of this one is with a change of variables from the previous example. It's all just uninteresting computations so I didn't write it down.

---

