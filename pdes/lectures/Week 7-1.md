### Robin Boundary Condition
Consider the following eigenvalue problem for $X(x)$
$$
\begin{cases}
-X''=\lambda X \\
X'(0) - a_{0}X(0) = 0, X'(l) + a_{l}X(l)=0
\end{cases}
$$
Where $a_{0}$ and $a_{l}$ are given constants.

For this problem, $\lambda=0$ is an eigenvalue if and only if $a_{0}+a_{l} = -a_{0}a_{l}l$ corresponding to the eigenfunction $X(x) = D(a_{0}x+1)$

$\lambda=-\gamma^{2}<0$ is an eigenvalue when:
$$
\tanh(\gamma l) = -\frac{(a_{0}+a_{l})l}{\gamma^{2} + a_{0}a_{l}}
$$
Which is known as the eigenvalue equation. Solutions to this equation with $\gamma>0$ would give us negative eigenvalues $\lambda=-\gamma^{2}$. However, recall that this is incredibly challenging.

We will use a graphical analysis. That is, looks for intersections between the graphs on each side of the equation. Intersections correspond to negative eigenvalues with the eigenfunctions:
$$
X(x) = \cosh(\gamma x) + \frac{a_{0}}{l} \sinh(\gamma x)
$$

For positive eigenvalues $\lambda=\beta^{2}>0$, the ODE becomes:
$$
X''=-\beta^{2}X \Rightarrow X(x) = C \cos(\beta x) + D \sin(\beta x)
$$
Plugging this function into the boundary conditions yields:
$$
X'(0) - a_{0}X(0) = \beta D - a_{0}C=0\Rightarrow D=\frac{a_{0}C}{\beta}
$$
$$
\begin{align}
X'(l) + a_{l}X(l) & = (\beta D + a_{l}C) \cos(\beta l) + (-\beta C+a_{l}D)\sin(\beta l) \\
 & = (a_{0}C + a_{l}C) \cos(\beta l) + \left( -\beta C + \frac{a_{0}a_{l}C}{\beta} \right) \sin(\beta l) \\
 & =0
\end{align}
$$
We want to avoid the trivial solution $C=0$, so divide the entire thing by $C$ and multiply by $\beta$ to obtain
$$
(a_{0}+a_{l})\beta \cos(\beta l) = (\beta^{2} - a_{0}a_{l}) \sin(\beta l)
$$
Another eigenvalue equation. Solving this equation for $\beta>0$ gives us an eigenvalue $\lambda=\beta^{2}$, with the corresponding eigenfunction
$$
X(x) = C \cos(\beta x) + D \sin(\beta x) = C\left[ \cos(\beta x) + \frac{a_{0}}{\beta} \sin(\beta x) \right]
$$
### Orthogonality & General Fourier Series
The key to being able to determine the Fourier sine series and cosine series  coefficients was the orthogonality relations
- This was the case when we integrated sines and cosines to find that specific combinations would always result in 0
- With more complex boundary conditions, can we say that we have a series solution that can be picked to ensure the initial conditions hold?

This leads us to begin investigating orthogonality in general

Let $f, g$ be functions defined on an interval $a\leq x\leq b$. We define their inner product to be:
$$
(f,g) = \int_{a}^{b} f(x)g(x) \, dx
$$
And $f,g$ are orthogonal if $(f,g)=0$
- No function is orthogonal to itself except for zero

Let $X_{1}(x)$ and $X_{2}(x)$ be two different eigenfunctions $(-X''=\lambda X)$ with some boundary conditions (Dirichlet, Neumann, ...) we have:
$$
(-X_{1}'X_{2} + X_{1}X_{2}') = -X_{1}'X_{2}' - X_{1}''X_{2} + X_{1}X_{2}'' + X_{1}'X_{2}' = X_{1}X_{2}'' - X_{1}''X_{2}
$$
From which we can conclude
$$
\int_{a}^{b} -X_{1}''X_{2} + X_{1}X_{2}'' \, dx = \left[ -X_{1}'X_{2} + X_{1}X_{2}' \right] ^b_{a}
$$
Hence,
$$
(\lambda_{1}-\lambda_{2}) \int_{a}^{b} X_{1}X_{2} \, dx = \left[ -X_{1}'X_{2} + X_{1}X_{2}' \right] ^b_{a}
$$

For Dirichlet condition:
$$
X_{1}(a) = X_{1}(b) = X_{2}(a)=X_{2}(b)=0
$$
And so the right hand side of the equation resolves to zero

For Neumann condition:
$$
X_{1}'(a) = X_{1}'(b) = X_{2}'(a) = X_{2}'(b)=0
$$
And the right hand side similarly resolves to zero in this case

For periodic conditions:
$$
X_{j}(a) = X_{j}(b), X_{j}'(a)=X_{j}'(b)
$$
For $j=1, 2$. The right hand side again collapses to 0

For Robin conditions, you again get 0.

