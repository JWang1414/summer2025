### Question 1
Determine the angle with the real axis.
$$
\tan\theta = \frac{\text{Opposite}}{\text{Adjacent}} = \frac{2}{1} \implies \theta = \arctan(2)
$$
Calculate the magnitude.
$$
R = \sqrt{ 1^{2}+2^{2} } = \sqrt{ 5 }
$$
Substitute back into the representation for $z$.
$$
z = \left[ \sqrt{ 5 }e^{ -i\arctan(2) } \right] ^{3} = 5^{3/2} e^{ -3i\arctan(2) }
$$
### Question 2
Split up the exponent, and simplify the imaginary exponent with the exponential.
$$
(1-i)^{1-i} = (1-i)(1-i)^{-i} = (1-i)e^{ \ln((1-i)^{-i}) }
$$
Apply logarithm laws.
$$
e^{ \ln((1-i)^{-i}) } = e^{ -i \ln(1-i) }
$$
Evaluate the logarithm.
$$
\ln(1-i) = \ln|1-i| + i \arg(1-i) = \ln|1-i| + i \left( -\frac{\pi}{4} + 2\pi k \right)
$$
Evaluate the full exponential term.
$$
-i\ln(1-i) = -i \left[ \ln|1-i| + i\left( 2\pi k -\frac{\pi}{4} \right) \right] = 2\pi k - \frac{\pi}{4} -i \ln \left| 1-i \right|
$$
Substitute back into the original statement.
$$
(1-i)\exp \left\{ 2\pi k - \frac{\pi}{4} -i \ln \sqrt{ 2 } \right\}
$$
### Question 3
Recall the Cauchy-Riemann equations:
$$
u_{x} = v_{y} \qquad v_{x} = -u_{y}
$$
For some function $f(z) = u(z)+iv(z)$. First, split the logarithm into the real and imaginary parts:
$$
\log z = \log|z| + i \arg z
$$
Now, define $z=x\pm iy$ and therefore we have:
$$
\log z = \log \sqrt{ x^{2}+y^{2} } + i \arctan\left( \frac{y}{x} \right)
$$
We obtain the two functions:
$$
u(x, y) = \frac{1}{2} \log(x^{2}+y^{2}) \qquad v(x, y) = \arctan\left( \frac{y}{x} \right)
$$
Compute the derivatives of $v$.
$$
\begin{align}
v_{x} & = - \frac{y}{x^{2}+y^{2}} \\
v_{y} & = \frac{x}{x^{2}+y^{2}}
\end{align}
$$
Therefore, from the Cauchy-Riemann equations:
$$
u_{x} = v_{y} \implies \frac{1}{2} \frac{d}{dx} \log(x^{2}+y^{2}) = \frac{x}{x^{2}+y^{2}}
$$
$$
u_{y} = -v_{x} \implies \frac{1}{2} \frac{d}{dy} \log(x^{2}+y^{2}) = \frac{y}{x^{2}+y^{2}}
$$
Furthermore, we know that:
$$
\frac{d}{dx} (x^{2}+y^{2}) = 2x \qquad \frac{d}{dy} (x^{2}+y^{2}) = 2y
$$
Hence, by observation we have:
$$
\frac{d}{dx} \log(x^{2}+y^{2}) = \frac{1}{x^{2}+y^{2}} \frac{d}{dx} (x^{2}+y^{2})
$$
$$
\frac{d}{dy} \log(x^{2}+y^{2}) = \frac{1}{x^{2}+y^{2}} \frac{d}{dy} (x^{2}+y^{2})
$$
Which is simply an application of the chain rule. I conclude, therefore, that:
$$
\frac{d}{d(x^{2}+y^{2})} \log(x^{2}+y^{2}) = \frac{1}{x^{2}+y^{2}} \implies \frac{d}{dz} \log(z) = \frac{1}{z}
$$
Now, we have:
$$
\frac{d}{dz} z^{s} = \frac{d}{dz} e^{ s \log z } = e^{ s\log z } \frac{d}{dz}(s \log z) = e^{ s \log z } (s) \frac{d}{dz} \log z = se^{ s\log z } \left( \frac{1}{z} \right)
$$
Which can easily be transformed back into:
$$
\frac{d}{dz} z^{s} = s (z^{s})\left( \frac{1}{z} \right) = s \frac{z^{s}}{z}
$$
### Question 4
Recall, Cauchy's integral formula:
$$
f(z) = \frac{1}{2\pi i} \int_{\gamma} \frac{f(\xi)}{\xi-z} \, d\xi
$$
Which is valid for some analytic function $f$ on a domain $D$, where $\gamma$ is a piecewise smooth, positively oriented simple closed curve in $D$ whose inside $\Omega$ also lies in $D$.

