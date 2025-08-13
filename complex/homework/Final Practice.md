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
Therefore:
$$
\frac{1}{\sin z} = \sum_{k=0}^{\infty} (-1)^{-k} z^{-2k-1} (2k+1)!
$$
Which is equivalent to:
$$
\sum_{k=-\infty}^{0} (-1)^{k} z^{2k-1}(1-2k)!
$$
Notice that the function $\sin ^{-1}(z)$ has just one singularity within the unit circle centred at zero. Therefore, according to the residue theorem:
$$
\int _{\gamma} f(z) \, dz = 2\pi i \sum_{z_{k} \text{ within }\gamma} \text{Res}(f;z_{k})
$$
Where $z_{k}$ denote the finite number of zeroes within $\gamma$. This residue is equal to the -1th term of the Laurent series, defined above, which is:
$$
(-1)^{-1} z^{2(-1)-1} (1-2(-1))! = \frac{1}{-1} z^{-3} (3)! = -\frac{6}{z^{3}}
$$