Therefore, in all cases we have $\lambda_{1}-\lambda_{2} \neq 0$ and $\int_{a}^{b} X_{1}X_{2} \, dx=0$. Which means that, then $X_{1}$ and $X_{2}$ correspond to distinct eigenvalues, the integral is 0, so they are orthogonal.

But, the right hand side $\left[ -X_{1}'X_{2} + X_{1}X_{2}' \right]^b_{a}$ is not always 0
- As an example, you can try $X(a)=X(b)$, $X'(a)=2X'(b)$

To solve this issue, we must constrain our boundary conditions to be *symmetric boundary conditions*. Which are boundary conditions that satisfy the right hand of the equation
$$
\begin{align}
\alpha_{1} X(a) + \beta_{1}X(b) + \gamma_{1}X'(a) + \delta_{1}X'(b)=0 \\
\alpha_{2} X(a) + \beta_{2} X(b) + \gamma_{2} X'(a) + \delta_{2} X'(b)=0
\end{align}
$$
Above is a general representation of boundary conditions with constants $\alpha_{n}, \beta_{2}, \dots$. In the cases we have considered so far, such as Dirichlet conditions, we just need to define the constants.

A set of boundary conditions is called *symmetric* if
$$
f'(x)g(x) - f(x)g'(x) \big| ^{x=b}_{x=a} =0
$$
For any pair of functions $f, g$ both of which satisfy the boundary conditions

Theorem:
> If you have symmetric boundary conditions, then any 2 eigenfunctions of $-X''=\lambda X$ that correspond to distinct eigenvalues are orthogonal. Therefore, if any function is expanded in a series of eigenfunctions, the coefficients are determined.

In fact, for some series of the form $\phi = \sum A_{n}X_{n}(x)$, then the coefficients are:
$$
A_{m} = \frac{(\phi, X_{m})}{(X_{m}, X_{m})}
$$
- Remark: If there are 2 different eigenfunctions with the same eigenvalue, then they don't have to be orthogonal
- If they are not orthogonal, you can make them orthogonal with the Gram-Schmidt method

---
Recall the diffusion equation with mixed boundary conditions
$$
\begin{cases}
u_{t} = ku_{xx}, & 0<x<l, t>0 \\
u(0, t)=0, u_{x}(l, t)=0, & t>0 \\
u(x,0)=\phi(x), & 0<x<l
\end{cases}
$$
Via separation of variables, we had the eigenvalue problem
$$
-X''=\lambda X, X(0)=X'(l)=0
$$
We found only positive eigenvalues
$$
\lambda_{n} = \left( \frac{(n+1 /2)\pi}{l} \right) ^{2}
$$
With eigenfunctions
$$
X_{n}(x) = \sin(\sqrt{ \lambda_{n} }x)$$
where $n=0, 1, 2, \dots$

The full solution is:
$$
u(x, t) = \sum_{n=0}^{\infty} A_{n} \exp \left( -\lambda_{n} kt \right) \sin(\sqrt{ \lambda_{n} }x)
$$
- Missing notes here

Claim
$$
A_{n} = \frac{2}{l} \int_{0}^{l} \phi(x) \sin(\sqrt{ \lambda_{n} }x) \, dx
$$
If $f(x)$ is such that $f(0)=f'(l)=0$, $g$ is such that $g(0)=g'(l)=0$. Check if this is symmetric:
$$
f'g-fg' |^l_{0} = 0-0-0+0=0
$$
Which confirms that it is indeed symmetric. By the theorem, we know that the coefficients are:
$$
A_{m} = \frac{(\phi, X_{m})}{(X_{m}, X_{m})} = \frac{\int_{0}^{l} \phi(x)X_{m(x)} \, dx }{\int_{0}^{l} X^{2}_{m}(x) \, dx }
$$
First:
$$
\int_{0}^{l} X^{2}_{m}(x) \, dx = \int_{0}^{l} \sin ^{2} \left[ \frac{(m+1 /2)\pi x}{l} \right]  \, dx = \frac{l}{2}
$$
Which is the same equation we obtained previously
$$
A_{m} = \frac{2}{l} \int_{0}^{l} \phi(x) \sin \left[ \frac{(m + 1 /2)\pi x}{l} \right]  \, dx
$$
---
### Negative Eigenvalues
Theorem:
> If you have symmetric boundary conditions with the ODE $-X''=\lambda X$, and $f(x)f'(x)\big|^{x=b}_{x=a}\leq 0$ for all functions $f(x)$ that satisfy the boundary conditions, then there is no negative eigenvalues

Green's First Identity:
$$
\int_{a}^{b} f''(x)g(x) \, dx = f'g|^b_{a} - \int_{a}^{b} f'(x)g'(x) \, dx
$$
---
Example:
Dirichlet conditions $f(a)=f(b)=0$, then we have:
$$
f(x)f'(x)|^b_{a}=0
$$
So the theorem holds, and we can conclude there are no negative eigenvalues

---
- This is an incredibly simple and quick test to check if you have negative eigenvalues