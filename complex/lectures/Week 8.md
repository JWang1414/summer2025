### Isolated Singularities
An analytic function $f$ has an *isolated singularity* at a point $z_{0}$ if $f$ is analytic in the punctured disc $0<|z-z_{0}|<r$, for some $r>0$
- We are interested in isolated singularities because they are helpful in computing definite integrals and have applications in flows and fields
- They will be used in the Residue Theorem

There are three possible behaviours for some $|f|$ when $0<|z-z_{0}|<R$
1. $|f(z)|$ remains bounded as $z\to z_{0}$
2. $\lim_{ z \to z_{0} }|f(z)|=\infty$
3. Neither 1 or 2
### Removable Singularities
Suppose that we have a singularity of type 1. Example:
$$
f(z) = \frac{(z^{2}-z_{0}^{2})}{z-z_{0}}
$$
Define another function
$$
g(z) = \begin{cases}
(z-z_{0})^{2} f(z),  & 0<|z-z_{0}|<r \\
0, & z=z_{0}
\end{cases}
$$
Then, the function is analytic for $0<|z-z_{0}|<r$ and differentiable at $z_{0}$ with the derivative:
$$
\lim_{ z \to z_{0} } \frac{g(z)-g(z_{0})}{z-z_{0}} = \lim_{ z \to z_{0} } (z-z_{0}) f(z) =0
$$
Since $g$ is analytic on the disc $|z-z_{0}|<r$, we know that $g$ has a valid power series expansion on this domain:
$$
g(z) = b_{0} + b_{1}(z-z_{0}) + b_{2}(z-z_{0})^{2} + \dots
$$
$g(z_{0})=0$ by definition and therefore $b_{0}=0$. $g'(z_{0})=0$ as just computed and therefore $b_{1}=0$. Hence, we can now claim that:
$$
f(z) = \frac{g(z)}{(z-z_{0})^{2}} = b_{2} + b_{3}(z-z_{0}) + \dots
$$
We have obtained a valid power series expansion for $f(z)$ and so can further conclude that $f$ is analytic on $\left| z-z_{0} \right|<r$.

When $f$ can be extended to be analytic on the disc $\left| z-z_{0} \right|<r$ we call $z_{0}$ are removable singularity for $f$.
### Poles
Suppose that we have a singularity of type 2. Since our function $|f(z)|\to \infty$ , we can roughly claim that $g(z)=1 /f(z)\to 0$ at $g(z_{0})$. Now define the function:
$$
g(z) = (z-z_{0})^{m}h(z)
$$
Where $h$ is analytic on the disc $\{ z:\left| z-z_{0} \right|<r \}$ and $h(z_{0})\neq 0$. Since $g$ does not vanish on the punctured disc, neither does $h$. Therefore, the function $H(z)=1 /h(z)$ is also analytic on the disc $\{ z:\left| z-z_{0} \right|<r \}$. From which we can conclude:
$$
f(z) = \frac{1}{g(z)} = \frac{1}{(z-z_{0})^{m}} \frac{1}{h(z)} = \frac{H(z)}{(z-z_{0})^{m}}
$$
We claim that $|f(z)|$ grows to infinity as $z\to z_{0}$ like some power of $1 /\left| z-z_{0} \right|$. The integer $m$ is the *order of the pole* is the same as the order of the zero of $1 /f$ at $z_{0}$.
### Essential Singularities
If we have a singularity of type 3, then $z_{0}$ is called essential. We cannot remove it.

Eg:
$$
h(z) = e^{ 1/z }
$$
### Computation of Residues
The residue of $f$ at $z_{0}$ is defined to be:
$$
\text{Res}(f;z_{0}) = \frac{1}{2\pi i} \int _{|\zeta-z_{0}|=s} f(\zeta) \, d\zeta
$$
Interestingly, it is possible to prove that the value of this integral is the same for all $s$ such that $0<s<r$

When $f$ has a pole at $z_{0}$ recall the representation:
$$
f(z) = \frac{H(z)}{(z-z_{0})^{m}}
$$
$H(z)$ has a power series expansion such that:
$$
f(z) = \frac{c_{0}}{(z-z_{0})^{m}} + \dots + \frac{c_{m-1}}{(z-z_{0})} + c_{m} + c_{m+1} (z-z_{0}) + \dots
$$
Recall that, from Cauchy's Theorem, for any given $j\in \mathbb{Z}$
$$
\frac{1}{2\pi i} \int _{|z-z_{0}|=s} (z-z_{0})^{j} \, dz = \begin{cases}
1 & \text{if }j=-1 \\
0 & \text{otherwise}
\end{cases}
$$
We conclude:
$$
\text{Res}(f;z_{0}) = c_{m-1} = \frac{H^{(m-1)}(z_{0})}{(m-1)!}
$$
Therefore, it is always possible to find the residue of a function $f$ with a pole at $z_{0}$ by writing the expansion of $f$ in positive and negative powers of $z-z_{0}$
### Laurent Series
A function analytic on an annulus $0\leq r<|z-z_{0}|<R$ can be represented as a power series called a Laurent series. It claims that our function $f(z)$ can be represented as:
$$
f(z) = f_{1}(z) + f_{2}(z), \qquad r<|z-z_{0}|<R
$$
Where $f_{1}$ is analytic on the disc $|z-z_{0}|<R$ and $f_{2}$ is analytic on the region $r<|z-z_{0}|$ including at $\infty$. $f_{1}$ has a power series in the variable $z-z_{0}$ and $f_{2}$ has a power series in the variable $(z-z_{0})^{-1}$.
$$
f(z) = \sum_{k=0}^{\infty} a_{k}(z-z_{0})^{k} + \sum_{k=1}^{\infty} b_{k} (z-z_{0})^{-k}
$$
or,
$$
f(z) = \sum_{k=-\infty}^{\infty} a_{k}(z-z_{0})^{k}, \text{where }a_{-k}=b_{k}
$$
In the case of a singularity such that we may choose $r_{1}$ and $R_{1}$ with:
$$
r<r_{1}<|z-z_{0}|<R_{1}<R
$$
The coefficients are:
$$
a_{k} = \frac{1}{2\pi i} \int _{|w-z_{0}|=s} \frac{f(w)}{(w-z_{0})^{k+1}} \, dw
$$
Notice that the function $H(z)$ is a Laurent series, but written with different notation. As a Laurent series, we can see:
$$
H(z) = \sum_{k=0}^{\infty} c_{k}(z-z_{0})^{k}
$$
Where $c_{k}$ has been taken from the function $f(z)$ it is representing.
### Class Notes
Laurent Series
> If $f$ is analytic on an annulus $r<|z-z_{0}|<R$ where $r\geq 0$ around $z_{0}$. Then,
$$
f(z) = \sum_{n=-\infty}^{\infty} a_{n}(z-z_{0})^{n}
$$
> Where
$$
a_{n} = \frac{1}{2\pi i} \int_{\gamma} \frac{f(\omega)}{(\omega-z_{0})^{n+1}} \, d\omega
$$
> The curve $\gamma$ is defined to be one that lies within the annulus and goes around $z_{0}$ once.

