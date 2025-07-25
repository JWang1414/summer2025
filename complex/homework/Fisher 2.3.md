Questions 1-12
### Questions 1-4
---
1.
The function within the integral is analytic within the domain $|z|\leq 1$. This domain contains the curve $|z|=1$ the integral is being taken over. Therefore, by Cauchy's theorem, the integral is 0
$$
\int _{|z|=1} \frac{z}{(z-2)^{2}} \, dz =0
$$
---
2.
Recall Cauchy's Formula:
$$
f(a) = \frac{1}{2\pi i} \int _{\gamma} \frac{f(z)}{z-a} \, dz
$$
This integral is being taken over the circle $|z|=2$. $z=0$ lies within the circle, but $z=3$ does not. I define the analytic function:
$$
f(z) = \frac{e^{ z }}{z-3}
$$
Simplifying the target integral into:
$$
\int _{\gamma} \frac{e^{ z }}{z(z-3)} \, dz = \int _{\gamma} \frac{f(z)}{z-0} \, dz = 2\pi i f(0)
$$
Where I have applied Cauchy's integral formula during the last step.
$$
2\pi i f(0) = 2\pi i \frac{e^{ 0 }}{0-3} = 2\pi i \left( \frac{1}{-3} \right) = -\frac{2}{3} \pi i
$$
---
3.
Factor.
$$
\int _{\gamma} \frac{z^{2}}{(2-z)(2+z)} \, dz
$$
The pole located at $z=-2$ is within the circle $|z+1|=2$. Define the new equation:
$$
f(z) = \frac{z^{2}}{2-z}
$$
This function is analytic within the circle. Substituting into the integral:
$$
\int _{\gamma} \frac{f(z)}{2+z} \, dz = \int _{\gamma} \frac{f(z)}{z-(-2)} \, dz = 2\pi i f(-2)
$$
Therefore,
$$
\int _{|z+1|=2} \frac{z^{2}}{4-z^{2}} \, dz = 2\pi i \left[ \frac{(-2)^{2}}{2-(-2)} \right] = 2\pi i
$$
---
4.
This has one pole within the circle $|z|=1$. Define the function:
$$
f(z) = \sin z
$$
This integral is now:
$$
\int _{\gamma} \frac{f(z)}{z-0} \, dz = 2\pi i f(0) = 2\pi i \sin 0 =0
$$
### Questions 5-8
---
5.
Using the substitution $z=e^{ i\theta }$ I obtain:
$$
\begin{align}
\cos \theta & = \frac{1}{2} \left( z+\frac{1}{z} \right) \\
d\theta & =\frac{1}{i} \frac{dz}{z}
\end{align}
$$
Apply this substitution to the integral:
$$
\int_{0}^{2\pi} \frac{1}{2+\cos \theta} \, d\theta = \int _{\gamma} \frac{1}{2+\left( \frac{1}{2}\left( z+\frac{1}{z} \right) \right)}\left( \frac{1}{iz} \right) \, dz =-2i \int_{\gamma} \frac{1}{z^{2}+4z+1} \, dz
$$
From the quadratic formula, the roots of this function are $-2\pm \sqrt{ 3 }$. The root $-2+\sqrt{ 3 }$ is within the circle $|z|=1$. Define $p=-2+\sqrt{ 3 }$ and $q=-2-\sqrt{ 3 }$, and write out the integral as:
$$
\int _{\gamma} \frac{1}{(z-p)(z-q)} \, dz
$$
Define the new function $f(z)$, which is analytic on the domain:
$$
f(z) = \frac{1}{z-q}
$$
Therefore, from Cauchy's formula:
$$
\int _{\gamma} \frac{1}{(z-p)(z-q)} \, dz = \int _{\gamma} \frac{f(z)}{z-p} \, dz = 2\pi i f(p) = 2\pi i \frac{1}{p-q}
$$
Substituting this back into the original equation:
$$
\int_{0}^{2\pi} \frac{1}{2+\cos \theta} \, d\theta = -2i \int _{\gamma} \frac{1}{z^{2}+4z+1} \, dz = -2i \left( 2\pi i \frac{1}{p-q} \right) = \frac{2\sqrt{ 3 }}{3}\pi
$$
---
7.
Use the substitution $z=e^{ i\theta }$
$$
a+b\cos \theta = a+b \left( \frac{1}{2}\left( z+\frac{1}{z} \right) \right) = \frac{2az+bz^{2}+b}{2z}
$$
And therefore this integral is:
$$
\int_{0}^{2\pi} \frac{1}{a+b\cos \theta} \, d\theta = \int _{\gamma} \frac{2z}{2az+bz^{2}+b} \frac{1}{iz} \, dz = -2i \int _{\gamma} \frac{1}{2az+bz^{2}+b} \, dz
$$
Which has roots at:
$$
z = \frac{-2a\pm \sqrt{ 4a^{2}-4b^{2} }}{2b} = \frac{-a \pm \sqrt{ a^{2}-b^{2} }}{b} = -\frac{a}{b} \pm \frac{\sqrt{ a^{2}-b^{2} }}{b}
$$
Check if one of the roots lies within $|z|=1$
$$
-\frac{a}{b} + \frac{\sqrt{ a^{2}-b^{2} }}{b} \leq 1 \implies -a + \sqrt{ a^{2}-b^{2} } \leq b \implies \sqrt{ a^{2}-b^{2} } \leq b+a
$$
$$
a^{2}-b^{2} \leq a^{2}+b^{2}+2ab \implies 0\leq 2b^{2} + 2ab
$$
Which is true and therefore this root lies within the circle.
$$
-\frac{a}{b} - \frac{\sqrt{ a^{2}-b^{2} }}{b} \leq 1 \implies -\sqrt{ a^{2}-b^{2} } \leq b+a \implies \sqrt{ a^{2}-b^{2} } \geq -b-a
$$
$$
a^{2}-b^{2} \geq a^{2}+2ab+b^{2} \implies 0 \geq 2b^{2} + 2ab
$$
Which is false and therefore this root does not lie in the circle. Define two new variables:
$$
p = -\frac{a}{b} + \frac{\sqrt{ a^{2}-b^{2} }}{b} \qquad q= -\frac{a}{b} - \frac{\sqrt{ a^{2}-b^{2} }}{b}
$$
Which will be used to represent the two roots of the function. I will now use Cauchy's integral formula to evaluate the integral:
$$
\int _{\gamma} \frac{1}{2az+bz^{2}+b} \, dz = \int _{\gamma} \frac{1}{(z-p)(z-q)} \, dz
$$
Only the root $p$ lies within the domain. Define the new function:
$$
f(z) = \frac{1}{z-q}
$$
And therefore:
$$
\int _{\gamma} \frac{1}{(z-p)(z-q)} \, dz = \int _{\gamma} \frac{f(z)}{z-p} \, dz = 2\pi i f(p) = 2\pi i \left( \frac{1}{p-q} \right)
$$
The full integral is therefore:
$$
\int_{0}^{2\pi} \frac{1}{a+b\cos \theta} \, d\theta = -2i \int _{\gamma} \frac{1}{2az+bz^{2}+b} \, dz = -2i(2\pi i)\left( \frac{1}{p-q} \right) = \frac{2\pi b}{\sqrt{ a^{2}-b^{2} }}
$$
### Questions 9-12
- These questions are all based on the theorem that, regardless of path, the line integral will always be the same, so long as the function is analytic along any possible defined line
---
9.
Define the new function $F(z)$ such that $F'(z)=f(z)$ where $f(z)$ is the integrand.
$$
F(z) = -\frac{1}{z} \implies F'(z) = \frac{1}{z^{2}} = f(z)
$$
Therefore,
$$
\begin{align}
\int _{\gamma} \frac{1}{z^{2}} \, dz  & = \int _{\gamma} f(z) \, dz  \\
 & = \int _{\gamma} F'(z) \, dz  \\
 & = F(\text{endpoint}) - F(\text{initial point}) \\
 & = F(1+i) - F(1-i)
