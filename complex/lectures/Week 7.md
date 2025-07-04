Max Modulus Principle:
If $f$ is analytic, non-constant on domain $\Omega$ then $|f|$ has no max on $\Omega$

Alternatively, if $f$ is continuous on the closed bounded set $B$, and analytic on the interior of $B$, then the max of $|f(z)|$ occurs on boundary of $B$
- If $f(z)\neq 0$ then you can apply the max mod principle to $1 /f(z)$ to obtain the min mod principle

Taylor Series Theorem:
If $f$ is analytic on domain $\Omega$, then, for some $z_{0}\in \Omega$
$$
f(z) = \sum_{k=0}^{\infty} \frac{f^{(k)}(z_{0})(z-z_{0})^{k}}{k!} = \sum_{k=0}^{\infty} \frac{1}{2\pi i} \left[ \int _{\gamma} \frac{f(\omega)}{(\omega-z_{0})^{k+1}} \, d\omega  \right] (z-z_{0})^{k}
$$
- Notice that for real functions, analytic means that a function is equal to its Taylor series
### Taylor Series Review
Let $S(z) = \sum_{k} a_{k}(z-a)^{k}$

The radius of convergence, $R$, of $S(z)$ is such that:
- $|z-a|<R \Rightarrow S(z)$ is convergent
- $|z-a|>R\Rightarrow S(z)$ is divergent

- Explanations of the ratio and root test here
	- Board text is too small to read
- Taylor series are summations. Derivatives and integrals commute

If $f(z)=S(z)$ and $g(z)=T(z)$ are both Taylor series then:
- $fg=ST$
- $f+g=S+T$

Definition:
If $f(a)=0$, $f$ is analytic, non-constant, $f=\sum a_{k}(z-a)^{k}$ then $\exists n\in \mathbb{N}$ such that
$$
f(z) = (z-a)^{n} \sum_{k=n+1}^{\infty} a_{k}(z-a)^{k-n}
$$
Where the summation here when $z=a$ is never equal to zero. We call the $n$ the order of $z=a$
- The order of $z=a$ is the order of first non-zero derivatives at $z=a$

Theorem:
Zeros of all non-zero analytic function are isolated
- This can be interpreted as: the zeroes for this function do not group up in arbitrarily small spaces

Theorem:
If $f$ vanishes on an open disk $D$ or on a curve $\gamma$, then $f$ is identically 0 on any domain containing $D$ or $\gamma$

Theorem:
Define two functions $f$ and $g$ such that $f$ is continuous on $\Omega_{1}\cup \gamma$ and analytic on $\Omega_{1}$, $g$ is continuous on $\Omega_{2}\cup \gamma$ and analytic on $\Omega_{2}$. If $f=g$ on $\gamma$ then:
$$
h(z) = \begin{cases}
f(z)\text{ in }\Omega_{1} \\
g(z)\text{ in } \Omega_{2} \\
f(z)=g(z)\text{ on }\gamma
\end{cases}\text{ is analytic on } \Omega_{1}\cup \Omega_{2}\cup \gamma
$$
### Laurent Series
Consider the function $f(z) = 1 /(1-z)$
- Not analytic at $z=1$
- If $z<1$ then it has a convergent Taylor series centred at 0

However, if $|z|>1$ then the function is analytic. But it is not analytic on the disk of radius $|z|$ centred at 0

Instead:
$$
f(z) = \frac{1}{1-z} = \frac{1}{z\left( \frac{1}{z}-1 \right)} = -\frac{1}{z} \left[ \frac{1}{1-\frac{1}{z}} \right] = -\frac{1}{z} \sum_{k=0}^{\infty} \left( \frac{1}{z} \right)^{k} = -\sum_{k=0}^{\infty} \left( \frac{1}{z} \right)^{k+1}
$$
This final term is called a Laurent series

Laurent series are for functions analytic on an annulus. For our function $f(z)$ the annulus can be $|z|>1$

Theorem:
If $0\leq r<R\leq \infty$ and $u=\{ z : r<|z-z_{0}|<R \}$ and $f:u\to \mathbb{C}$ is analytic, then $f$ has a Laurent series
$$
f(z) = \sum_{k=0}^{\infty} a_{k}(z-z_{0})^{k}
$$
Where:
$$
a_{k} = \frac{1}{2\pi i} \int _{\gamma} \frac{f(\omega)}{(\omega-z_{0})^{k+1}} \, d\omega
$$
$\gamma$ is any closed curve $u$ circling $z_{0}$
