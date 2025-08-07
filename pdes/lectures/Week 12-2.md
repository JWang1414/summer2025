The FT and inverse FT are defined to be:
$$
\int_{-\infty}^{\infty} \left| f(x) \right| ^{2} \, dx = \frac{1}{2\pi} \int_{-\infty}^{\infty} \left| \hat{f}(k) \right|  \, dk
$$
Try not to get the factor of $2\pi$ confused.

Recall from last class we were proving the uncertainty principle. We have $f(x)$ normalized such that:
$$
\int_{-\infty}^{\infty} \left| f(x) \right| ^{2} \, dx =1
$$
We have position and momentum defined as:
$$
\bar{x}^{2} = \int_{-\infty}^{\infty} \left| xf(x) \right| ^{2} \, dx \qquad \bar{k}^{2} = \int_{-\infty}^{\infty} \left| k\hat{f}(k) \right| ^{2} \, \frac{dk}{2\pi}
$$
The uncertainty theorem states that:
$$
\bar{x} \bar{k} \geq \frac{1}{2}
$$
For the proof, we use the Schwarz inequality:
$$
\left| \int_{-\infty}^{\infty} xf(x)f'(x) \, dx  \right| \leq \left[ \int_{-\infty}^{\infty} \left| xf(x) \right| ^{2} \, dx  \right] ^{1 /2} \left[ \int_{-\infty}^{\infty} \left| f'(x) \right| ^{2} \, dx  \right] ^{1 /2}
$$
Notice that this first term is equivalent to the position:
$$
\bar{x} \left[ \int_{-\infty}^{\infty} \left| f'(x) \right| ^{2} \, dx  \right] ^{1 /2}
$$
Which, using Plancherel's theorem we have:
$$
\bar{x} \left[ \frac{1}{2\pi} \int_{-\infty}^{\infty} \left| k\hat{f}(k) \right| ^{2} \, dk ^{1 /2} \right] = \bar{x} \bar{k}
$$
Going back to the first integral, on the left hand side:
$$
\int_{-\infty}^{\infty} xf(x)f'(x) \, dx = \frac{1}{2} x\left[ f(x) \right] ^{2}\bigg|^{\infty}_{-\infty} - \int_{-\infty}^{\infty} \frac{1}{2} \left[ f(x) \right] ^{2} \, dx = 0-\frac{1}{2} = -\frac{1}{2}
$$
The size of this part is therefore one half and we have:
$$
\frac{1}{2} < \bar{x}\bar{k}
$$
As needed.
### Laplace Transform
> Let $f(t)$ given for $t\geq 0$, the Laplace transform of $f$, denoted as $\mathcal{L}\{ f(t) \}$ or $F(s)$, is given by:
$$
\mathcal{L}\{ f(t) \}(s) := \int_{0}^{\infty} f(t)e^{ -st } \, dt
$$
> Which is valid whenever this integral converges.

---
Example:
Let $f(t)=1$ defined for all $t\geq 0$,
$$
\mathcal{L}\{ 1 \}(s) = \int_{0}^{\infty} e^{ -st } \, dt = -\frac{1}{s}e^{ -st }\bigg|^{\infty}_{0} =0-\left( -\frac{1}{s} \right) =\frac{1}{s}
$$
---
Example:
$$
\mathcal{L}\{ \sin(at) \} = \int_{0}^{\infty} e^{ -st }\sin(at) \, dt
$$
Don't feel like writing all the computations. You just use integration by parts a few times. The answer is:
$$
\frac{1}{a} - \frac{s^{2}}{a^{2}} F(s) \Rightarrow F(s) = \frac{a}{s^{2}+a^{2}}
$$
---

The Laplace transform is linear,
$$
\mathcal{L}\{ c_{1}f_{1}(t)+c_{2}f_{2}(t) \} = c_{1} \mathcal{L}\{ f_{1}(t) \} + c_{2} \mathcal{L}\{ f_{2}(t) \}
$$
Derivatives are:
$$
\mathcal{L}\{ f'(t) \} = s \mathcal{L}\{ f(t) \} - f(0)
$$
$$
\mathcal{L}\{ f^{(n)}(t) \} = s ^{n} \mathcal{L}\{ f(t) \} - s ^{n-1} f(0) - \dots - sf^{(n-2)}(0) - f^{n-1}(0)
$$

---
Example:
Solve the IVP
$$
y'' + 2y' + y = 2 \sin t, y(0)=0, y'(0)=0
$$
By linearity, we have:
$$
\mathcal{L}\{ y'' \} + 2 \mathcal{L}\{ y' \} + \mathcal{L}\{ y \} = 2 \mathcal{L}\{ \sin t \}
$$
Which, swapping notation, is equal to:
$$
s ^{2} Y(s) - sy(0) - y'(0) + 2 \left[ sY(s) - y(0) \right]  + Y = \frac{2}{s ^{2}+1}
$$
Which can be simplified into the ODE:
$$
s ^{2} Y(s) + 2s Y(s) + Y(s) = \frac{2}{s ^{2}+1}
$$
Which gives us the equation:
$$
Y(s) = \frac{2}{(s ^{2}+1)(s ^{2}+2s+1)} = \frac{1}{s+1} + \frac{1}{(s+1)^{2}} - \frac{s}{s^{2}+1}
$$
This is the Laplace transform:
$$
\mathcal{L}\{ e^{ -t } \} + \mathcal{L}(te^{ -t }) - \mathcal{L}\{ \cos t \} \Rightarrow y(t) = e^{ -t } + te^{ -t } - \cos t
$$
---
### Step Functions
To deal with functions having discontinuities, it's helpful to introduce the *unit step function*, or *Heaviside function*,
$$
u_{c}(t) = \begin{cases}
0 & t<c \\
1 & t\geq c
\end{cases}
$$
The Laplace transform is:
$$
\mathcal{L}\{ u_{c}(t) \} = \int_{c}^{\infty} e^{ -st } \, dt = \frac{1}{s}e^{ -sc }
$$
Sometimes, we may write a function in terms of the related function $g(t)$
$$
g(t) = u_{c}(t) f(t-c)
$$
Theorem:
$$
\mathcal{L}\{ u_{c}(t)f(t-c) \} = e^{ -cs } \mathcal{L}\{ f(t) \}
$$
> .

---
Example:
$$
\mathcal{L}\{ f(ct) \}
$$
Defined for $c>0$.
$$
\int_{0}^{\infty} e^{ -st }f(ct) \, dt = \frac{1}{c} \int_{0}^{\infty} e^{ -s \sigma/c } f(\sigma) \, d\sigma
$$
Where we have used the substitution $\sigma=ct$. This above integral can be evaluated to:
$$
\frac{1}{c} F\left( \frac{s}{c} \right)
$$
- And so we have scaling under Laplace transformations
---
Example:
$$
\mathcal{L}\{ tf(t) \} = \int_{0}^{\infty} e^{ -st }tf(t) \, dt = \int_{0}^{\infty} \frac{d}{ds}\left[ -e^{ -st } \right] f(t) \, dt
$$
Which is:
$$
-\frac{d}{ds} \int_{0}^{\infty} e^{ -st }f(t) \, dt = -F'(s)
$$
---

Theorem:
$$
\mathcal{L}\{ e^{ ct }f(t) \} = F(s-c)
$$
> This can be proven via direct computation

---
Example:
$$
\begin{cases}
y''(t)=f(t) \\
y(0)=0, y'(0)=0
\end{cases}
$$
The function $f$ is given:
$$
\begin{cases}
0  & t<1\\
t-1 & t\geq 1
\end{cases}
$$
And so we have:
$$
f(t) = (t-1)u_{c}(t)
$$
$$
s ^{2}Y(s) - sy(0) - y'(0) = \mathcal{L}\{ (t-1)u_{1}(t) \}
$$
$$
s ^{2}Y = \mathcal{L}\{ (t-1)u_{1}(t) \}
$$
$$
s ^{2}Y(s) = e^{ -s }\mathcal{L}(t) = \frac{1}{s^{2}}e^{ -s }\Rightarrow Y(s) = \frac{1}{s ^{4}} e^{ -s }
$$
Invert
$$
y(t) = \mathcal{L}^{-1}\left\{  e^{ -s } \frac{1}{s ^{4}}  \right\} = u_{1}(t) \frac{1}{6} (t-1)^{3}
$$