Note the the defined domain, the circle of radius 3 centred at the origin, is valid for this theorem to be applied. Furthermore, the function:
$$
f(z) = \frac{\sin z + e^{ z }}{(z-2\pi)}
$$
is analytic on the defined domain. The full integral can be re-written:
$$
\int _{|\xi|=3} \frac{\sin \xi + e^{ \xi }}{(\xi-1)(\xi-2\pi)} \, d\xi
$$
Where I have, for simplicity, used the substitution $z=\xi$. Now, it can easily be seen that this integral is equal to:
$$
\int _{|\xi|=3} \frac{f(\xi)}{(\xi-1)} \, d\xi = 2\pi i f(1) = 2\pi i \left[ \frac{\sin(1) + e}{1-2\pi} \right]
$$
### Question 5
The Taylor series for $\sin z$ is:
$$
\sin z = \sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k+1)!} z^{2k+1}
$$
And so,
$$
\frac{1}{\sin z} = \sum_{k=0}^{\infty} \frac{(2k+1)!}{(-1)^{k}} z^{-(2k+1)}
$$
As a Laurent series, the -1st term would be the one with $-(2k+1)=-1$, which is when $k=0$. So, this coefficient is:
$$
\frac{(2(0)+1)!}{(-1)^{0}} = \frac{1!}{1} = 1
$$
This is the residue of this function, for the root at $z=0$. According to the residue theorem, I conclude that:
$$
\int _{\gamma} \frac{1}{\sin z} \, dz = 2\pi i (1) = 2\pi i
$$
### Question 6
The Taylor series of $e^{ z }$ is:
$$
e^{ z } = \sum_{k=0}^{\infty} \frac{z^{k}}{k!}
$$
And so in this case we have:
$$
e^{ 1/z } = \sum_{k=0}^{\infty} \frac{(1 /z)^{k}}{k!} = \sum_{k=0}^{\infty} \frac{z^{-k}}{k!}
$$
Therefore,
$$
z^{100} e^{ 1/z } = \sum_{k=0}^{\infty} \frac{z^{-k}z^{100}}{k!} = \sum_{k=0}^{\infty} \frac{z^{100-k}}{k!}
$$
Use index shift:
$$
\sum_{k=-\infty}^{100} \frac{z^{k}}{(100-k)!}
$$
The coefficient for the -1st term is:
$$
\frac{1}{(100-1)!} = \frac{1}{99!}
$$
Recall the residue theorem:
$$
\int _{\gamma} f(z) \, dz = 2\pi i \sum_{z_{k} \text{ within }\gamma} \text{Res}(f;z_{k})
$$
So the integral is equal to:
$$
\int _{\gamma} z^{100} e^{ 1/z } \, dz = 2\pi i \frac{1}{99!} = \frac{2\pi i}{99!}
$$
### Question 7
Factor the function:
$$
\frac{x^{2}}{(x^{2}+1)^{2}(x^{2}+2x+2)} = \frac{x^{2}}{[(x+i)(x-i)]^{2} (x+(1-i))(x+(1+i))}
$$
Where we have two poles of order 2, and two poles of order 1. If I define the region $\gamma$ where gamma is the upper-half plane, then I can take the complex integral using the residues. The poles of interest are $z=i$ and $z=-1+i$.

I will compute the residues using the theorem:
$$
\text{Res}(f;z_{0}) = c_{m-1} = \frac{H^{(m-1)}(z_{0})}{(m-1)!}
$$
Where $H^{(m-1)}$ is the version of the function continuous at $z_{0}$, and $m$ is the order of the zero. For the zero of order 1 we have :
$$
\begin{align}
\mathrm{Re}s(f;-1+i) & = \frac{1}{(1-1)!} \left[ \frac{z_{0}^{2}}{(z_{0}+i)^{2}(z_{0}-i)^{2}(z_{0}+1+i)} \right] \\
 & = \frac{(-1+i)^{2}}{(-1+i+i)^{2}(-1+i-i)^{2}(-1+i+1+i)} \\
 & = \frac{1}{25} (3-4i)
