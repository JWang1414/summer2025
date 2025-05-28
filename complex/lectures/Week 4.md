For some complex function $f : \Omega \in \mathbb{C}\to \mathbb{C}$ at some point $z\in \Omega$ differentiation is defined to be:
$$
\lim_{ w \to z } \frac{f(w)-f(z)}{w-z} = \lim_{ h \to 0 } \frac{f(z+h)-f(z)}{h} \equiv f'(z)
$$
If we consider $h\in \mathbb{R}$, and $z=x+iy$, then the definition can also be written as:
$$
\lim_{ h \to 0 } \frac{f(x+h, y)-f(x, y)}{h} \equiv \frac{ \partial f }{ \partial x }
$$
Which is equivalent to the partial derivative. Going further, we can use $f(z)=u(z)+iv(z)$, and the definition of derivative can once again be written as:
$$
\frac{ \partial u }{ \partial x }  + i \frac{ \partial v }{ \partial x }
$$
Now, lets imagine $h=ik$ is a purely imaginary value $(k\in \mathbb{R})$. The complex definition transforms into:
$$
\lim_{ k \to 0 } \frac{f(x, y+k)-f(x, y)}{ik} = \frac{1}{i}\frac{ \partial f }{ \partial y } = -i \left( \frac{ \partial u }{ \partial y } +i \frac{ \partial v }{ \partial y }  \right) = \frac{ \partial v }{ \partial y } -i \frac{ \partial u }{ \partial y }
$$
### Cauchy-Riemann Equations
If $f'(z)$ exists, then:
$$
f'(z) = \frac{ \partial u }{ \partial x } +i \frac{ \partial v }{ \partial x } = \frac{ \partial v }{ \partial y } -i \frac{ \partial u }{ \partial y }
$$
Which tells us that
$$
\begin{align}
u_{x}=v_{y} &  & v_{x}=-u_{y}
\end{align}
$$
For some function $f(z) = u(z)+iv(z)$

Interestingly, the real Jacobian is:
$$
D_{f}=\begin{pmatrix}
u_{x} & u_{y} \\
v_{x} & v_{y}
\end{pmatrix}
$$
- This implies that, for complex functions, the Jacobian is vastly simplified
- However, I'm not sure if this is true
### Differentiability
If $f'(z)$ exists for all $z$ in its domain, then $f$ is called *holomorphic* or *analytic*

Methods to check differentiability
- From definition
- If the Cauchy-Riemann equations disagree

> Example: $f(z)=\bar{z}$

From definition
$$
\lim_{ h \to 0 } \frac{\bar{z}+\bar{h} - \bar{z}}{h} = \lim_{ h \to 0 } \frac{\bar{h}}{h}
$$
Which DNE

Using Cauchy-Riemann
$$
\begin{align}
u_{x}=1 &  & v_{y}=-1
\end{align}
$$
Which do not agree, and so it is not complex differentiable

---

A function $f : \mathbb{R}^n\to \mathbb{R}$ is called harmonic if:
$$
\frac{ \partial ^2g }{ \partial x^{2}_{1} } + \frac{ \partial^{2}g }{ \partial x_{2}^{2} } + \dots + \frac{ \partial^{2}g }{ \partial x_{n}^{2} } = 0
$$
Notably, the real and complex parts of a holomorphic function are harmonic. That is, if $f=u+iv$ where $f, u, v$ are functions, then $u$ and $v$ are harmonic

$u, v : \mathbb{R}^{2}\to \mathbb{R}$ are called harmonic conjugates if they satisfy the Cauchy-Riemann equations
- Conjugates are only unique up to the addition of a constant
