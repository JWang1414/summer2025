### Orthogonality and General Fourier Series
For two real-values continuous functioned functions $f(x)$ and $g(x)$ defined on an interval $a\leq x\leq b$, we define the *inner product* to be:
$$
(f, g) \equiv \int_{a}^{b} f(x)g(x) \, dx
$$
- This is always a real number
- $f(x)$ and $g(x)$ are called *orthogonal* if $(f, g)=0$
- No function is orthogonal to itself except $f(x)\equiv 0$
Fourier series works, and is so powerful, because we know that every eigenfunction is orthogonal to every other eigenfunction.

Green's second identity:
$$
\int_{a}^{b} (-X_{1}'' X_{2} + X_{1}X_{2}'') \, dx = (-X_{1}' X_{2} + X_{1}X_{2}')\big|^{b}_{a}
$$
If you evaluate this right hand term for: Dirichlet, Neumann, Periodic, and Robin boundary conditions, it will always resolve to 0

The identity reduces to:
$$
(\lambda_{1} - \lambda_{2}) \int_{a}^{b} X_{1}X_{2} \, dx = 0
$$
Assuming that $\lambda_{1} \neq \lambda_{2}$, we conclude that $X_{1}$ and $X_{2}$ are orthogonal.
### Symmetric Boundary Conditions
Note that the right hand side of Green's second identity is not always zero. The boundary conditions must satisfy some condition.

Take any arbitrary pair of boundary conditions:
$$
\begin{align}
\alpha_{1} X(a) + \beta_{1} X(b) + \gamma_{1} X'(a) + \delta_{1} X'(b)  & =0 \\
\alpha_{2} X(a) + \beta_{2} X(b) + \gamma_{2} X'(a) + \delta_{2} X'(b)  & =0
\end{align}
$$
A set of boundary conditions is called symmetric if:
$$
f'(x)g(x) - f(x)g'(x) \bigg|^{x=b}_{x=a} =0
$$
- All the standard/typical boundary conditions we will encounter in this course are symmetric

Theorem 1:
> Given symmetric boundary conditions, then any two eigenfunctions that correspond to distinct eigenvalues are orthogonal. Therefore, if any function is expanded in a series of these eigenfunctions, the coefficients are determined

If $X_{n}(x)$ denotes the eigenfunction with the eigenvalue $\lambda_{n}$ and if:
$$
\phi(x) = \sum_{n} A_{n}X_{n}(x)
$$
Is a convergent series, where $A_{n}$ are constants, then:
$$
(\phi, X_{m}) = \left( \sum_{n}A_{n}X_{n} , X_{m} \right) = \sum_{n} A_{n}(X_{n}, X_{m}) = A_{m}(X_{m}, X_{m})
$$
And the formula for the coefficients is:
$$
A_{m} = \frac{(\phi, X_{m})}{(X_{m}, X_{m})}
$$
Note that it is possible for $X_{1}$ and $X_{2}$ to be non-orthogonal eigenfunctions if $\lambda_{1} = \lambda_{2}$. However, they can be made orthogonal using the Gram-Schmidt method
### Negative Eigenvalues
Theorem 3:
> Assume the same conditions as Theorem 1. If:
$$
f(x)f'(x) \bigg|_{x=a}^{x=b} \leq 0
$$
> For all real-valued functions, $f(x)$ satisfying the boundary conditions, then there is no negative eigenvalue
