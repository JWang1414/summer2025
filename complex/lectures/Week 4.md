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
Notably, the real and complex parts of a holomorphic function are always harmonic. That is, if $f=u+iv$ where $f, u, v$ are functions, then $u$ and $v$ are harmonic

$u, v : \mathbb{R}^{2}\to \mathbb{R}$ are called harmonic conjugates if they satisfy the Cauchy-Riemann equations
- Conjugates are only unique up to the addition of a constant

Theorem:
> Let $\Omega \subseteq \mathbb{C}$ be open and $f : \Omega\to \mathbb{C}$. Then, if $f$ is analytic at $z\in \Omega$ if and only if partials $u_{x}=v_{y}$ and $u_{y}=-v_{x}$ at $z$ and $u_{x}, u_{y}, v_{x}, v_{y}$ are continuous at $z$

Definition:
> A function $f : \Omega \in \mathbb{C} \to \mathbb{C}$ is called *entire* if it is analytic and $\Omega=\mathbb{C}$

---
Example:  Let $z=re^{ i\theta }$. Recall that $\log z = \log r + i\theta$. Let $-\pi<\theta<\pi$, $r>0$

WTS $\log z$ is analytic

First, recall the properties of multi variable derivatives. Lets say we have a variable change from $(x, y)\to(r, \theta)\to(u, v)$ then the Jacobians follow:
$$
\begin{bmatrix}
u_{x} & u_{y} \\
v_{x} & v_{y}
\end{bmatrix} = \begin{bmatrix}
u_{r} & u_{\theta} \\
v_{r} & v_{\theta}
\end{bmatrix} \begin{bmatrix}
r_{x} & r_{y} \\
\theta_{x} & \theta_{y}
\end{bmatrix}
$$
Notice that the matrix on the left is the CR equations. On the right is a propagation of the chain rule.

In polar coordinates, we define $r=\sqrt{ x^{2}+y^{2} }$ and $\theta = \arctan\left( \frac{y}{x} \right)$. The resulting Jacobian as:
$$
\begin{bmatrix}
r_{x} & r_{y} \\
\theta_{x} & \theta_{y}
\end{bmatrix} = \begin{bmatrix}
\cos \theta & \sin \theta \\
\sin \theta /r & \cos \theta /r
\end{bmatrix}
$$
Cutting out the details, from these equations we can derive
$$
\begin{align}
u_{r} = \frac{v_{\theta}}{r} &  & v_{r} = \frac{u_{\theta}}{r}
\end{align}
$$
- This is, in a sense, the polar version of the CR equations

Going back to the example with the logarithms, we get
$$
\begin{align}
u_{r} & = \frac{1}{r} &  & v_{\theta}=1 \\
u_{\theta}  & =0 &  & v_{r}=0
\end{align}
$$
These functions are all continuous at $r\neq 0$, and the CR equations all hold, hence, we conclude the $\log$ is an analytic function.

---
The properties of the complex derivative are as you would expect from real differentiation. They appear to still be linear, product, division, and chain rules appear identical.

Polynomials are entire, and rational functions are analytic on domain.

Theorem:
> Let $f=u+iv$ be analytic on a domain (connected, open set). If $u$ is constant or $v$ is constant or $u^{2}+v^{2}$ is constant, then $f$ is also constant.

We have defined the complex derivative $f'(z) = \frac{df}{dz}$. So now, what should $\frac{df}{d\bar{z}}$ mean? Well, using the CR equations, it is possible to prove that:
$$
\text{CR Equations hold} \iff \frac{df}{d\bar{z}} = 0
$$
This has no limit interpretation, however, so it's not really possible to give it a formal expression, nor realistic to give it a meaningful interpretation
