### Convolution of Functions
An important form of multiplication of functions is called convolution. If $f$, $g$ are functions over $\mathbb{R}$, then the convolution $f*g$ is a new function defined over $\mathbb{R}$ given by
$$
(f*g)(x):= \int_{-\infty}^{\infty} f(x-y)g(y) \, dy
$$
Recall that the solution to the diffusion equal on $\mathbb{R}$ looked something like:
$$
u(x, t) = \frac{1}{\sqrt{ 4\pi kt }} \int_{-\infty}^{\infty} e^{ -(x-y)^{2}/4kt } \phi(y) \, dy
$$
Define the new function:
$$
S(x, t) = \frac{1}{\sqrt{ 4\pi kt }} = e^{ -x^{2}/4kt }
$$
And so the solution can also be represented as:
$$
u(x, t) = \int_{-\infty}^{\infty} S(x-y)\phi(y) \, dy = S*\phi
$$

Convolution is commutative. Let $z=x-y$, then we have:
$$
(f*g)(x) = \int_{-\infty}^{\infty} f(x-y)g(y) \, dy = \int_{-\infty}^{\infty} f(z)g(x-z) \, dx = (g*f)(x)
$$
Differentiation:
$$
\begin{align}
(f*g)'(x) & = \frac{d}{dx} \int_{-\infty}^{\infty} f(x-y)g(y) \, dy  \\
 & = \int_{-\infty}^{\infty} f'(x-y)g(y) \, dy