Definition:
> If $f$ is analytic on $D_{r}(z_{0})\setminus \{ z_{0} \}$ then the *residue* is defined as:
$$
\text{Res}(f, z_{0}) = \frac{1}{2\pi i} \int _{\gamma}f(\omega) \, d\omega = a_{-1}
$$
> Where $\gamma$ is in the annulus and goes around $z_{0}$ once.
- Notice that this is equivalent to the -1 term in the Laurent series
- If $f$ is analytic on $D(z_{0})\Rightarrow \text{residue}=0$

Definition:
> If $f$ is analytic on a punctured disk at $z_{0}$ $\{ z : 0<|z-z_{0}|<r \}$ but not at $z_{0}$, then it has an *isolated singularity* at $z=z_{0}$
- If $f$ has isolated singularity at $z_{0}$ then it has a Laurent series at $z_{0}$

Definition:
> A singularity $z=z_{0}$ is removable if $\exists M$ such that $|f(z)|<M$ in a nbhd around $z_{0}$

Theorem 24: Remann's theorem on removable singularities
If $f$ has removable singularity at $z=z_{0}$ and $f$ is analytic on $D_{r}(z_{0})\setminus \{ z_{0} \}=\{ z:0<|z-z_{0}|<r \}$. Then there exists an analytic function $g(z)$ on $D_{r}(z_{0})=\{ z:|z-z_{0}|<r \}$ such that $f(z)=g(z)$ on $D_{r}(z_{0})\setminus \{ z_{0} \}$. Moreover, Laurent series of $f$ has no coefficients of negative index ($a_{n}=0$ if $n<0$)

Definition:
> A singularity $z=z_{0}$ is a *pole* if $\lim_{ z \to 0 }|f(z)|=\infty$

Theorem 25:
> If $f$ has a pole at $z=z_{0}$, then $\exists m$ such that $f(z)=g(z) /(z-z_{0})^{m}$ such that $g$ is analytic and $g(z_{0})\neq 0$
- This $m$ is the order of the pole at $z_{0}$

Definition:
> A singularity $z=z_{0}$ is called *essential* if it is not removable and not a pole

Theorem 26: Picard's Great Theorem
> If $f$ has an essential singularity at $z-z_{0}$, then on any nbhd of $z_{0}$, $f$ takes on all possible values in $\mathbb{C}$ except possibly 1
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
> Let $u$ be a simply connected domain and $\{ z_{1}, \dots, z_{n} \}$ is a finite collection of points in $u$. Let $f:u\setminus \{ z_{1}, \dots, z_{n} \}\to \mathbb{C}$ be analytic. Let $\gamma$ be a closed contour not going through of the points $z_{i}$ (oriented counter-clockwise). Then:
$$
\int _{\gamma}f(z) \, dz = 2\pi i \sum_{z_{i}\text{ in }\gamma} \text{Res}(f, z_{i})
$$
- That is, the residue around all these small individual points will sum up to the residue around the entire domain
- Very useful for computing integrals with discontinuities

### Applications of Residue Theorem
The Residue Theorem:
Suppose that $f$ is analytic on a simply-connected domain $D$ except for a finite number of isolated singularities at points $z_{1}, \dots, z_{N}$ of $D$. Let $\gamma$ be a piecewise smooth positively oriented simple closed curve in $D$ that does not pass through any of the point $z_{1}, \dots, z_{N}$. Then
$$
\int _{\gamma}f(z) \, dz = 2\pi i \sum_{z_{k}\text{ inside }\gamma} \text{Res}(f;z_{k})
$$
Where the sum is taken over all the singularities $z_{k}$ of $f$ that lie inside $\gamma$

Suppose $P$ and $Q$ are polynomials that are real-values on the real axis and for which the degree of $Q$ exceeds the degree of $P$ by 2 or more. If $Q(x)\neq 0$ for all real $x$ then:
$$
\int_{-\infty}^{\infty} \frac{P(x)}{Q(x)} \, dx = 2\pi i \sum_{U} \text{Res}\left( \frac{P}{Q};z_{j} \right)
$$
Where the sum is taken over all the poles of $P /Q$ that lie in the upper half-plane $U=\{ z:\mathrm{Im}(z)>0 \}$
