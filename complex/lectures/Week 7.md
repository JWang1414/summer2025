Theorem 1:
> Suppose that $f$ is analytic on a domain $D$ and $z_{0}$ is a point of $D$. If the disc $\{ z:|z-z_{0}|<R \}$ lies in $D$, then $f$ has a power series:
$$
f(z) = \sum_{k=0}^{\infty} a_{k}(z-z_{0})^{k}
$$
> valid in this disc. Furthermore, the coefficients are given by:
$$
a_{k} = \frac{1}{2\pi i} \int _{\gamma} \frac{f(\zeta)}{(\zeta-z_{0})^{k+1}} \, d\zeta
$$
> where $\gamma$ is the positively oriented circle $\{ \zeta : \left| \zeta - z_{0} \right|=r \}$ are $r$ is any positive number less than $R$

From Theorem 1: If $f$ is analytic on domain $D$, then so is $f'$. Hence, $f$ has derivative of all orders, and each derivative is analytic on $D$.
- Since on every disc in $D$, $f$ is given by a power series, we can claim $f$ is infinitely differentiable because power series are infinitely differentiable
- From the existence of one derivative, we may assume the existence of infinite

Recall a number of fundamental Taylor series:
$$
\begin{align}
\log(1-z) = - \sum_{n=1}^{\infty} \frac{z^{n}}{n} &  & \cosh z = \sum_{k=0}^{\infty} \frac{z^{2k}}{(2k)!} &  & \sinh z = \sum_{k=0}^{\infty} \frac{z^{2k+1}}{(2k+1)!}
\end{align}
$$
- The Taylor series for $\log$ is valid for $|z|<1$
- The Taylor series for $\cosh$ and $\sinh$ are valid for all $z$

From Theorem 1: Suppose that $f$ is analytic on a domain $D$ and, further, at some point $z_{0}\in D$, $f^{(k)}(z_{0})=0$, $k=0,1,2,\dots$ Then $f(z)=0$ for all $z\in D$
### Order of a Zero
Suppose that $f$ is analytic and not identically zero on a domain $D$, and $f(z_{0})=0$ for some $z_{0}\in D$. Thus, the power series for $f$ centred at $z_{0}$ is:
$$
f(z) = a_{1}(z-z_{0}) + a_{2}(z-z_{0})^{2} + \dots
$$
Not all the coefficients $a_{k}$ can vanish, so there is an integer $m\geq 1$ such that
$$
a_{1}=\dots=a_{m-1} =0, \qquad \text{ but } a_{m}\neq 0
$$
Therefore
$$
f(z) = a_{m}(z-z_{0})^{m} + a_{m+1}(z-z_{0})^{m+1} + \dots, \qquad a_{m}\neq 0
$$
This means that $f^{(k)}(z_{0})=0$ for $k=0, \dots, m-1$, but $f^{(m)}(z_{0})\neq 0$. We say that $f$ has a zero of order $m$ at $z_{0}$.

If $f$ has a zero of order $m$ at $z_{0}$, then $f(z)=(z-z_{0})^m g(z)$, where $g$ is analytic on $D$ and $g(z_{0})\neq 0$. That is, we can claim that the function:
$$
g(z) = \frac{f(z)}{(z-z_{0})^{m}}
$$
is analytic on the domain $D\setminus \{ z_{0} \}$.
### Morera's Theorem
Morera's Theorem:
> If $f$ is a continuous function on a domain $D$ and if
$$
\int _{\gamma}f(z) \, dz =0
$$
> for every simple closed contour $\gamma$ lying in $D$, then $f(z)$ is analytic in $D$

This theorem has numerous consequences, which will now be detailed in the following sections.

Liouville's Theorem:
> If $F$ is entire and if there is a constant $M$ such that $|F(z)|\leq M$ for all $z$, then $F$ is identically constant.

Fundamental Theorem of Algebra:
For any polynomial
$$
P(z) = a_{0} + a_{1}z + \dots + a_{m}z^{m}, \qquad (a_{m}\neq 0)
$$
Where $m\geq 1$ has at least one point $z=a$ such that $P(a)=0$. That is, $P(z)$ has at least one root

Maximum Principles:
> If $f(z)$ is analytic on domain $D$, then $|f(z)|$ cannot have a maximum in $D$ unless $f(z)$ is a constant.

> If $f(z)$ is analytic in a bounded region $D$ and $|f(z)|$ is continuous in the closed region $\bar{D}$, then $|f(z)|$ assumes it maximum on the boundary of the region.

Note that using a similar proof to the maximum principles, one may establish the minimum principle, stating that $f(z)$ must attain its minima on the boundary.
### Class notes
Max Modulus Principle:
> If $f$ is analytic, non-constant on domain $\Omega$ then $|f|$ has no max on $\Omega$

Alternatively, if $f$ is continuous on the closed bounded set $B$, and analytic on the interior of $B$, then the max of $|f(z)|$ occurs on boundary of $B$
- If $f(z)\neq 0$ then you can apply the max mod principle to $1 /f(z)$ to obtain the min mod principle

Taylor Series Theorem:
> If $f$ is analytic on domain $\Omega$, then, for some $z_{0}\in \Omega$
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
> If $f(a)=0$, $f$ is analytic, non-constant, $f=\sum a_{k}(z-a)^{k}$ then $\exists n\in \mathbb{N}$ such that
$$
f(z) = (z-a)^{n} \sum_{k=n+1}^{\infty} a_{k}(z-a)^{k-n}
$$
> Where the summation here when $z=a$ is never equal to zero. We call the $n$ the order of $z=a$
- The order of $z=a$ is the order of first non-zero derivatives at $z=a$

Theorem:
> Zeros of all non-zero analytic function are isolated
- This can be interpreted as: the zeroes for this function do not group up in arbitrarily small spaces

Theorem:
> If $f$ vanishes on an open disk $D$ or on a curve $\gamma$, then $f$ is identically 0 on any domain containing $D$ or $\gamma$

Theorem:
> Define two functions $f$ and $g$ such that $f$ is continuous on $\Omega_{1}\cup \gamma$ and analytic on $\Omega_{1}$, $g$ is continuous on $\Omega_{2}\cup \gamma$ and analytic on $\Omega_{2}$. If $f=g$ on $\gamma$ then:
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
> If $0\leq r<R\leq \infty$ and $u=\{ z : r<|z-z_{0}|<R \}$ and $f:u\to \mathbb{C}$ is analytic, then $f$ has a Laurent series
$$
f(z) = \sum_{k=0}^{\infty} a_{k}(z-z_{0})^{k}
$$
> Where:
$$
a_{k} = \frac{1}{2\pi i} \int _{\gamma} \frac{f(\omega)}{(\omega-z_{0})^{k+1}} \, d\omega
$$
> $\gamma$ is any closed curve $u$ circling $z_{0}$
