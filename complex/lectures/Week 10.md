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
Along the real axis $[0, R]$, $z=x$ where $x \in \mathbb{R}$. $f(x)$ is a real valued function, and so $\text{arg}(f(x))=0$

Now check over the curve. Parametric $z=R e^{ it }$, $t\in\left[ 0, \frac{\pi}{2} \right]$
$$
f(z) = (R e^{ it })^{3} - 2 (R e^{ it })^{2} + 4 = R^{3} e^{ 3it } \left( 1 - \frac{2}{R e^{ it }} + \frac{4}{R^{3} e^{ 3it }} \right)
$$
See how the argument changes in this domain by evaluating the function.
 
 When $t=0$
$$
f(z) = R^{3} \left( 1-\frac{2}{R} + \frac{4}{R^{3}} \right)
$$
This is a real valued function, and so the argument is 0

When $t=\frac{\pi}{2}$
$$
f(z) = R^{3} e^{ 3\pi i/2 } \left(  1-\frac{2}{R e^{ \pi i/2 }} + \frac{4}{R^{3} e^{ 3\pi i/2 }}\right)
$$
Take the limit as $R\to \infty$, and the portion in brackets collapses to 1. The argument of the function is therefore equal to:
$$
\text{arg}(R^{3} e^{ 3\pi i/2 }) = \frac{3\pi}{2}
$$
Therefore, the change in argument over this curve is $3\pi /2$

Along the imaginary axis, define $z=iy$ and therefore:
$$
f(z) = -iy^{3} + 2y^{2} + 4
$$
Recall that we can determine the argument by taking the $\arctan$ of the imaginary and real portions of the function.
$$
\text{arg}(f) = \arctan\left( -\frac{y^{3}}{2y^{2}+4} \right)
$$
To determine the change in argument along the imaginary axis, take the difference between $y=0$ and $y\to \infty$
$$
y\to \infty \Rightarrow -\frac{y^{3}}{2y^{2}+4} \to -\infty \qquad y=0 \Rightarrow -\frac{y^{3}}{2y^{2}+4} =0
$$
And therefore the change in argument is:
$$
\arctan(0) - \arctan(-\infty) = 0  + \frac{\pi}{2} = \frac{\pi}{2}
$$
By the argument principle, the number of zeroes is:
$$
\frac{1}{2\pi} \left[ \text{arg}(f) \right] _{\gamma} = \frac{1}{2\pi} \left[ \frac{3\pi}{2} + \frac{\pi}{2} \right]  = 1
$$
And there is one zero in the first quadrant

---

Theorem 30: Rouche's Theorem
> If $f$, $g$ are analytic functions on and inside a simple closed contour $\gamma$, and $|f|>|g|$ on $\gamma$, then $f$ and $f+g$ have the same number of zeroes in $\gamma$

---
Example:
Prove the fundamental theorem of algebra with this theorem: Define $P(z)$ to be a degree $n$ polynomial. Then $P(z)$ has $n$ zeroes, counted with multiplicity.

Model $p(z)$ as:
$$
a_{n}z^{n} + \dots + a_{1}z + a_{0}
$$
Let $f(z)=a_{n}z^{n}$ and $g(z)=p(z)-a_{n}z^{n}$

WTS on $\gamma_{R}$ for large $R$ $,|f|>|g|$

Our goal is to use Rouche's theorem on $f$ and $f+g=p(z)$ to show that they have the same number of zeroes, proving that $p(z)$ has $n$ zeroes.

Look at...
$$
\left| \frac{g(z)}{f(z)} \right|  = \left| \frac{a_{n-1}z^{n-1} + \dots + a_{1}z + a_{0}}{a_{n} z^{n}} \right| \leq \frac{|a_{n-1}|}{|a_{n}|R} + \frac{|a_{n-2}|}{|a_{n}R^{2}} + \dots + \frac{|a_{0}|}{R^{n}}
$$
Where we have used the triangle inequality, and then substituted $z=R$. Moreover, it is clear that as $R\to \infty$, this function converges to 0. Hence we conclude:
$$
\left| \frac{g}{f} \right| < 1 \Rightarrow |g| < |f|
$$
And the Rouche theorem can be used to finish the rest of the proof.

---
Example:
Show that $e^{ z } = 4z+1$ has one solution on the unit disk

We want to show that $h(z)=e^{ z }-4z-1$ has one zero in the unit disk. We would like to do this by writing $h=f+g$ such that $|f|>|g|$ and $f$ has one zero on the unit disk

Try:
$$
\begin{align}
f(z) & = -4z \\
g(z) & = e^{ z }-1
\end{align}
$$
On the unit disk we have:
$$
\begin{align}
|g(z)| & = |e^{ z }| + |-1| = e^{ |z| }+1 \\
 & \leq e+1 \approx 2.7+1 \\
 & < 4 = |4z| \\
 & = |f(z)|
\end{align}
$$
And therefore, since $f(z)$ has just one zero in the unit disk, we $h$ also has one zero in the unit disk.

---
Example:
Show that $p(z)=z^{8}-4z^{3}+10$ has all its roots in the annulus $1\leq z\leq 2$

Our strategy will be to:
1. Show all roots are $|z|<2$
2. No roots of $p(z)$ are in $|z|<1$

WTS Part 1.

Use $f(z)=z^{8}$ and $f(z)=-4z^{3}+10$

On $|z|=2$
$$
\begin{align}
|g(z)|  & \leq |-4z^{3}| + |10| = 4(2)^{3} + 10 = 42 \\
|f(z)| & = |z|^{8} = 2^{8} > 42
\end{align}
$$
And therefore $|f|>|g|$ on $|z|=2$. Furthermore, since $f$ has 8 roots in $|z|\leq 2$, $p(z)=f+g$ must also have 8 roots in $|z|\leq 2$. We conclude that all roots of $p(z)$ are within $|z|\leq 2$ because $p(z)$ is a polynomial of order 8.

WTS Part 2
Use $f(z)=10$ and $g(z)=z^{8}-4z^{3}$

On $|z|=1$ we have:
$$
\begin{align}
|g(z)| & = |z|^{8} + 4|z|^{3} = 1+4(1) = 5 \\
|f(z)| & = 10
\end{align}
$$
And since $f(z)$ has no roots in $|z|<1$ $f+g=p(z)$ also has no roots within this region.

Both parts have been shown, and we can conclude all zeroes lie within the aforementioned annuli

---

Theorem 31: Open mapping theorem
> If $\Omega$ is open and connected and $h:\Omega\to \mathbb{C}$ is analytic and non-constant then the image $h(\Omega)$ is also open and connected.

