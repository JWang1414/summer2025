### The Fourier Transform
> Let $f(x)$ be an integrable real-valued function on $\mathbb{R}$; that is,
$$
\int_{-\infty}^{\infty} \left| f(x) \right|  \, dx <\infty
$$
> For each $k\in \mathbb{R}$, we define the *Fourier transform* of the function $f$ at $k$ to be:
$$
\hat{f}(k) := \int_{-\infty}^{\infty} f(x) e^{ -ikx } \, dx
$$

- Notice that, after a Fourier transform, the function of $x$ is now a function of $k$.

Alternate notation for the Fourier transform looks like:
$$
\mathcal{F}\{ f \} = \hat{f} \qquad \mathcal{F}\{ f(x) \}(k) = \hat{f}(k)
$$
- As a function of $k$, $\hat{f}$ is bounded, since $\left| e^{ -ikx } \right|=1$
### Properties of the Fourier Transform
The Fourier transform is a linear operation on functions. That is,
$$
\widehat{(af_{1}+bf_{2})}(k) = a\hat{f}_{1}(k) + b \hat{f}_{2}(k)
$$
For two integrable functions $f_{1}$ and $f_{2}$ and $a,b\in \mathbb{R}$

Differentiation is transformed into complex polynomial multiplication:
$$
\widehat{\frac{df}{dx}}(k) = \int_{-\infty}^{\infty} \frac{df}{dx} e^{ -ikx } \, dx = ik\hat{f}(k)
$$
This is valid for $n$ degrees of differentiation:
$$
\widehat{\frac{df^{(n)}}{dx^{n}}}(k) = (ik)^{n} \hat{f}(k)
$$

Fourier Inversion Theorem:
> Suppose $f$ and $\hat{f}$ are integrable and continuous. Then:
$$
f(x) = \frac{1}{2\pi} \int_{-\infty}^{\infty} \hat{f}(k) e^{ ikx } \, dk
$$

Alternative notation for the inverse Fourier transform looks like:
$$
\mathcal{F}^{-1}\{ g \} = \check{g} \qquad \mathcal{F}^{-1}\{ g(k) \} = \check{g}(x)
$$
And so, from the Fourier inversion formula, we have:
$$
\check{\hat{f}}=f
$$
### Convolution of Functions
The *convolution* of function is a form of "multiplication of functions". If $f(x)$ and $g(x)$ are functions over $\mathbb{R}$, then the convolution $f*g$ is a new function defined over $\mathbb{R}$ by:
$$
(f*g)(x) := \int_{-\infty}^{\infty} f(x-y)g(y) \, dy
$$
Where, in the integral, $x$ is fixed.
- The solutions to many important PDEs are expressed as convolutions

