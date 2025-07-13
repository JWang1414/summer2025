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
If $f$ is analytic on $D_{r}(z_{0})\setminus \{ z_{0} \}$ then the *residue* is defined as:
$$
\text{Res}(f, z_{0}) = \frac{1}{2\pi i} \int _{\gamma}f(\omega) \, d\omega = a_{-1}
$$
Where $\gamma$ is in the annulus and goes around $z_{0}$ once.
- Notice that this is equivalent to the -1 term in the Laurent series
- If $f$ is analytic on $D(z_{0})\Rightarrow \text{residue}=0$

Definition:
If $f$ is analytic on a punctured disk at $z_{0}$ $\{ z : 0<|z-z_{0}|<r \}$ but not at $z_{0}$, then it has an *isolated singularity* at $z=z_{0}$
- If $f$ has isolated singularity at $z_{0}$ then it has a Laurent series at $z_{0}$

Definition:
A singularity $z=z_{0}$ is removable if $\exists M$ such that $|f(z)|<M$ in a nbhd around $z_{0}$

Theorem 24: Remann's theorem on removable singularities
If $f$ has removable singularity at $z=z_{0}$ and $f$ is analytic on $D_{r}(z_{0})\setminus \{ z_{0} \}=\{ z:0<|z-z_{0}|<r \}$. Then there exists an analytic function $g(z)$ on $D_{r}(z_{0})=\{ z:|z-z_{0}|<r \}$ such that $f(z)=g(z)$ on $D_{r}(z_{0})\setminus \{ z_{0} \}$. Moreover, Laurent series of $f$ has no coefficients of negative index ($a_{n}=0$ if $n<0$)

Definition:
A singularity $z=z_{0}$ is a *pole* if $\lim_{ z \to 0 }|f(z)|=\infty$

Theorem 25:
If $f$ has a pole at $z=z_{0}$, then $\exists m$ such that $f(z)=g(z) /(z-z_{0})^{m}$ such that $g$ is analytic and $g(z_{0})\neq 0$
- This $m$ is the order of the pole at $z_{0}$

Definition:
A singularity $z=z_{0}$ is called *essential* if it is not removable and not a pole

Theorem 26: Picard's Great Theorem
If $f$ has an essential singularity at $z-z_{0}$, then on any nbhd of $z_{0}$, $f$ takes on all possible values in $\mathbb{C}$ except possibly 1
- Furthermore, its Laurent series has an $\infty$ number of non-zero coefficients of negative index

If $f$ has a pole of order $k$ at $z_{0}$, such as:
$$
f(z) = \frac{g(z)}{(z-z_{0})^{k}}
$$
Such that $g(z_{0})\neq 0$ and $g$ is analytic, then
$$
\text{Res}(f, z_{0}) = \frac{g^{(k-1)}(z_{0})}{(k-1)!}
$$
Theorem 28: Residue Theorem
Let $u$ be a simply connected domain and $\{ z_{1}, \dots, z_{n} \}$ is a finite collection of points in $u$. Let $f:u\setminus \{ z_{1}, \dots, z_{n} \}\to \mathbb{C}$ be analytic. Let $\gamma$ be a closed contour not going through of the points $z_{i}$ (oriented counter-clockwise). Then:
$$
\int _{\gamma}f(z) \, dz = 2\pi i \sum_{z_{i}\text{ in }\gamma} \text{Res}(f, z_{i})
$$
- That is, the residue around all these small individual points will sum up to the residue around the entire domain
- Very useful for computing integrals with discontinuities
