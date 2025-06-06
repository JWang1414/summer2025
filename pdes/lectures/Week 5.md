### Diffusion equation, in-homogeneous, half-line
- Now, we will try to solve the diffusion equation on the half-line, with Dirichlet boundary conditions
$$
\begin{cases}
u_{t} - ku_{xx} = f(x, t) &  & 0<x<\infty, t>0 \\
u(x,0)=\phi(x) \\
u(0,t)=0
\end{cases}
$$
Since we're doing Dirichlet boundary conditions, we choose to define the odd extensions $\phi _\text{odd}$ and $f_\text{odd}$ with respect to $x=0$
$$
\begin{cases}
u_{t}-ku_{xx} = f_\text{odd}(x, t) &  & -\infty<x<\infty, t>0 \\
u(x,0) = \phi _\text{odd}(x)
\end{cases}
$$
The solution to this will be the solution we already solved for (diffusion with a source).
- $v(0,t)=0$ is automatically satisfied, because it is an odd function
- The solution will be the restriction $u=v$ for $x>0$
$$
u(x, t) = \int_{-\infty}^{0} S(x-y)\phi _\text{odd}(y) \, dy + \int_{0}^{\infty} \dots \, dy + \int_{0}^{t} \left[ \int_{-\infty}^{0} S(x-y, t-s)f_\text{odd}(y, s) \, dy + \int_{0}^{\infty} \dots \, dy  \right]  \, ds
$$
Skipping over the intermediate steps, we get:
$$
\int_{0}^{\infty} \left[ S(x-y, t)-S(x+y, t) \right] \phi(y) \, dy + \int_{0}^{t} \int_{0}^{\infty} \left[ S(x-y, t-s)-S(x+y, t-s) \right] f(y, s) \, dy  \, ds
$$
---
Now, lets try the same problem with $u(0,t)=h(t)$.

Define a new function $v(x, t) = u(x, t)-h(t)$.

Then, we have $u_{t} = u_{t}-h'$, $v_{xx} = u_{xx}$.
$$
\begin{cases}
v_{t}-kv_{xx}=f(x, t) - h',  &  & 0<x<\infty, t>0 \\
v(x,0) = u(x,0)-h(0) = \phi(x)-h(0) \\
v(0,t) = u(0,t) - h(t) = h(t)-h(t)=0
\end{cases}
$$
Now, the final condition is once again 0, so we can just repeat the same derivation above.

---
Try it for the Neumann problem

$$
\begin{cases}
u_{t}-ku_{xx} = f(x, t) &  & 0<x<\infty, t>0 \\
u(x,0)=\phi(x) \\
u_{x}(0,t) = 0
\end{cases}
$$
Since this is the Neumann problem, we will use an even extension. This is a pretty familiar problem, so I won't write it down. The solution is the same as the Dirichlet problem, with a slight change of sign
$$
\int_{0}^{\infty} \left[ S(x-y, t)+S(x+y, t) \right] \phi(y) \, dy + \int_{0}^{t} \int_{0}^{\infty} \left[ S(x-y, t-s)+S(x+y, t-s) \right] f(y, s) \, dy  \, ds
$$
---
Now, what about the Neumann problem with $u_{x}(0,t) = h(t)$?

Define a new function $v(x, t) = u(x, t) - xh(t)$

Which gives us
$$
\begin{align}
v_{t}=u_{t}-xh'(t),  &  & v_{xx}=u_{xx}
\end{align}
$$
And the problem changes to
$$
\begin{cases}
v_{t}-kv_{xx}=f(x, t) = f(x, t)-xh'(t),  &  & 0<x<\infty, t>0 \\
v(x,0) = u(x,0) - xh(0) = \phi(x) - xh(0) \\
v_{x}(0,t) = u_{x}(0,t) - h(t) = h(t)-h(t) = 0
\end{cases}
$$
So now, we can go back again to the solution we have already found, and use it for this modified problem.
### Transport Equation
Recall that the solution to the homogeneous version:
$$
\begin{cases}
u_{t} + cu_{x} = 0 \\
u(x,0) = \phi(x)
\end{cases}
$$
Is the general equation $g(x-ct)$. So now, we will use Duhammel's equation to solve for
$$
\begin{cases}
u_{t}+cu_{x} = f(x, t) \\
u(x,0) = \phi(x)
\end{cases}
$$
Define the new equations:
$$
\begin{align}
u & =u^h+u^p \\
 & =\phi(x-ct) + \int_{s=0}^{s=t} w(x, t;s) \, ds 
