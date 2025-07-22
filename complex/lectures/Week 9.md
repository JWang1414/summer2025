### Evaluating Integrals
For integrals of the form:
$$
\int_{-\infty}^{\infty} \frac{N(x)}{D(x)} \, dx
$$
Where $D(x)\neq 0$ for $x \in \mathbb{R}$ and $D(x)$ is at least 2 degrees greater than the degree of $N(x)$, we consider the integral:
$$
\oint_{C} f(z) \, dz = \int_{-R}^{R} f(x) \, dx + \int _{C_{R}} f(z) \, dz
$$
$C$ is a contour which encloses all the singularities of $f(z)$, and $C_{R}$ is a large semicircle. Showing that $\lim_{ R \to \infty }\int _{C_{R}} f(z) \, dz=0$ the following integral can be evaluated with:
$$
\int_{-\infty}^{\infty} f(x) \, dx = 2\pi i \sum_{i=1}^{N} \text{Res}(f(z), z_{i})
$$
Further more, it is possible to prove as a theorem that:
> For some rational function $f(z)=N(z) /D(z)$ such that the degree of $D(z)$ exceeds the degree of $N(z)$ by at least two, then
$$
\lim_{ R \to \infty } \int C_{R} f(z) \, dz =0
$$
![[Pasted image 20250722111930.png]]

Jordan's Lemma:
> Suppose that on the circular arc $C_{R}$, we have $f(z)\to 0$ uniformly as $R\to \infty$. Then
$$
\lim_{ R \to \infty } \int _{C_{R}} e^{ ikz } f(z) \, dz =0
$$
> When $k>0$. 

For integrals of the form:
$$
\int_{-\infty}^{\infty} R(x) \sin x \, dx \qquad \int_{-\infty}^{\infty} R(x) \cos x \, dx
$$
Where $R$ is a rational function, real-valued on the real axis, we can use the Residue theorem on the function $f(z)=R(z)e^{ iz }$ and then use the imaginary of real part of the resulting value. Under this transformation we have:
$$
\cos t = \frac{1}{2} \left( z+\frac{1}{z} \right) \qquad \sin t = \frac{1}{2i} \left( z-\frac{1}{z} \right)
$$
![[Pasted image 20250722113015.png]]
Theorem:
> Suppose that on the contour $C_{\epsilon}$ depicted above we have $(z-z_{0})f(z)\to 0$ uniformly as $\epsilon\to 0$. Then
$$
\lim_{ \epsilon \to 0 } \int _{C_{\epsilon}}f(z) \, dz =0
$$
> Suppose $f(z)$ has a simple pole at $z=z_{0}$ with residue $\text{Res}(f(z);z_{0})=C_{-1}$. Then, for the contour $C_{\epsilon}$
$$
\lim_{ \epsilon \to 0 } \int _{C_{\epsilon}} f(z) \, dz = i \phi C_{-1}
$$

Generally speaking, when attempting to evaluate integrals on the real line, we are interested in drawing contours of integration like this:
![[Pasted image 20250722113403.png]]
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
Example:
$$
\int_{-\infty}^{\infty} \frac{x^{3} \sin x}{x^{4}+16} \, dx
$$
Define the new function:
$$
f(x) = \frac{z^{3} e^{ iz }}{z^{4}+16}
$$
Now, we would like to integrate this function over a semi-circle with radius $R$, as we have done before:
$$
\int _{\gamma_{R}} f(z) \, dz = \int _{\gamma_{1}} f(z) \, dz + \int _{\gamma_{2}} f(z) \, dz
$$
We can show that:
$$
\lim_{ R \to \infty } \int _{\gamma_{2}}f(z) \, dz =0
$$
Recall that this is the integral going around the semi-circle. Now, we can use the residuals to calculate the full integral. First, factor the denominator:
$$
\begin{align}
z^{4}+16 & = (z^{2}+4i)(z^{2}-4i) \\
 & = (z-2e^{ 3\pi i/4 })(z + e^{ 3\pi i/4 })(z-2e^{ \pi i/4 })(z + e^{ \pi i/4 })
\end{align}
$$
The pole that are in the upper-half plane are:
$$
r_{1}=z-2e^{ 3\pi i/4 } \qquad r_{3} = z- 2e^{ \pi i/4 }
$$
Calculate the residuals:
$$
\int _{\gamma_{R}} f(z) \, dz = 2\pi i \sum \text{Res}(f, z_{i}) = 2\pi i\left[ \text{Res}(f, r_{1}) + \text{Res}(f, r_{3}) \right] = \frac{\pi i}{e^{ \sqrt{ 2 } }} \cos \sqrt{ 2 }
$$
Afterwards, because we are computing the sine portion as opposed to the cosine portion, we take the imaginary part, so our final answer is:
$$
\int_{-\infty}^{\infty} \frac{x^{3}\sin x}{x^{4} + 16} \, dx = \frac{\pi i}{e^{ \sqrt{ 2 } }} \cos \sqrt{ 2 }
$$
---

Type 3:
$$
\int_{0}^{2\pi} r (\cos \theta, \sin\theta) \, d\theta
$$
Where $(\cos\theta, \sin\theta)$ is some rational function of cosines and sines.

