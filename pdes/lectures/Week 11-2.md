### Definition of the Fourier Transform & Fundamental Properties
For the Fourier transform to work, we require that $f(x)$ is integrable on $\mathbb{R}$
$$
\int_{-\infty}^{\infty} \left| f(x) \right|  \, dx <\infty
$$
> For each $k\in \mathbb{R}$, we define the Fourier transform of the function $f$ at $k$ to be
$$
\hat{f}(k) = \int_{-\infty}^{\infty} f(x)e^{ -ikx } \, dx
$$
> Where the transform is notated with the "hat"

The Fourier transform (FT) has transformed the function of $x$ into Fourier space ($k$-space) as opposed to the original space where $x$ lives.
$$
\mathcal{F}\{ f \} = \hat{f} \qquad \mathcal{F}\{ f(x) \}(k) = \hat{f}(k)
$$
The FT is related to the original function in a convoluted and non-local way $\to$ to find $\hat{f}$ at any point $k$, we need to incorporate (integrate) the values of the original function everywhere.

In general, $\hat{f}(k)$ is also complex. However, FT of several important function has no imaginary part.

FT is bounded. For all $k\in \mathbb{R}$,
$$
\left| \hat{f}(k) \right|  \leq \int_{-\infty}^{\infty} \left| f(x) \right| \left| e^{ -ikx } \right|  \, dx = \int_{-\infty}^{\infty} \left| f(x) \right|  \, dx < \infty
$$
FT is a linear operation on functions. If $f_{1}$ and $f_{2}$ are integrable, then:
$$
(a f_{1} + b f_{2}) (k) = a \hat{f}_{1}(k) + b \hat{f}_{2} (k)
$$

---
Example:
Let $a>0$ and consider:
$$
f(x) = \begin{cases}
1 & |x|<a \\
0 & |x|\geq a
\end{cases}
$$
Compute the FT:
$$
\begin{align}
\hat{f}(k) & = \int_{-\infty}^{\infty} f(x)e^{ -ikx } \, dx  \\
 & = \int_{-a}^{a} e^{ -ikx } \, dx  \\
 & = -\frac{1}{ik} e^{ -ikx } \bigg|^a_{-a} \\
 & = \frac{2}{k} \sin(ak)
\end{align}
$$
Things to note:
- This FT has no imaginary part
- $f$ has compact support and took only the values 0, 1
	- Compact support means that a function is zero outside of a region
	- The FT is not compactly supported and takes on a continuum of values
---

A large motivation behind the use of FT is for derivatives. So, lets investigate its behaviour.

Suppose $f(x)$ and $\frac{df}{dx}$ both integrable, then,
$$
\begin{align}
\frac{d}{dx} \hat{f}(k) & = \int_{-\infty}^{\infty} \frac{df}{dx} e^{ -ikx } \, dx = \lim_{ L \to \infty } \int_{-L}^{L} \frac{df}{dx} e^{ -ikx } \, dx  \\
 & = \lim_{ L \to \infty } \left( f(x) e^{ -ikx }|^L_{-L} - \int_{-L}^{L} f(x) (-ik) e^{ -ikx } \, dx  \right)
\end{align}
$$
$|f(L)|$ and $|f(-L)|$ must tend to zero at $L\to \infty$ because $f$ and $f'$ are integrable over the entire real line. This gives us:
$$
= (ik) \int_{-\infty}^{\infty} f(x) e^{ -ikx } \, dx = ik \hat{f}(k)
$$
And so FT transforms differentiation into complex polynomial multiplication.

Under the assumption that all relevant derivatives are integrable, we find the identity:
$$
\frac{d^{n}}{dx^{n}} \hat{f}(k) = (ik)^{n} \hat{f}(k)
$$
Should we be concerned that transformations into Fourier space we are losing information? That is, is it possible to go back to the original function by inverting the FT?

For nice, integrable functions, we have the Fourier inversion formula. Suppose $f$ and $\hat{f}$ are integrable, then:
$$
f(x) = \frac{1}{2\pi} \int_{-\infty}^{\infty} \hat{f}(k) e^{ ikx } \, dk
$$
The inverse FT of a function $g(k)$ is defined to be:
$$
\mathcal{F}^{-1}\{ g \} = \frac{1}{2\pi} \int_{-\infty}^{\infty} g(k) e^{ ikx } \, dk
$$
And the Fourier inversion formula states that $\mathcal{F}^{-1}\{ \hat{f}(k) \}(x) = f(x)$
- There's another way to notate the Fourier transform, with an inverted hat, but I cannot find it
- Hopefully I can find it later

---
Example:
Find the FT of $f(x)=e^{ -a|x| }$ where $a>0$.

$$
\begin{align}
\mathcal{F}\{ e^{ -a|x| } \} & = \int_{-\infty}^{\infty} e^{ -a|x| } e^{ -ikx } \, dx  \\
 & = \int_{-\infty}^{0} e^{ (a-ik)x } \, dx + \int_{0}^{\infty} e^{ -(a+ik)x } \, dx  \\
 & = \lim_{ b \to \infty } \left[ \frac{e^{ (a-ik)x }}{a-ik} \right] ^0_{b} + \lim_{ b \to \infty } \left[ \frac{e^{ -(a+ik)x }}{-a-ik} \right] ^b_{0} \\
 & = \frac{2a}{a^{2}+k^{2}}
\end{align}
$$
---

- Besides that factor of $2\pi$, the only difference between the FT and inverse FT is a sign change in the exponential. 
Using a neutral variable $y$, for any nice function $g$
$$
\mathcal{F}\{ g \}(y) = \hat{g}(y) = 2\pi \mathcal{F}^{-1}\{ g \}(-y)
$$
So suppose we know the FT of $f(x)$ is some function $g(k)$, and we want to find the FT of $g$. Then,
$$
\hat{g}(y) = 2\pi \mathcal{F}^{-1}\{ g \}(-y) = 2\pi \mathcal{F}\{ \mathcal{F}^{-1}\{ f \}(-y) \} = 2\pi f(-y)
$$

---
Example:
We have just found:
$$
\mathcal{F}\{ e^{ -a|x| } \} = \frac{2a}{a^{2}+k^{2}}
$$
And therefore we have:
$$
\mathcal{F}\left\{  \frac{2a}{a^{2}+x^{2}}  \right\} = 2\pi e^{ -a|k| }
$$
---

REMEMBER TO UPDATE THE INVERSE FOURIER TRANSFORM NOTATION
