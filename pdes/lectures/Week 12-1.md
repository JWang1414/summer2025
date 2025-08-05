Let $a>0$. Find the Fourier transform of
$$
f(x) = \begin{cases}
a-|x|  & |x|\leq a \\
0 & |x|>a
\end{cases}
$$
$$
\hat{f}(k) = \int_{-\infty}^{\infty} f(x)e^{ -ikx } \, dx = \int_{-a}^{a} (a-|x|)e^{ -ikx } \, dx
$$
$$
\int_{-a}^{0} (x+a)e^{ -ikx } \, dx + \int_{0}^{a} (a-x)e^{ -ikx } \, dx
$$
Split into numerous integrals:
$$
a \int_{-a}^{0} e^{ -ikx } \, dx + a\int_{0}^{a} e^{ -ikx } \, dx + \int_{-a}^{0} xe^{ -ikx } \, dx - \int_{0}^{a} xe^{ -ikx } \, dx
$$
I don't feel like writing down all the computations. It's just a lot of integration by parts. The answer is:
$$
\frac{2}{k^{2}} (1-\cos(ka))
$$
---
Use the FT to solve the IVP
$$
\begin{cases}
u_{t} + u_{xxx} =0  & -\infty<x<\infty, t>0 \\
u(x, 0) = g(x)
\end{cases}
$$
FT both sides of the PDE with respect to $x$ to obtain:
$$
\widehat{u_{xxx}}(k, t) + \widehat{u_{t}}(k, t) =0
$$
By the derivative rule we have:
$$
(ik)^{3}\hat{u}(k, t) + \hat{u}_{t}(k, t)=0
$$
And the initial condition becomes:
$$
\hat{u}(k, 0) = \hat{g}(k)
$$
Which is an ODE with the solution:
$$
\hat{u}(k, t) = A(k) e^{ ik^{3}t }
$$
From the initial conditions:
$$
\hat{u}(k, 0) = A(k) = \hat{g}(k)
$$
And therefore the solution to this ODE is:
$$
\hat{u}(k, t) = \hat{g}(k)e^{ -ik^{3}t }
$$
Now, we need to invert this function. We can use the convolution theorem for this.
$$
u(x, t) = \left[ \hat{g}(k)e^{ -ik^{3}t } \right] ^{\vee} = (g*F)(x, t)
$$
Where we have defined the new function:
$$
F = (e^{ ik^{3}t })^{\vee} = \frac{1}{2\pi} \int_{-\infty}^{\infty} e^{ -ik^{3}t }e^{ ikx } \, dk = \frac{1}{2\pi} \int_{-\infty}^{\infty} e^{ i(kx+k^{3}t) } \, dk
$$
Which can be written as:
$$
u(x, t) = \int_{-\infty}^{\infty} g(x-y) \left[ \frac{1}{2\pi} \int_{-\infty}^{\infty} e^{ i(ky+k^{3}t) } \, dk  \right]  \, dy
$$
Using the substitution $k^{3}t=z^{3} /3$, which function can be written in terms of the Airy function:
$$
\frac{1}{(3t)^{1 /3}} \int_{-\infty}^{\infty} g(x-y) Ai\left( \frac{y}{(3t)^{1 /3}} \right) \, dy
$$
---

### Plancherels' Theorem
Recall the class of integrable functions on $\mathbb{R}$, that is, functions $f$ with
$$
\int_{-\infty}^{\infty} \left| f(x) \right|  \, dx <\infty
$$
which is also sometimes denoted as $f\in L^{1}(\mathbb{R})$. The FT of an integrable function need not be integrable. Given the back and forth nature of the FT and inverse FTs, it is desirable to seek a space of functions with the property that the FT of any member of the space remains in the space.

Such a space exists, and we call this space $L^{2}(\mathbb{R})$, the space of square-integrable functions.
$$
\int_{-\infty}^{\infty} \left| f(x) \right| ^{2} \, dx <\infty
$$
In general, a function in $L^{2}(\mathbb{R})$ may not be integrable, so it is not clear how to define the Fourier transform on $L^{2}$ functions. The key to extending the FT to $L^{2}$ is a fundamental theorem.

Plancherel's Theorem:
> If $f\in L^{1}(\mathbb{R})\cap L^{2}(\mathbb{R})$, then
$$
\int_{-\infty}^{\infty} \left| f(x) \right| ^{2} \, dx = \frac{1}{2\pi} \int_{-\infty}^{\infty} \left| \hat{f}(k) \right| ^{2} \, dk
$$
- No proof for this theorem. We will assume it is true, because the proof is too far outside of this course.
### Heisenberg Uncertainty Principle
In QM, the Fourier variable $k$ represents momentum, and $x$ is position. The wave functions are normalized so that:
$$
\int_{-\infty}^{\infty} \left| f(x) \right| ^{2} \, dx =1
$$
The expected value of the square of the position is:
$$
\bar{x}^{2} = \int_{-\infty}^{\infty} \left| xf(x) \right| ^{2} \, dx
$$
The expected value of the square of the momentum is:
$$
\bar{k}^{2} = \frac{1}{2\pi} \int_{-\infty}^{\infty} \left| k \hat{f}(k) \right| ^{2} \, dk
$$
The uncertainty principle states that $\bar{x}\cdot \bar{k}\geq \frac{1}{2}$
- We omit the $\hbar$ in math
