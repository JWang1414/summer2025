Recall the diffusion equation with homogeneous Dirichlet boundary conditions
$$
\begin{cases}
u_{t}=ku_{xx},  & 0<x<l, t>0 \\
u(0,t) = u(l,t)=0,  & t>0 \\
u(x,0)=\phi(x),  & 0<x<l
\end{cases}
$$
- Notice that this is over the finite line, so we will be applying the separation of variables algorithm

Look for solutions of the PDE and boundary conditions of the form $X(x)T(t)$
$$
X(x)T'(t)=kX''(x)T(t) \implies -\frac{T'(t)}{kT(t)} = -\frac{X''(x)}{X(x)} = \lambda
$$
Where $\lambda$ is some constant. This gives us two eigenvalue problems, associated with the same eigenvalue
$$
\begin{align}
X''+\lambda X & = 0 \\
T'+\lambda kT & = 0
\end{align}
$$
By boundary conditions, we have $X(0)T(t)=X(l)T(t)=0$. We obtain $X(0)=X(l)=0$. This same boundary value problem has already been solved during the wave equation.
- There are only positive eigenvalues $\lambda_{n}=(n\pi /l)^{2}$ with $X_{n}=\sin(n\pi x /l)$, where $n\in \mathbb{N}$

Going back to the temporal part, we get
$$
T'+\left( \frac{n\pi}{l} \right)^{2}kT = 0
$$
This is a common ODE, with a known solution, that being:
$$
T_{n}(t) = A_{n}\exp \left[ \frac{-n^{2}\pi^{2}kt}{l^{2}} \right]
$$
Now, we have separated solutions to the PDE, and the boundary conditions
$$
u_{n}=X_{n}(x)T_{n}(t) = A_{n}\exp \left[ -\frac{n^{2}\pi^{2}kt}{l^{2}} \right] \sin\left( \frac{n\pi x}{l} \right)
$$
Consider the series
$$
u(x, t) = \sum_{n=1}^{\infty} A_{n}\exp \left[ -\frac{n^{2}\pi^{2}kt}{l^{2}} \right] \sin\left( \frac{n\pi x}{l} \right)
$$
Then, from the initial condition $u(x,0)=\phi(x)$, we get:
$$
\phi(x) = \sum_{n=1}^{\infty} A_{n}\sin\left( \frac{n\pi x}{l} \right)
$$
- This is our Fourier sine-series
Conclude the coefficients are:
$$
A_{n} = \frac{2}{l} \int_{0}^{l} \phi(x)\sin\left( \frac{n\pi x}{l} \right) \, dx
$$
---
Example
$$
\begin{cases}
u_{t}=ku_{xx},  & 0<x<l, t>0 \\
u(0,t)=u(l,t)=0,  & t>0 \\
u(x,0)=1
\end{cases}
$$
Since $\phi(x)=1$, the coefficients simplify into
$$
\begin{align}
A_{n} & =\frac{2}{l} \int_{0}^{l} \sin\left( \frac{n\pi x}{l} \right) \, dx  \\
 & = -\frac{2}{l} \frac{l}{n\pi} \cos\left( \frac{n\pi x}{l} \right) \bigg|^l_{0} \\
 & = -\frac{2}{n\pi}\left[ \cos n\pi - 1 \right] 
\end{align}
$$
Which we can simplify into cases
$$
A_{n} = \begin{cases}
0,  & n\text{ even} \\
\frac{4}{n\pi},  & n\text{ odd}
\end{cases}
$$
The full solution is
$$
u(x, t) = \sum_{n\text{ odd}} \frac{4}{n\pi} \exp \left[ -\frac{n^{2}\pi^{2}kt}{l^{2}} \right] \sin\left( \frac{n\pi x}{l} \right)
$$
- Alternatively, if you dislike writing "$n$ odd", then you can use $2n-1$ to generate infinite odd values
---
Diffusion equation with homogeneous Neumann boundary conditions
$$
\begin{cases}
u_{t}=ku_{xx},  & 0<x<l,t>0 \\
u_{x}(0,t)=u_{x}(l,t)=0,  & t>0 \\
u(x,0)=\phi(x),  & 0<x<l
\end{cases}
$$
We still have the relation $X''+\lambda X=0$, however, we have new boundary conditions.

Check if $\lambda=0$ could be an eigenvalue:
$$
X''=0 \Rightarrow X(x)=C+Dx
$$
Which yields
$$
\begin{align}
X'(0)=D=0,  &  & X(x)=C,  &  & X'(l)=0
\end{align}
$$
Therefore $\lambda=0$ is an eigenvalue with corresponding eigenfunction that is any constant

Check if the eigenvalue is negative:

