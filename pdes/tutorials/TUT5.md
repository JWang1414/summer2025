### Separation of Variables
Lets look at the diffusion equation
$$
u_{t}-ku_{xx}=0
$$
How many variables do you need for a well posed problem? Well, you would need the boundary conditions. And then you might need the initial values like $u(x,0)=f$

---

How does heat travel around a circle?

Lets say we have an initial condition like $u(x,0)=\phi(x)$

The boundary conditions would be along the circle, radians measured $-\pi$ and $\pi$
$$
\begin{align}
u(-\pi, t)=u(\pi, t) &  & u_{x}(-\pi,t)=u_{x}(\pi, t)
\end{align}
$$
- This means that the quantity and speed that the heat diffuses is continuous

Now, we solve this with separation of variables. Define $u(x, t)=X(x)T(t)$

Why are we allowed to make the assumption that $u(x, t)$ can be split into two functions?
- Imagine a vector space, in a 2-D vector space, it is possible to write any vector in-terms of two basis vectors
- In the case of separation of variables, we are, in a sense, attempting to search for the basis vectors to represent a 2-D solution
- $X(x)$ and $T(t)$ can be imagined as two basis vectors

The two separated equations are:
$$
\begin{align}
X''+\lambda X & =0 \\
T'+k\lambda T & =0
\end{align}
$$
Check if $\lambda=0$ is possible:
$$
X''=0\Rightarrow X(x)=Ax+B
$$
From the initial conditions, we have $X(\pi)=X(-\pi)$ and $X'(\pi)=X'(-\pi)$. Using this data, we get
$$
-A\pi+B=A\pi+B\Rightarrow A=0
$$
This means that $\lambda_{0}$ is a valid eigenvalue, and $X_{0}(x) = C_{0} /2$ is the eigenfunction.

Check if $\lambda$ is positive:

Define $\lambda=\beta^{2}>0$. We obtain the equation
$$
X''+\beta^{2}X=0\Rightarrow X(x)=A\cos(\beta x) + B\sin(\beta x)
$$
Subbing in the initial values again, we obtain
$$
2B\sin(B\pi)=0
$$
And therefore the eigenvalues are $\lambda_{n}=n^{2}$, $n \in \mathbb{Z}$. With eigenfunctions
$$
X_{n}=C_{n} \cos(nx) + D_{n} \sin(nx)
$$

Check if $\lambda$ is negative:

- In this case, you would repeat the same steps with $\lambda=-\beta^{2}<0$. This time, you will find there are no solutions, and so no negative eigenvalues

Now, we swap our attention to the temporal equation. The solution is:
$$
T'=-k\lambda T \Rightarrow T_{n} = e^{ -kn^{2}t }
$$
And $T_{0}=1$. We can quickly assert this because we already know the eigenvalues.

Now, begin to define the solution
$$
u(x, t)=X_{0}T_{0} + \sum_{n=1}^{\infty} X_{n}(x)T_{n}(t) = \frac{C_{0}}{2} + \sum_{n=1}^{\infty} \left[ C_{n}\cos(nx) + D_{n}\sin(nx) \right] e^{ -kn^{2}t }
$$
The coefficients are:
$$
\begin{align}
C_{n} & = \frac{1}{\pi} \int_{-\pi}^{\pi} \cos(nx)\psi(x) \, dx  \\
D_{n} & = \frac{1}{\pi} \int_{-\pi}^{\pi} \sin(nx)\psi(x) \, dx 
\end{align}
$$
