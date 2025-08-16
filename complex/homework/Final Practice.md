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
Taking the imaginary part, I conclude that the value of the original integral is:
$$
\int_{-\infty}^{\infty} \frac{\sin x}{(x^{2}+1)^{2}((x-3)^{2}+1)} \, dx = 2\pi \left( \frac{17}{1014e} - \frac{2 \cos(3)}{507e} + \frac{5 \sin(3)}{3042e} \right)
$$
### Question 10
---
a.
The singularities are located where $\cos z=0$ and $\sin ^{2}(3z)=0$. These are:
$$
\cos z=0 \Rightarrow z = \left( n+\frac{1}{2} \right)\pi
$$
Where $n\in \mathbb{Z}$.
$$
\sin ^{2}(3z) =0 \Rightarrow \sin(3z)=0 \Rightarrow 3z = n\pi \Rightarrow z = \frac{n}{3}\pi
$$
Where $n\in \mathbb{Z}$. Notice that the singularities from the cosine and sine functions, in this case, never overlap. Therefore, this function has a pole at all $n\pi /3$.

The Taylor series of $\sin z$ is:
$$
\sin z = \sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k+1)!}z^{2k+1} = x - \frac{x^{3}}{6} + \frac{x^{5}}{120} + \dots
$$
Which will be non-zero after one derivative. Implying that the pole for $1 /\sin z$ is of order 1. Therefore, I conclude that the pole from $1 /\sin ^{2}(3z)$ has order 2.

---
b.
This function is similar to the function
$$
e^{ 1/z }
$$
Which has an essential singularity when $z=0$. I conclude that there is an essential singularity when $\sin z=0$
$$
\sin z=0 \implies z=n\pi
$$
Where $n\in \mathbb{Z}$

---
c.
Find the roots of the numerator and denominator:
$$
e^{ iz }-1 =0 \Rightarrow e^{ iz } = \cos z + i \sin z =1 \Rightarrow \cos z =1 \Rightarrow z=2\pi k
$$
Where $k\in \mathbb{Z}$.
$$
\sin(4z) = 0 \Rightarrow 4z = n\pi \Rightarrow z = \frac{n}{4} \pi
$$
Where $n\in \mathbb{Z}$. Both the numerator and denominator are 0 at intervals of $2\pi k$. According to L'Hopital's rule:
$$
\lim_{ z \to 2\pi k } \frac{e^{ iz }-1}{\sin(4z)} = \lim_{ z \to 2\pi k } \frac{ie^{ iz }}{4 \cos(4z)} = \frac{i}{4}
$$
I conclude that there is a removable singularity at every interval $2\pi k$. All other poles at $n\pi /4$ have order 1.

I know they have order 1 because after one derivative $\sin z$ is $\cos z$ which is not zero at that point. Same argument as (a).

---
### Question 11
The Maximum-Modulus Principle:
> If $f$ is a nonconstant analytic function on a domain $D$, then $\mathrm{Re}\{ f \}$ has no local maximum and no local minima on $D$

Define a new function $g=1 /f$. Then, on the set $U$ we have:
$$
0 > \left| g(z_{0}) \right|  \geq \left| g(z) \right|
$$
Since $|f(z)|>0$ for all points in $U$, I know that $g(z)$ is bounded on this domain. By the maximum modulus principle, $g(z)$ must also attain its maxima on the boundary of the open set $U$. Furthermore, it also claims that $g$ has no local maxima within $U$.

That is, the Maximum-modulus principle implies that, on the domain $U$, if it has some local maxima at $z_{0}$, then $g$ must be a constant function. Therefore, $f=1 /g$ is also a constant function.

---
### Question 12
Theorem 30: Rouche's Theorem
> If $f$, $g$ are analytic functions on and inside a simple closed contour $\gamma$, and $|f|>|g|$ on $\gamma$, then $f$ and $f+g$ have the same number of zeroes in $\gamma$

First, find the number of zeroes in the circle with radius 2.

Choose the functions:
$$
f(z) = z^{7} \qquad g(z) = -5z^{3}+12
$$
On the circle $|z|=2$ we have:
$$
\begin{align}
|f(z)|  & = |2^{7}| \\
|g(z)|  & = |-5(2)^{3}+12| = |-28|=28
\end{align}
$$
In this case, $2^{7}>28$ and so $|f|>|g|$. Therefore, $f$ and $f+g$ have the same number of zeroes in $\gamma$. This implies that the original function has 7 zeroes within this region.