Try using the parametrization $z=\gamma(t)=e^{ it }$. Then we have $\gamma'(t)=ie^{ it }=iz$.

Notice that:
$$
\cos t = \frac{1}{2} \left( z+\frac{1}{z} \right) \qquad \sin t = \frac{1}{2i} \left( z-\frac{1}{z} \right)
$$
Therefore we have:
$$
\int_{\gamma} r \left( \frac{1}{2}\left( z+\frac{1}{z} \right), \frac{1}{2i}\left( z-\frac{1}{z} \right) \right) \left( \frac{1}{iz} \right) \, dt
$$
And from here, we can complete the computation with residuals.

---
Example:
$$
\int_{0}^{\pi} \frac{1}{a + \cos\theta} \, d\theta
$$
Where $a>1$. Note that the bound of this function are not $[0, 2\pi]$, which means we will either need to use a different parametrization, or a different strategy to simplify it into the form we like. But since cosine is symmetric around $\pi$, we can claim that:
$$
\frac{1}{2} \int_{0}^{2\pi} \frac{1}{a+\cos\theta} \, d\theta
$$
Use the substitution defined from before:
$$
\frac{1}{2} \int _{|z|=1} \frac{1}{a+ \frac{1}{2} \left( z+\frac{1}{z} \right)}\left( \frac{1}{iz} \right) \, dz = \frac{1}{2i} \int _{|z|=1} \frac{1}{\frac{1}{2}z^{2} + az + \frac{1}{2}} \, dx
$$
Use the quadratic function to find the roots: $-a \pm \sqrt{ a^{2}-1 }$. Which are of order 1.

And now compute the residuals:
$$
\frac{1}{2i} \cdot 2\pi i \sum \text{Residuals} = \pi \sum \text{Residuals} = \pi \left( \frac{1}{z-r_{2}} \bigg|_{z=r_{1}} \right)
$$
Where $r_{2}=-a-\sqrt{ a^{2}-1 }$ and $r_{1}=-a+\sqrt{ a^{2}-1 }$ is inside the region $|z|=1$. Final answer:
$$
\frac{\pi}{r_{1}-r_{2}} = \frac{\pi}{2\sqrt{ a^{2}-1 }}
$$
---

Type 4: Multivalued functions
- There is no one way to compute these integrals

---
Example:
$$
\int_{0}^{\infty} \log \frac{\log x}{(1+x^{2})^{2}} \, dx
$$
Recall that for complex values, we must pick a branch of log, because it is a multivalued function. We will choose:
$$
f(z) = \frac{\log z}{(1+z^{2})^{2}} \qquad \text{arg}(z)\in\left( -\frac{\pi}{2}, \frac{3\pi}{2} \right)
$$
Take this integral over two concentric semi-circles, one of radius $R$, and the other of radius $\epsilon$. The one of radius $\epsilon$ exists because the logarithm isn't defined at $z=0$, so we need to try and exclude it. You will find that:
$$
\lim_{ R \to \infty } \left| \int _{\gamma_{R}} f(z) \, dz  \right| = \lim_{ R \to \infty } \left| \int _{\gamma_{\epsilon}} f(z) \, dz  \right|  =0
$$
Compute the residuals:
$$
2\pi i \sum \text{Residuals} = \int _{\gamma_{1}} f(z) \, dz + \int _{\gamma_{2}} f(z) \, dz
$$
Which you can prove (through a series of convoluted steps I don't really understand) is:
$$
2 \int_{\epsilon}^{R} \frac{\log t}{(1+t^{2})^{2}} \, dt + \pi i \int_{\epsilon}^{R} \frac{1}{1+t^{2}} \, dt
$$
The first integral has just one relevant singularity at $z=i$ of order 2
$$
\text{Res}(f, i) = \frac{d}{dz} \bigg|_{z=i} \left( \frac{\log z}{(z+i)^{2}} \right) = \frac{2i+\pi}{8}
$$
Therefore:
$$
\int_{0}^{\infty} \frac{\log t}{(1+t^{2})^{2}} \, dt = \mathrm{Re}\left\{ 2\pi i \text{Res}(f, i) \right\} = -\frac{\pi}{4}
$$
---
Example:
$$
\int_{0}^{\infty} \frac{x^{1/3}}{x^{2}+4x+8} \, dx
$$
We must pick a branch of $x^{1/3}$. Define the new function:
$$
f(z) = \frac{z^{1/3}}{z^{2} + 4z+8}, \qquad \text{arg}(z^{1/3}) \in \left(0 , \frac{2\pi}{3} \right)
$$
Defined on $\mathbb{C}\setminus \mathbb{R}^{\geq 0}$. By this point we should know that, along the two concentric circles that have been defined, the integral will be 0.

Choose parametrization:
$$
\begin{align}
\gamma_{1}(t) & = t e^{ i\delta } \\
\gamma_{2}(t) & = te^{ i(2\pi-\delta) }
\end{align}
$$
Where, in both cases, $t\in(\epsilon, R)$. 

...

$$
(1 - e^{ 2\pi i/3 }) \int_{0}^{\infty} f(t) \, dt = 2\pi i \sum \text{Residuals}
$$