\end{align}
$$
Where $w$ solves
$$
\begin{cases}
w_{t} + cw_{x} = 0, -\infty<x<\infty, t>s \\
w(x,s;s) = f(x, s)
\end{cases}
$$
$w$ will be the original solution to the transport equation, but shifted by some $s$:
$$
w = f(x-c(t-s))
$$
Which we can substitute back into the formula above:
$$
u = \phi(x-ct) + \int_{0}^{t} f(x-c(t-s)) \, ds
$$
### Finite Line
These are the lines were $0<x<L$. Doing away with the $\pm \infty$ bounds.
- This is a lot more physically relevant
- The key topic to study here will be separation of variables

One way to tackle the finite line is to split up your original function into a summation.

Consider a function $\phi(x)$ defined on $(0, l)$. Our goal is the determine coefficients for:
$$
\phi(x) = \sum_{i=1}^{\infty}A_{i} \sin\left( \frac{i\pi x}{l} \right)
$$
- We would like the partial sum $S_{N} = \sum_{i=1}^{N}A_{i}\sin(\dots)$ to converge to the number $\phi(x)$ as $N\to \infty$
	- Which, as expected, requires the coefficients $A_{i}$ to be selected based on the particular function $\phi(x)$

We will use the orthogonality relations:
$$
\int_{0}^{l} \sin\left( \frac{n\pi x}{l} \right)\sin\left( \frac{m\pi x}{l} \right) \, dx =0\text{, if }m\neq n
$$
To use this, we will multiply $\phi(x)$ by a sin factor, and integrate:
$$
\begin{align}
\int_{0}^{l} \phi(x)\sin\left( \frac{m\pi x}{l} \right) \, dx  & = \int_{0}^{l} \sum_{i=1}^{\infty} A_{i}\sin\left( \frac{i\pi x}{l} \right)\sin\left( \frac{m\pi x}{l} \right) \, dx  \\
 & = \sum_{i=1}^{\infty} A_{i}\int_{0}^{l} \sin\left( \frac{i\pi x}{l} \right)\sin\left( \frac{m\pi x}{l} \right) \, dx \\
 & = A_{m}\int_{0}^{l} \sin ^{2}\left( \frac{m\pi x}{l} \right) \, dx  \\
 & = \frac{A_{m}l}{2}
\end{align}
$$
After some algebra, we obtain
$$
A_{m} = \frac{2}{l}\int_{0}^{l} \phi(x)\sin\left( \frac{m\pi x}{l} \right) \, dx
$$
These are the coefficients that we needed previously
- If a series exists for some function $\phi(x)$, then the series is called a *Fourier sine series* for $\phi(x)$ on the interval $(0,l)$
---
Example: Find the Fourier sine series for $\phi(x)=x$ on $(0,l)$
$$
A_{n} = \frac{2}{l}\int_{0}^{l} x \sin\left( \frac{n\pi x}{l} \right) \, dx = \frac{2}{l}\left[ -\frac{xl}{n\pi}\cos\left( \frac{n\pi x}{l} \right)\bigg|^l_{0} + \int_{0}^{l} \frac{l}{n\pi}\cos\left( \frac{n\pi x}{l} \right) \, dx  \right]
$$
Which can be simplified into
$$
\begin{align}
 & =-\frac{2l}{n\pi} \cos(n\pi) \\
 & =(-1)^{n+1} \frac{2l}{n\pi}
\end{align}
$$
The full Fourier sine series can be written:
$$
\phi(x) = x = \sum_{n=1}^{\infty} (-1)^{n+1} \frac{2l}{n\pi} \sin\left( \frac{n\pi x}{l} \right)
$$
---
### Fourier Cosine Series
$$
\phi(x) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} A_{n}\cos\left( \frac{n\pi x}{l} \right)
$$
Which, same as the sine series, is defined on $(0,l)$

Another orthogonality relation:
$$
\int_{0}^{l} \cos\left( \frac{n\pi x}{l} \right)\cos\left( \frac{m\pi x}{l} \right) \, dx =0\text{, if }m\neq n
$$
Repeating the same derivative, we obtain the coefficients
$$
A_{n} = \frac{2}{l} \int_{0}^{l} \phi(x)\cos\left( \frac{m\pi x}{l} \right) \, dx\text{, for }n=1, 2, 3, \dots
$$
Furthermore, in the case when $n=0$ we have
$$
\int_{0}^{l} \phi(x) \, dx = \int_{0}^{l} \left( \frac{1}{2}A_{0} + \sum_{i=1}^{\infty} A_{i}\cos\left( \frac{n\pi x}{l} \right)\right) \, dx = \frac{1}{2}A_{0}l
$$
And therefore we obtain,
$$
A_{0} = \frac{2}{l} \int_{0}^{l} \phi(x) \, dx
$$
---
Example:  Find the Fourier cosine series for $\phi(x)\equiv_{1}$ on $(0,l)$

