Ablowitz 2.4
### Question 2
Parametrize the unit circle around the origin:
$$
\gamma(t)=e^{ it }
$$
With $t\in[0,2\pi]$. Calculator the derivative
$$
\gamma'(t) = ie^{ it }
$$
Now, we can use the definition of the derivative
$$
\int_{\gamma}f(z) \, dz = \int_{a}^{b} f(\gamma(t))\gamma'(t) \, dt 
$$
---
a.
Write out the integral
$$
\int_{a}^{b} (1+2(e^{ it })+(e^{ it })^{2})(ie^{ it }) \, dt
$$
By linearity, this integral can be split into smaller, simpler integrals
$$
i\int_{0}^{2\pi} e^{ it } \, dt + 2i\int_{0}^{2\pi} e^{ it }e^{ it } \, dt +i \int_{0}^{2\pi} e^{ 2it }e^{ it } \, dt
$$
Define $n\in \mathbb{N}$. I will solve a single generalization for each of these integrals
$$
\int_{0}^{2\pi} e^{ nit } \, dt = \left[ \frac{1}{ni}e^{ nit } \right] ^{2\pi}_{0} = \frac{1}{ni} \left[ e^{ 2\pi ni }-e^{ 0 } \right] = \frac{1}{ni} \left[ 1-1 \right] = 0
$$
Therefore:
$$
\int_{\gamma} 1+2z+z^{2} \, dz = i(0)+2i(0)+i(0) = 0
$$
- This function is analytic everywhere, and since we are integrating over a closed curve, it should always be 0
---
b.
Compute:
$$
\int_{0}^{2\pi} \frac{1}{(e^{ it }-1 /2)^{2}}(ie^{ it }) \, dt
$$
Use the substitution $u = e^{ it }-1 /2$ and $du=ie^{ it }dt$
$$
\int u^{-2} \, du = -\frac{1}{u}
$$
Evaluate the bounds
$$
\left[ -\frac{1}{e^{ it }-1 /2} \right] ^{2\pi}_{0} = -\frac{1}{e^{ 2\pi i }-1 /2} + \frac{1}{e^{ 0 }-1 /2} = -\frac{1}{1-1 /2} + \frac{1}{1- 1 /2} = 0
$$
---
c.
Compute:
$$
\int_{0}^{2\pi} \frac{1}{\overline{e^{ it }}}(ie^{ it }) \, dt = \int_{0}^{2\pi} \frac{1}{e^{ -it }}(ie^{ it }) \, dt = i \int_{0}^{2\pi} e^{ 2it } \, dt = 0
$$
- I know this is zero from a previous computation
---
d.
Compute:
$$
\int_{0}^{2\pi} e^{ it }\overline{e^{ it }}(ie^{ it }) \, dt = \int_{0}^{2\pi} e^{ it }e^{ -it }(ie^{ it }) \, dt = i \int_{0}^{2\pi} e^{ it } \, dt = 0
$$
---
e.
I will simplify the function by writing it out as a power series
$$
\int_{\gamma}e^{ \bar{z} } \, dz = \int_{\gamma} \sum_{n=0}^{\infty} \frac{\bar{z}^n}{n!} \, dz
$$
Therefore, we can write out the integral as:
$$
\int_{0}^{2\pi} (ie^{ it }) \sum_{n=1}^{\infty} \frac{(\overline{e^{ it }})^n}{n!} \, dt = i \sum_{n=1}^{\infty} \int_{0}^{2\pi} (e^{ it }) \frac{e^{ -nit }}{n!} \, dt = i \sum_{n=1}^{\infty} \frac{1}{n!} \int_{0}^{2\pi} e^{ -nit }(e^{ it }) \, dt = i \sum_{n=1}^{\infty} \frac{1}{n!} \int_{0}^{2\pi} e^{ it(1-n) } \, dt
$$
Evaluate the integral on the inside
$$
\int_{0}^{2\pi} e^{ it(1-n) } \, dt  = \left[ \frac{1}{i(1-n)}e^{ it(1-n) } \right] ^{2\pi}_{0}
$$