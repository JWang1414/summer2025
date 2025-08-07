### Fourier Transform
Given $f(x)$, its Fourier transform is
$$
\hat{f}(k) = \int_{-\infty}^{\infty} f(x)e^{ -ikx } \, dx
$$
- There is a factor $1 /2\pi$ when converting to and from a Fourier transform. Sometimes expressed as a factor for $1 /\sqrt{ 2\pi }$, otherwise just expressed with the full fraction, but only on the inverse FT or FT

How do we know the factor inside the FT integral is integrable? Well, we can try to use the estimate:
$$
\left| \int_{-\infty}^{\infty} e^{ -ikx }f(x) \, dx  \right| \leq \int_{-\infty}^{\infty} \left| e^{ -ikx } \right| \left| f(x) \right|  \, dx = \int_{-\infty}^{\infty} \left| f(x) \right|  \, dx
$$
---
Example:
$$
\begin{cases}
u_{t} - \alpha u_{xx} =0 \\
u(x, 0) = f(x) & x \in \mathbb{R}
\end{cases}
$$
Take the FT in $x$
$$
\hat{u}_{t} - \alpha(-ik)^{2}\hat{u} =0
$$
$$
\hat{u}(k, 0) = \hat{f}(k)
$$
And so we now have an ODE with just one derivative in terms of $t$. It has the solution:
$$
\hat{u}_{t} =-\alpha k^{2}\hat{u} \Rightarrow \hat{u}(k, t) = A(k) e^{ -\alpha k^{2}t }
$$
And, from the initial conditions,
$$
\hat{u}(k, 0) = A(k) = \hat{f}(k)
$$
Now, we need to invert this Fourier transform for the solution:
$$
u(x, t) = 2\pi \int_{-\infty}^{\infty} e^{ ikx }\hat{f}(k)e^{ -\alpha k^{2}t } \, dk
$$