\end{align}
$$
Evaluate,
$$
= -\frac{1}{1+i} + \frac{1}{1-i} = i
$$
---
10.
Define the new function $F(z)$
$$
F(z) = \frac{z^{2}}{2} + \log z \implies F'(z) = z + \frac{1}{z} = f(z)
$$
Therefore the integral is:
$$
\begin{align}
\int_{\gamma} \left( z+\frac{1}{z} \right) & = F(6+2i) - F(-4+i) \\
 & = \frac{(6+2i)^{2}}{2} + \log(6+2i) - \left[ \frac{(-4+i)^{2}}{2} + \log(-4+i) \right]  \\
 & = \frac{17}{2} + 16i - \log(-4+i) + \log(6+2i)
\end{align}
$$
---
11.
You can try the parametrization $\gamma(t)=-e^{ -it }$ and then integrate it from $t\in[0, \pi]$, but that's significantly harder, and yields the same result.

Define,
$$
F(z) = e^{ z } \implies F'(z) = e^{ z } = f(z)
$$
Therefore,
$$
\begin{align}
\int _{\gamma} e^{ z } \, dz & = \int _{\gamma} F'(z) \, dz  \\
 & = F(\text{endpoint}) - F(\text{initial point}) \\
 & = e^{ 1 } - e^{ -1 } \\
 & = e-\frac{1}{e}
\end{align}
$$
---
12.
Define,
$$
F(z) = -\cos z \implies F'(z) = \sin z
$$
Therefore,
$$
\begin{align}
\int _{\gamma} \sin z \, dz & = \int _{\gamma} F'(z) \, dz   \\
 & = F(\text{endpoint}) - F(\text{initial point}) \\
 & = F(\pi) - F(i) \\
 & = -\cos \pi + \cos i \\
 & = \frac{(1+e)^{2}}{2e}
\end{align}
$$
---