Second, find the number of zeroes with the circle of radius 1.

Choose the functions:
$$
f(z)=12 \qquad g(z) = z^{7} - 5z^{3}
$$
On the circle $|z|=1$ we have:
$$
\begin{align}
|f(z)|  & = 12 \\
|g(z)|  & = |z^{7}-5z^{3}| = |1-5(1)| = |1-5| = |-4| = 4
\end{align}
$$
And therefore we have $|f|>|g|$. And so I conclude this function has no zeroes within this region.

I conclude that this function has 7 zeroes in the annulus $1<|z|<2$
### Question 13
Argument Principle:
> Suppose $h$ is analytic on a domain $D$ except for isolated poles. Let $\gamma$ be a piecewise smooth positively oriented simple closed curve in $D$ whose inside lies in $D$ and which does not pass through any zeroes of poles of $h$. Then,
$$
\frac{1}{2\pi} \Delta \text{arg}\left\{ h(z) \right\}  = \text{No. Zeroes} - \text{No. Poles}
$$

By observation, this function have no poles in the first quadrant. To use the principle, I will first find the change in argument over the real axis $[0, R]$.

Along the real axis we have $z=x$ where $x \in \mathbb{R}$. In this case, $f(x)$ is an entirely real valued function, and so $\Delta \arg(f)=0$

Now, use the parametrization $R e^{ it }$ where $t\in[0, \pi /2]$. We have:
$$
\begin{align}
f(R e^{ it }) & = (R e^{ it })^{4} + (R e^{ it })^{3} + 5(R e^{ it })^{2} + 2(R e^{ it }) + 4 \\
 & = R^{4} e^{ 4it } \left( 1 + \frac{1}{R e^{ it }} + \frac{5}{R^{2} e^{ 2it }} + \frac{2}{R^{3} e^{ 3it }} + \frac{4}{R^{4}e^{ 4it }} \right)
\end{align}
$$
Taking the limit as $R\to \infty$, the argument change can be isolated to $e^{ 4it }$.
$$
\Delta \arg(e^{ 4it }) = 4\left( \frac{\pi}{2} \right) = 2\pi
$$
Along the imaginary axis, use $z=iy$. The function is now:
$$
f(iy) = (iy)^{4} + (iy)^{3} + 5(iy)^{2} + 2(iy) + 4 = y^{4} -iy^{3} -5y^{2}+2iy +4
$$
Visualise the change in argument using the imaginary are real parts:
$$
\begin{align}
\mathrm{Re}\left\{ f(iy) \right\} & = y^{4} -5y^{2}+4 \\
\mathrm{Im}\left\{ f(iy) \right\}  & = -y^{3} + 3y
\end{align}
$$
When $y\to \infty$ it lies to the right on the real axis. As $y\to 0$ it approaches 4 on the real axis. Furthermore, as $y$ decreases, the function goes into the fourth quadrant. This implies that $\arg(f)$ decreases by $2\pi$. 

Hence, the number of zeroes is:
$$
\frac{1}{2\pi} \Delta\arg(f) = \frac{1}{2\pi} (2\pi-2\pi) = \frac{1}{2\pi}(0) =0
$$
### Question 14
Try using Rouche's theorem. Define the two new functions:
$$
h(z) = z^{5} \qquad g(z) = z+1
$$
Along the circle $|z|=2$ we have:
$$
\begin{align}
|h|  & = 2^{5} \\
|g|  & = 2+1 =3
\end{align}
$$
We have $2^{5}>3$ and therefore $|h|>|g|$ I conclude that $h+g$ has the same number of zeroes as $h$ within this domain.

By observation, $h$ has 5 zeroes within this domain. Furthermore:
$$
h+g = z^{5} + z+1 = f
$$
And so $f$ has 5 zeroes within the disk $D$.
### Question 15
---
a.
To compute a Laurent series, I must expand 1 in terms of $z$. The coefficients follow the form:
$$
a_{n} = \frac{f^{(n)}(z_{0})}{n!}
$$
Where $f$ is the function in the numerator.

All derivatives of 1 are 0, and so all the coefficients are zero. However, this function is already in the form of a Laurent series. It is convergent everywhere except for $z=0$.

---
b.
This function has 3 poles. The Laurent series will be convergent on the unit circle around each of these three poles: $z=0,1, 2$. 