Write $\lambda=-\gamma^{2}$ to check if $\lambda<0$. Let $\gamma>0$.
$$
X''=\gamma^{2}(X)\Rightarrow X(x) = C \cosh(\gamma x)+D\sinh(\gamma x)
$$
Now,
$$
\begin{align}
X'(x) & =\gamma C\sinh(\gamma x) + \gamma D\cosh(\gamma x) \\
X'(0) & =\gamma D=0\Rightarrow D=0\Rightarrow X(x)=C \cosh(\gamma x) \\
X'(l) & =\gamma c\sinh(\gamma l)=0\Rightarrow C=0
\end{align}
$$
Which means we have no negative eigenvalues.

Check for positive eigenvalues. This time, we will use $\lambda=\beta^{2}$ instead of $\gamma$
$$
X''=-\beta^{2}X\Rightarrow X(x)=C\cos(\beta x) + D\sin(\beta x)
$$
Then,
$$
\begin{align}
X'(x)  & = -C\beta \sin(\beta x)+D\beta \cos(\beta x) \\
X'(0)  & = D\beta=0\Rightarrow D=0\Rightarrow X(x)=C\cos(\beta x) \\
X'(l) & =-C\beta \sin(\beta l)=0
\end{align}
$$
We do not want $C=0$, and so instead take $\sin(\beta l)=0$. Which means that $\beta l=n\pi$. The positive eigenvalues are therefore
$$
\lambda=\beta^{2}=\left( \frac{n\pi}{l} \right)^{2}
$$
Written together, the eigenvalue and eigenfunctions are:
$$
\begin{align}
\lambda_{n}=\left( \frac{n\pi}{l} \right)^{2} &  & X_{n}(x)=C_{n}\cos\left( \frac{n\pi x}{l} \right), \text{ where }n = 0, 1, 2, \dots
\end{align}
$$
Temporal eigenfunctions are
$$
T_{n} = \tilde{C}_{n } \exp \left[ -\frac{n^{2}\pi^{2}kt}{l^{2}} \right]
$$
Writing it out as a series, to derive the Fourier cosine series:
$$
u(x, t) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} A_{n} \exp \left[ -\frac{n^{2}\pi^{2}kt}{l^{2}} \right] \cos\left( \frac{n\pi x}{l} \right)
$$
Recall that $u(x,0)=\phi(x)$ requires
$$
\phi(x) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} A_{n}\cos\left( \frac{n\pi x}{l} \right)
$$
Which is the Fourier cosine series we wanted. The constants are:
$$
A_{n} = \frac{2}{l} \int_{0}^{l} \phi(x)\cos\left( \frac{n\pi x}{l} \right) \, dx , \text{ where }n=0, 1, 2, \dots
$$
Wave equation with homogeneous Neumann boundary conditions
$$
\begin{cases}
u_{tt}=c^{2}u_{xx},  & 0<x<l, t>0 \\
u_{x}(0,t)=u_{x}(l,t)=0,  & t>0 \\
u(x,0)=\phi(x), u_{t}(x,0)=\psi(x),  & 0<x<l
\end{cases}
$$
Begin by looking for solutions of the form $X(x)T(t)$
$$
X(x)T''(t) = c^{2}X''(x)T(t) \Rightarrow -\frac{T''}{c^{2}T} = -\frac{X''}{X} = \lambda
$$
Where $\lambda$ is a constant. Which yields the equations
$$
\begin{align}
X''+\lambda X=0,  &  & T''+\lambda c^{2}T=0
\end{align}
$$
We have already solved a similar equation for $X$, with the boundary conditions $X'(0)=X'(l)=0$. The solutions are:
$$
\lambda_{n} = \left( \frac{n\pi}{l} \right)^{2}, X_{n} = \cos\left( \frac{n\pi x}{l} \right), \text{where } n=0, 1, 2, \dots
$$
Now, we would like to solve the temporal problem.

In the case when $n=0$, $T''=0$
$$
T(t) = A+Bt
$$
In the case when $n\geq 1$
$$
T_{n}(t) = A_{n}\cos\left( \frac{n\pi ct}{l} \right) + B_{n}\sin\left( \frac{n\pi ct}{l} \right)
$$
$$
u(x, t) = \frac{1}{2}A_{0} + \frac{1}{2}B_{0} + \sum_{n=1}^{\infty} \left( A_{n}\cos\left( \frac{n\pi ct}{l} \right) + B_{n}\sin\left( \frac{n\pi ct}{l} \right) \right)\cdot \cos\left( \frac{n\pi x}{l} \right)
$$
Applying the condition $u(x,0)=\phi(x)$
$$
\phi(x) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} A_{n}\cos\left( \frac{n\pi x}{l} \right)
$$
- Which is a cosine series
Applying the condition $u_{t}(x,0) = \psi(x)$
$$
\psi(x) = \frac{1}{2}B_{0} + \sum_{n=1}^{\infty} B_{n} \frac{n\pi c}{l}\cos\left( \frac{n\pi x}{l} \right)
$$
- Which is another cosine series