Find the first coefficient
$$
A_{0}=\frac{2}{l}\int_{0}^{l} 1 \, dx =2
$$
And now
$$
A_{n} = \frac{2}{l}\int_{0}^{l} \cos\left( \frac{n\pi x}{l} \right) \, dx = 0
$$
Which results in:
$$
\phi(x)=1=\frac{1}{2}(2)+0 = 1
$$
- Good sanity check, but not very interesting
---
### Full Fourier Series
$$
\phi(x) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} \left( A_{n}\cos\left( \frac{n\pi x}{l} \right) + B_{n}\sin\left( \frac{n\pi x}{l} \right) \right)
$$
Which is valid on the interval $(-l,l)$

We use a new orthogonality relation: Pick any two functions from the set:
$$
\left\{  1, \cos\left( \frac{n\pi x}{l} \right), \sin\left( \frac{n\pi x}{l} \right)  \right\}
$$
Where $n\in \mathbb{N}$. Multiply them, and integrate over $(-l,l)$ to get 0

The coefficients for the series are:
$$
\begin{align}
A_{n}  & = \frac{1}{l}\int_{-l}^{l} \phi(x)\cos\left( \frac{n\pi x}{l} \right) \, dx , \, n=0, 1, 2 \\
B_{n} & = \frac{1}{l}\int_{-l}^{l} \phi(x)\sin\left( \frac{n\pi x}{l} \right) \, dx , \, n=1, 2, 3
\end{align}
$$
---
Example: Find the full Fourier series of $\phi(x)=x$ on $(-l,l)$

Solve for the first cosine coefficient:
$$
A_{0}=\frac{1}{l} \int_{-l}^{l} \phi(x) \, dx = \frac{1}{l}\int_{-l}^{l} x \, dx =0
$$
Solve for the rest of the cosine coefficients:
$$
\begin{align}
A_{n}  & = \frac{1}{l}\int_{-l}^{l} x \cos\left( \frac{n\pi x}{l} \right) \, dx  \\
 & =\frac{1}{l}\left[ \frac{xl}{n\pi}\sin\left( \frac{n\pi x}{l} \right) \bigg|^l_{-l} = \int_{-l}^{l} \frac{l}{n\pi}\sin\left( \frac{n\pi x}{l} \right) \, dx  \right]  \\
 & = \frac{1}{l} \left[ 0 + \frac{l^{2}}{n^{2}\pi^{2}} \cos\left( \frac{n\pi x}{l} \right) \bigg|^l_{-l} \right]  \\
 & =0
\end{align}
$$
Solve for the sine coefficients:
$$
\begin{align}
B_{n}  & = \frac{1}{l}\int_{-l}^{l} x \sin\left( \frac{n\pi x}{l} \right) \, dx  \\
 & = (-1)^{n+1} \frac{2l}{n\pi}
\end{align}
$$
- Which is the same thing we obtained when solving for the sin series!
---
### Even/Odd & Periodicity of Fourier Series
- The Fourier sine series is defined for any $x \in \mathbb{R}$. It is comprised of entirely odd function with period $2l$. Therefore, the Fourier sine series is an odd function with period $2l$
- Under the same analysis, we find that the cosine function is an even function with period $2l$
- The full Fourier series has period $2l$. However, we cannot say if it is odd or even
### Separation of Variables
- We will begin with separation of variables for boundary problems
- We will start with an algorithm to follow on PDEs with boundary conditions, and/or initial conditions

(Assume the PDE involves time and one spatial variables $x$)

1. Look for separated solutions to the PDE of the form $X(x)T(t)$. This reduces the solution to eigenvalue problems with components $X$ and $T$. Both with the same eigenvalue
2. The boundary conditions carry over to the eigenvalue problem for $X(x)$. Solving this problem will yield countably many eigenvalues $\lambda_{n}$, for which there exists non-trivial solutions $X_{n}(x)$
3. Solve the eigenvalue problem for $T(t)$ for each eigenvalue $\lambda_{n}$ found in the previous step
4. Arrive at countably many separated solutions $u_{n}(x, t)=X_{n}(x)T_{n}(t)$ to the PDE and boundary conditions
5. Consider an infinite linear combination of the $u_{n}(x, t)$ with coefficients TBD
6. Achieving the initial conditions is done by choosing appropriate coefficients

MISSING NOTES HERE