Convolutions are commutative:
$$
(f*g)(x) = (g*f)(x)
$$
Differentiation of convolutions follows the form:
$$
(f*g)'(x) = (f'*g)(x) = (f*g')(x)
$$
The Fourier transform of a convolution is ordinary pointwise multiplication:
$$
\widehat{(f*g)}(k) = \hat{f}(k) \hat{g}(k)
$$
In terms of the Fourier transform, we have:
$$
\left[ \hat{f}(k)\hat{g}(k) \right] ^{\vee} = (f*g)(x)
$$
If $f$ and $g$ are integrable functions such that $fg$ is also integrable then:
$$
\widehat{f(x)g(x)}(k) = \frac{1}{2\pi} (\hat{f}*\hat{g})(k)
$$
### More Properties of the Fourier Transform
Translation:
$$
\widehat{f(x-a)} = e^{ -iak } \hat{f}(k) \qquad \widehat{e^{ iak }f(x)} = \hat{f}(k-a)
$$
Scaling. For any $a>0$:
$$
\widehat{\frac{1}{a}f\left( \frac{x}{a} \right)} = \hat{f}(ak) \qquad \widehat{f(ax)} = \frac{1}{a} \hat{f} \left( \frac{k}{a} \right)
$$
The Fourier transform changes differentiation in real space into polynomial multiplication in Fourier space:
$$
\widehat{xf(x)} = i \frac{d\hat{f}(k)}{dk}
$$
Invariance of the Gaussian:
$$
f(x) = e^{ -x^{2}/2 } \implies \hat{f}(k) = \sqrt{ 2\pi } e^{ -k^{2}/2 }
$$
### Using Fourier Transform for Linear PDEs
1. Fourier transform both sides of the PDE in the space variable and also Fourier transform the data at $t=0$
2. Solve for $\hat{u}$ using the fact that in the transformed variables, the differentiation is now algebraic. For each $k$, this results in an ODE for $\hat{u}(k, t)$ with initial condition given by the Fourier transform of the data at $k$
3. Solve the ODE initial value problem for $\hat{u}(k, t)$ at any time $t$
4. Take the inverse Fourier transform in the spatial variables to obtain $u(x, t)$. Here you will often need the fact that multiplication in Fourier space is convolution in real space

I will not include examples here. They are present in my class notes.
### Fourier Transform in Higher Space Dimensions
> Let $f$ be an integrable function on $\mathbb{R}^{N}$. We define its Fourier transform to be the complex-valued function on $\mathbb{R}^{N}$:
$$
\begin{align}
\hat{f}(\vec{k}) & := \int_{-\infty}^{\infty} \dots \int_{-\infty}^{\infty} \dots \int_{-\infty}^{\infty} f(\vec{x})e^{ -i\vec{k}\cdot \vec{x} } \, d\vec{x} \\
 & = \int_{-\infty}^{\infty} \dots \int_{-\infty}^{\infty} \dots \int_{-\infty}^{\infty} f(x_{1}, \dots, x_{n}) e^{ -ik_{1}x_{1} } \dots e^{ -ik_{n}x_{n} } \, dx_{1} \dots dx_{n}
\end{align}
$$
> For example, in dimension $N=3$,
$$
\hat{f}(\vec{k}) := \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} f(x_{1},x_{2},x_{3})e^{ -ik_{1}x_{1} } e^{ -ik_{2}x_{2} } e^{ -ik_{3}x_{3} } \, dx_{1} \, dx_{2}  \, dx_{3}
$$
- Note how the multiplication $kx$ in the exponential of the 1D Fourier transform is now $\vec{k}\cdot \vec{x}$.

> To conveniently label a general partial derivative of a function of several variables, we adopt the notation of Laurent Schwartz. Let $\alpha$ denote a vector with $N$ components whose entries are non-negative integers. Each entry $\alpha_{i}$ means $\alpha_{i}$ derivatives with respect to $x_{i}$, and $\alpha_{i}=0$ means no derivatives are taken. We call $\alpha$ a *multi-index*. Here is an example:
$$
\partial^{(2, 3, 2)} \phi(x_{1}, x_{2}, x_{3}) = \frac{ \partial^{7} }{ \partial x_{1}^{2} \partial x_{2}^{3} \partial x_{3}^{2} } \phi(x_{1}, x_{2}, x_{3})
$$
> $|\alpha|$ is therefore the total number of derivatives taken.

Let $\partial^{\alpha}$ denote the partial derivative associated with the multi-index $\alpha=(\alpha_{1}, \dots, \alpha_{N})$. Then for any $\vec{k}=(k_{1}, \dots, k_{N})\in \mathbb{R}$, we define the polynomial $\vec{k}^{\alpha}$ to be:
$$
\vec{k}^{\alpha} = k_{1}^{\alpha_{1}}k_{2}^{\alpha_{2}} \dots k_{N}^{\alpha_{N}}
$$
If $\alpha$ is any multi-index, then:
$$
\widehat{\partial^{\alpha}f}(\vec{k}) = i^{|\alpha|} \vec{k}^{\alpha} \hat{f}(\vec{k})
$$
