### Question 2
This function is the Gaussian multiplied by a polynomial. Recall that for any arbitrary function $h(x)$,
$$
\mathcal{F}\{ xh(x) \} = i \frac{d\hat{h}(k)}{dk}
$$
Define the function $g(x)=e^{ -ax^{2}/2 }$, then,
$$
f(x) = xe^{ -ax^{2}/2 } = xg(x) \implies \hat{f}(k) = \mathcal{F}\{ xg(x) \} = i \frac{d\hat{g}(k)}{dk}
$$
$g(x)$ is simply a Gaussian function, which is invariant under the Fourier transform. I will apply the property:
$$
h(x) = e^{ -\alpha x^{2} } \implies \hat{h}(k) = \sqrt{ \frac{\pi}{\alpha} } e^{ -k^{2}/4\alpha }
$$
For any arbitrary constant $\alpha>0$. For the function $g(x)$, $\alpha=a /2$, valid since $a>0$. Therefore,
$$
\hat{g}(k) = \sqrt{ \frac{\pi}{(a /2)} } e^{ -k^{2}/4(a /2) } = \sqrt{ \frac{2\pi}{a} } e^{ -k^{2}/2a }
$$
I conclude that the Fourier transform of $f(x)$ is:
$$
\hat{f}(k) = i \frac{d\hat{g}(k)}{dk} = i \sqrt{ \frac{2\pi}{a} } \frac{d}{dk} e^{ -k^{2}/2a } = -\frac{\sqrt{ 2\pi }ik}{a^{3/2}} e^{ -k^{2}/2a }
$$
### Question 3
Expand the Laplace operator:
$$
\begin{cases}
u_{xx} + u_{yy} =0 \\
u(x, 0) = g(x)
\end{cases}
$$
Take the Fourier transform of both side in terms of $x$. Start with the PDE:
$$
\widehat{u_{xx}} + \widehat{u_{yy}} = (ik)^{2} \hat{u} + \hat{u}_{yy} = -k^{2} \hat{u} + \hat{u}_{yy} =0
$$
Now, the boundary conditions:
$$
\hat{u}(k, 0) = \hat{g}(k)
$$
Which has the solution:
$$
\hat{u}(k, y) = A(k) e^{ -|k|y } + B(k) e^{ |k|y }
$$
We are interested in a bounded solution for $u(x, y)$, and therefore $B(k)=0$. From the boundary conditions:
$$
\hat{u}(k, 0) = A(k) e^{ 0 } = A(k) = \hat{g}(k)
$$
Invert the function:
$$
\mathcal{F}^{-1}\left\{ \hat{g}(k)e^{ -|k|y } \right\} = (g*f)(x, y) = (f*g)(x, y)
$$
Since, under the Fourier transform, convolution is:
$$
\widehat{(a*b)}(k) = \hat{a}(k)\hat{b}(k)
$$
For any two arbitrary functions $a$ and $b$. Furthermore, I have defined the function:
$$
\hat{f} = e^{ -|k|y } \implies f = \mathcal{F}^{-1} \left\{ e^{ -|k|y } \right\} = \frac{1}{2\pi} \frac{2y}{y^{2}+x^{2}} = \frac{y}{\pi(x^{2}+y^{2})}
$$
Hence,
$$
u(x, y) = (f*g)(x, y) = \frac{1}{\pi} \int_{-\infty}^{\infty} \frac{y}{y^{2}+(x-z)^{2}} g(z) \, dz
$$