\end{align}
$$
For the zero of order 2 we have:
$$
\text{Res}(f;i) = \frac{1}{(2-1)!} \left[ \frac{d}{dz} \frac{z^{2}}{(z+i)^{2}(z+1-i)(z+1+i)} \right] _{z=i}
$$
This derivative is equal to:
$$
\implies - \frac{2z(z^{3}+z^{2}-iz-2i)}{(z+i)^{3} (z^{2}+2z+2)^{2}}
$$
Evaluated at $z=i$ we have:
$$
\text{Res}(f;i) = \frac{3}{100} (-4+3i)
$$
From residue theorem we have:
$$
\int _{\gamma} \frac{z^{2}}{(z^{2}+1)^{2}(z^{2}+2z+2)} \, dz = 2\pi i \left[ \frac{1}{25}(3-4i) + \frac{3}{100}(-4+3i) \right] = \frac{7\pi}{50}
$$
Which is the answer to the original integral.
### Question 8
Use the parametrization $\gamma(t)=e^{ it }=z$ with $\gamma'(t)=ie^{ it }=iz$. Under this we have:
$$
\cos t = \frac{1}{2} \left( z+\frac{1}{z} \right) \qquad \sin t = \frac{1}{2i} \left( z-\frac{1}{z} \right)
$$
Furthermore, the bounds of the integral $[0, 2\pi]$ are transformed to the unit circle centred at the origin. The full integral has been transformed to:
$$
\int_{0}^{2\pi} \frac{1}{a+b \sin t} \, dt = \int _{\gamma} \frac{1}{a+b\left[ \frac{1}{2i}\left( z-\frac{1}{z} \right) \right] } \left( \frac{1}{iz} \right) \, dz
$$
Simplify this function:
$$
\frac{2}{bz^{2} + 2iaz -b}
$$
Which has the roots:
$$
z = \frac{-2ia \pm \sqrt{ 4b^{2}-4a^{2} }}{2b} = \frac{-ia \pm \sqrt{ b^{2}-a^{2} }}{b} = -\frac{ia}{b} \pm \frac{\sqrt{ b^{2}-a^{2} }}{b}
$$
Check which one of these roots lies within the unit circle:
$$
\sqrt{ \left( \frac{a}{b} \right)^{2} + \left( \frac{\sqrt{ b^{2}-a^{2} }}{b} \right)^{2} } = \sqrt{ \left( \frac{a^{2}}{b^{2}} \right) + \frac{b^{2}-a^{2}}{b^{2}} } <1 \implies \frac{a^{2}+b^{2}-a^{2}}{b^{2}} <1 \implies 1<1
$$
Which implies that both roots lie upon the unit circle. Define the variables:
$$
p= \frac{-ia + \sqrt{ b^{2}-a^{2} }}{b} \qquad q = \frac{-ia - \sqrt{ b^{2}-a^{2} }}{b}
$$
And so the function can be re-written:
$$
\frac{2}{(z-p)(z-q)}
$$
With two roots of order 1. I intend to use the residual theorem to compute this integral. The two residuals that lie within the domain are $p$ and $q$.
$$
\text{Res}(f;p) = \frac{2}{z_{0}-q} = \frac{2}{p-q} = 2 \left( \frac{b}{2\sqrt{ b^{2}-a^{2} }} \right) = \frac{b}{\sqrt{ b^{2}-a^{2} }}
$$
$$
\text{Res}(f;q) = \frac{2}{z_{0}-p} = \frac{2}{q-p} = 2 \left( -\frac{b}{2\sqrt{ b^{2}-a^{2} }} \right) = -\frac{b}{\sqrt{ b^{2}-a^{2} }}
$$
According to the residual theorem, the integral is therefore:
$$
\int_{0}^{2\pi} \frac{1}{a+b\sin t} \, dt = \int _{\gamma} \frac{2}{bz^{2}+2iaz-b} \, dz = 2\pi i \left[ \frac{b}{\sqrt{ b^{2}-a^{2} }} - \frac{b}{\sqrt{ b^{2}-a^{2} }} \right] =0
$$
### Question 9
Define the new function, and the new integral:
$$
\int _{\gamma} \frac{e^{ iz }}{(z^{2}+1)^{2}((z-3)^{2}+1)} \, dz
$$
Factor the polynomial in the denominator.
$$
(z^{2}+1)^{2} ((z-3)^{2}+1) = (z+i)^{2}(z-i)^{2} (z-3-i)(z-3+i)
$$
Which has two roots in the upper-half plane. $z=i$ and $z=3+i$. One of order 2, and the other of order 1. Compute residuals:
$$
\text{Res}(f;i) = \frac{d}{dz} \frac{e^{ iz }}{(z+i)^{2}((z-3)^{2}+1)} \bigg|_{z=i} = \frac{51-148i}{3042e}
$$
$$
\text{Res}(f;3+i) = \frac{e^{ iz }}{(z^{2}+1)^{2}(z-3+i)} \bigg|_{z=3+i}  = -\left( \frac{2}{507} + \frac{5i}{3042} \right)e^{ 3i-1 }
$$
By residue theorem:
$$
\int _{\gamma} \frac{e^{ iz }}{(z^{2}+1)^{2} ((z-3)^{2}+1)} \, dz = 2\pi i \left[ \frac{51-148i}{3042e} - \left( \frac{2}{507} + \frac{5i}{3042} \right)e^{ 3i-1 } \right]
$$
### Question 10
---
a.
