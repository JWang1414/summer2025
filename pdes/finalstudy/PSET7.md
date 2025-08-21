### Question 2
For this problem, recall two different properties of the Fourier transform. Under multiplication by a polynomial, the Fourier transform is:
$$
\mathcal{F}\{ xf(x) \} = i \frac{d\hat{f}(k)}{dk}
$$
Where $f$ is some arbitrary function. The invariance of the Gaussian under the Fourier transform:
$$
\mathcal{F}\{ e^{ -ax^{2} } \} = \sqrt{ \frac{\pi}{a} }e^{ -k^{2}/4a }
$$
Where $a>0$. From the first identity,
$$
\mathcal{F}\{ xe^{ -ax^{2}/2 } \} = i \frac{d}{dk} \mathcal{F}\{ e^{ -ax^{2}/2 } \}
$$
From the second,
$$
\mathcal{F}\{ e^{ -ax^{2}/2 } \} = \sqrt{ \frac{\pi}{(a /2)} } e^{ -k^{2}/4(a/2) } = \sqrt{ \frac{2\pi}{a} } e^{ -k^{2}/2a }
$$
Substituting back into the previous computations,
$$
= i \frac{d}{dk} \left[ \sqrt{ \frac{2\pi}{a} } e^{ -k^{2}/2a } \right] = \sqrt{ \frac{2\pi}{a} }i \frac{d}{dk} e^{ -k^{2}/2a } = \sqrt{ \frac{2\pi}{a} } i e^{ -k^{2}/2a } \left( -\frac{1}{2a} \right)(2k) = -ik \frac{\sqrt{ 2\pi }}{a^{3/2}} e^{ -k^{2}/2a }
$$
---
### Question 3
Begin by computing a Fourier transform in the $x$ dimension on both sides of the equation:
$$
\Delta u = u_{xx} + u_{yy} =0 \implies (ik)^{2}u + \hat{u}_{yy} =0
$$
For the boundary conditions:
$$
\hat{u}(k, 0) = \hat{g}(k)
$$
Solve the newly obtained ODE:
$$
\hat{u}_{yy} = k^{2}u \implies u(k, y) = A(k)e^{ -|k|y } + B(k)e^{ |k|y }
$$
Which must be bounded as $y\to \infty$, therefore, $B(k)=0$. Apply the boundary conditions:
$$
\hat{u}(k, 0) = A(k)e^{ -0 } = A(k) = \hat{g}(k)
$$
So, the function we are interested in is:
$$
u(x, y) = \mathcal{F}^{-1}\{ \hat{g}(k)e^{ -|k|y } \} =\mathcal{F}^{-1}\{ \hat{g}(k)\hat{f}(k) \} = (f*g)(x, y)
$$
Where I have used a property of the convolution of functions under the Fourier transform, and defined a new function:
$$
\hat{f}(k) = e^{ -|k|y }
$$
The inverse Fourier transform of this function is:
$$
\mathcal{F}^{-1}\{ e^{ -|k|y } \} = \frac{1}{2\pi} \frac{2y}{y^{2}+x^{2}} = \frac{y}{\pi(x^{2}+y^{2})}
$$
$u$ is therefore,
$$
u(x, y) = (f*g)(x, y) = \int_{-\infty}^{\infty} f(x-z, y)g(z) \, dz = \int_{-\infty}^{\infty} \frac{y}{\pi((x-z)^{2}+y^{2})} g(z) \, dz
$$