\end{align}
$$
By the commutative property we also have:
$$
(g*f)'(x) = \int_{-\infty}^{\infty} g'(x-y)f(y) \, dy
$$
And so the derivative is:
$$
(f*g)'(x) = (f'*g)(x) = (f*g')(x)
$$
Now, what about the Fourier transform?
$$
\begin{align}
\hat{(f*g)}(x) & = \int_{-\infty}^{\infty} (f*g)(x)e^{ -ikx } \, dx  \\
 & = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(x-y)e^{ ik(x-y) }g(y)e^{ -iky } \, dy  \, dx  \\
 & = \int_{-\infty}^{\infty} \left( \int_{-\infty}^{\infty} f(x-y)e^{ -ik(x-y) } \, dx  \right)g(y)e^{ -iky } \, dy
\end{align}
$$
Let $z=x-y$
$$
\begin{align}
= & \int_{-\infty}^{\infty} \left( \int_{-\infty}^{\infty} f(z)e^{ -ikz } \, dz  \right)g(y)e^{ -iky } \, dy  \\
= & \left( \int_{-\infty}^{\infty} f(z)e^{ -ikz } \, dz  \right)\left( \int_{-\infty}^{\infty} g(y)e^{ -iky } \, dy  \right)
\end{align}
$$
Which is the just the Fourier transform of two functions. Therefore, we have:
$$
\hat{(f*g)}(k)= \hat{f}(k)\hat{g}(k)
$$
And the inverse FT is as expected:
$$
\mathcal{F}^{-1}\{ \hat{f}(k)\hat{g}(k) \}= (f*g)(x)
$$
### Various Properties of the FT
Translation property of the FT:
$$
\hat{f(x-a)} = e^{ -iak }\hat{f}(k)
$$
That is:
$$
\begin{align}
\mathcal{F}\{ f(x-a) \} & = \int_{-\infty}^{\infty} f(x-a)e^{ -ikx } \, dx  \\
 & = e^{ -ika } \int_{-\infty}^{\infty} f(z)e^{ -ikz } \, dz = e^{ -ika } \hat{f}(k)
\end{align}
$$
And, furthermore, as you would expect:
$$
\mathcal{F}\{ e^{ iax }f(x) \} = \hat{f}(k-a)
$$
Scaling property:
$$
\hat{f(ax)} = \frac{1}{|a|} \hat{f}\left( \frac{k}{a} \right) \text{ where }a\neq  0
$$
Case $a>0$
$$
\begin{align}
\mathcal{F}\{ f(ax) \} & = \int_{-\infty}^{\infty} f(ax)e^{ -ikx } \, dx  \\
 & = \frac{1}{a} \int_{-\infty}^{\infty} f(z)e^{ -ikz/a } \, dz  \\
 & = \frac{1}{a} \hat{f}\left( \frac{k}{a} \right)
\end{align}
$$
Case $a<0$
$$
\begin{align}
\mathcal{F}\{ f(ax) \} & = \int_{-\infty}^{\infty} f(ax)e^{ -ikx } \, dx  \\
 & = \frac{1}{a} \int_{\infty}^{-\infty} f(z)e^{ -ikz/a } \, dz  \\
 & = -\frac{1}{a} \hat{f}\left( \frac{k}{a} \right)
\end{align}
$$
Multiplication by a polynomial:
$$
\hat{xf(x)} = i \frac{d\hat{f}(k)}{dk}
$$
Proof:
$$
\begin{align}
\mathcal{F}\{ xf(x) \} & = \int_{-\infty}^{\infty} xf(x) e^{ -ikx } \, dx  \\
 & = \int_{-\infty}^{\infty} xf(x) \frac{d}{dk}\left( \frac{e^{ -ikx }}{-ix} \right) \, dx  \\
 & = i \int_{-\infty}^{\infty} f(x) \frac{d}{dk} e^{ -ikx } \, dx  \\
  & = i \frac{d}{dk} \int_{-\infty}^{\infty} f(x) e^{ -ikx } \, dx  \\
 & = i \frac{d\hat{f}(k)}{dk}
\end{align}
$$
### Invariance of the Gaussian
Gaussian functions
$$
e^{ -x^{2}/2 }
$$
are special under the FT because the FT of a Gaussian is once again a Gaussian. That is:
$$
f(x) = e^{ -x^{2}/2 } \Rightarrow \hat{f}(k) = \sqrt{ 2\pi } e^{ -k^{2}/2 }
$$
### FT to Solve Linear PDEs
Consider linear PDEs with space $x$, time $t$ an data with $t=0$.
1. FT both sides of the PDE in the space variable and FT the data at $t=0$
2. In the transformed variable, the differentiation is now algebraic
	- For each $k$, we get an ODE for $\hat{u}(k,t)$
3. Solve the ODE initial value problem for $\hat{u}(k,t)$
4. Take the inverse FT in the spatial variable in obtain $u(x, t)$

---
Example:
Let $f(x)$ be integrable over $\mathbb{R}$, find the solution $y(x)$ to the ODE $y''-y=f$

Take FT in the variable $x$ on both sides of the ODE
$$
\begin{align}
\hat{y''}(k) - \hat{y}(k) & =\hat{f}(k) \\
 (ik)^{2} \hat{y}(k) - \hat{y}(k) & = \hat{f}(k) \\
-(1+k^{2})\hat{y}(k) & = \hat{f}(k) \\
\hat{y}(k) & = -\frac{\hat{f}(k)}{1+k^{2}}
\end{align}
$$
Take the inverse FT of both sides
$$
y(x) = \mathcal{F}^{-1}\left\{ - \left[ \hat{f}(k) \cdot \frac{1}{1+k^{2}} \right] (x) \right\}
$$
If we use the function $\hat{g}(k)=\frac{1}{1+k^{2}}$ then we have:
$$
y(x) = \mathcal{F}^{-1}\left\{ -(\hat{f}(k)\cdot \hat{g}(k))(x) \right\} = -(f*g)(x)
$$
The inverse Fourier transform of $g(k)$ is:
$$
\mathcal{F}^{-1}\left\{ \frac{1}{1+k^{2}} \right\} = \frac{1}{2} e^{ -|x| }
$$
Hence we have:
$$
y(x) = -(f*g)(x) = -\frac{1}{2} \int_{-\infty}^{\infty} f(x-z)e^{ -|z| } \, dz
$$
---
Example:
$$
\begin{cases}
u_{xx} + u_{tt} =0 \\
u(x, 0) = g(x) \\
u\text{ bdd}
\end{cases}
$$
FT both sides of PDE with respect to $x$
$$
\hat{u_{xx}}(k, t) + \hat{u_{tt}} (k, t) =0
$$
Note that:
$$
\hat{u_{t}} (k, t) = \int_{-\infty}^{\infty} u_{t}(x, t)e^{ -ikx } \, dx = \frac{ \partial \hat{u}(k, t) }{ \partial t } = \hat{u}_{t}(k, t)
$$
- Operators of time differentiation and space FT commute
And therefore the new equation is:
$$
(ik)^{2}\hat{u}(k,t) + \hat{u}_{tt}(k, t) =0
$$
And so:
$$
\begin{cases}
-k^{2}\hat{u}(k,t) + \hat{u}_{tt}(k,t) =0 \\
\hat{u}(k,0) = \hat{g}(k)
\end{cases}
$$
Which has the solution:
$$
\hat{u}(k,t) = A(k)e^{ -|k|t } + B(k)e^{ |k|t }
$$
We require our solution function to be bounded, and so the Fourier transform must also be bounded. Therefore $B(k)=0$. Now, from boundary conditions:
$$
\hat{u} = A(k)e^{ -|k|t } \Rightarrow \hat{u}(k,0) = A(k) = \hat{g}(k)
$$
Now invert our function:
$$
\mathcal{F}^{-1}\left\{ \hat{g}(k) e^{ -|k|t } \right\} = (g*F)(x, t) = (F*g)(x, t)
$$
Where:
$$
F = \mathcal{F}^{-1}\left\{ e^{ -|k|t } \right\}  = \frac{1}{2\pi} \frac{2t}{t^{2}+x^{2}} = \frac{t}{\pi(t^{2}+x^{2})}
$$
Hence,
$$
u(x, t) = (F*g)(x, t) = \frac{1}{\pi} \int_{-\infty}^{\infty} \frac{t}{t^{2}+(x-y)^{2}} g(y) \, dy
$$
---
### The FT in Higher Space Dimensions
...
- Didn't manage to write this stuff down

Definition:
Let $f$ be an integrable function $\mathbb{R}^{N}$. Then,
$$
\hat{f}(\vec{k}) := \int_{-\infty}^{\infty} \dots \int_{-\infty}^{\infty} f(\vec{x})e^{ -i\vec{k}\cdot \vec{x} } \, d\vec{x}
$$
...
- Missed more stuff lol

Theorem:
Let $\partial^{\alpha}$ denote the partial derivative associated with the multi-index $\alpha=(\alpha_{1}, \dots, \alpha_{N})$. For any $\vec{k}=(k_{1}, \dots, k_{N})\in \mathbb{R}$. Define polynomial $\vec{k}^{\alpha}$ to be
$$
\vec{k}^{\alpha} = k_{1} ^{\alpha_{1}} k_{2}^{\alpha_{2}} \dots k_{N}^{\alpha_{N}}
$$
Then we have
- I COULDN'T WRITE THIS DOWN EITHER FUUUUCK
