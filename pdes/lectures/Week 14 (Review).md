Consider the 2nd order equation:
$$
u_{xx} - 3u_{xt} - 4u_{tt}=0
$$
Is this function elliptic, parabolic, or hyperbolic?
$$
b^{2}-4ac = (-3)^{2} - 4(1)(-4) = 9 + 16 >0
$$
So this equation is hyperbolic.

Find the general solution $u(x, t)$ to the PDE.
$$
\left( \frac{ \partial  }{ \partial x } + \frac{ \partial  }{ \partial t }  \right) \left( \frac{ \partial  }{ \partial x } -4 \frac{ \partial  }{ \partial t }  \right) u=0
$$
Introduce the characteristic coordinates: $\eta=x-t$ and $\alpha=-4x-t$. Alternatively, you can use $\eta=x-t$ and $\alpha=4x+t$.

From here you apply the chain rule with these coordinates, and you can easily solve the PDE from there. You end up with:
$$
\begin{align}
\frac{ \partial  }{ \partial x } + \frac{ \partial  }{ \partial t }  & = 5u_{\alpha} \\
\frac{ \partial  }{ \partial x } - 4\frac{ \partial  }{ \partial t }  & = 5u_{\eta}
\end{align}
$$
The equation takes the form:
$$
25 u_{\alpha \eta} =0 \Rightarrow u_{\alpha \eta} =0 \Rightarrow f(\eta) + g(\alpha)
$$
Returning to the original coordinate system:
$$
u(x, t) = f(x-t) + g(4x+t)
$$
---
Solve:
$$
\begin{cases}
u_{tt} = c^{2} u_{xx} & 0<x<\infty, t>0 \\
u(x, 0) = \sin x & u_{t}(x, 0) =0 \\
u_{x}(0, t) =0
\end{cases}
$$
This is the Neumann problem for the wave equation on the half-line. We have the solution for the full line. So, use an even extension and restrict the full line to the half-line.

The whole line solution is given by D'Alembert's formula.

For $x>ct$, all arguments are positive, and the formula is:
$$
\begin{align}
u(x, t) & = \frac{1}{2} \left[ \phi(x+ct) + \phi(x-ct) \right] = \frac{1}{2} \left[ \sin(x+ct) + \sin(x-ct) \right]  \\
 & = \frac{1}{2} \left[ \sin x \cos ct + \cos x \sin ct + (\sin x \cos(-ct) + \cos x \sin(-ct)) \right]  \\
 & = \frac{1}{2} \left[ \sin x \cos ct + \cos x \sin ct + \sin x \cos ct - \cos x \sin ct \right]  \\
 & = \sin x \cos ct
\end{align}
$$
For $x<ct$ then $x-ct$ is negative, and we must use the even extension.
$$
\begin{align}
u(x, t) & = \frac{1}{2} \left[ \sin(x+ct) + \sin(ct-x) \right]  \\
 & = \frac{1}{2} \left[ \sin x \cos ct + \cos x \sin ct + \sin ct \cos(-x) + \cos ct \sin(-x) \right]  \\
 & = \frac{1}{2} \left[ \sin x \cos ct + \cos x \sin ct + \sin ct \cos x - \cos ct \sin x \right]  \\
 & = \cos x \sin ct
\end{align}
$$
The full solution can be written as:
$$
u(x, t) = \begin{cases}
\sin x \cos ct & x>ct \\
\cos x \sin ct & 0<x<ct
\end{cases}
$$
---
Consider the Klein-Gordon equation:
$$
u_{tt} - c^{2}u_{xx} + m^{2}u =0
$$
Where $c,m>0$ are constant. Define the quantity:
$$
E(t) := \frac{1}{2} \int_{-\infty}^{\infty} u^{2}_{t} + c^{2}u^{2}_{x} + m^{2}u^{2} \, dx
$$
Assuming that $u$ and its derivatives tend to 0 as $|x|\to \infty$. What can we conclude about $E$ as a function of $t$?
$$
\begin{align}
E'(t) & = \frac{1}{2} \int_{-\infty}^{\infty} 2u_{t}u_{tt} + 2c^{2}u_{x}u_{xt} + 2m^{2}uu_{t} \, dx  \\
 & = \int_{-\infty}^{\infty} u_{t}(c^{2}u_{xx}-m^{2}u) + c^{2}u_{x}u_{xt} + m^{2}uu_{t} \, dx  \\
 & = \int_{-\infty}^{\infty} c^{2} u_{t}u_{xx} + c^{2}u_{x}u_{xt} \, dx  \\
 & = c^{2} \left[ \int_{-\infty}^{\infty} u_{t}u_{xx} \, dx + c^{2} \int_{-\infty}^{\infty} u_{x}u_{xt} \, dx  \right] 
\end{align}
$$
Use integration by parts:
$$
\int_{-\infty}^{\infty} u_{t}u_{xx} \, dx = u_{t} u_{x} \big|_{-\infty}^{\infty} - \int_{-\infty}^{\infty} u_{tx}u_{x} \, dx
$$
The first term will tend to zero, and therefore we have:
$$
E'(t) = -c^{2} \int_{-\infty}^{\infty} u_{x}u_{xt} \, dx + c^{2} \int_{-\infty}^{\infty} u_{x}u_{xt} \, dx =0
$$
And so $E(t)$ is constant in time.

---
Use the method of separation of variables to solve:
$$
\begin{cases}
u_{xx} + u_{yy} =0 & x^{2}+y^{2}>a^{2} \\
u = h(\theta) & x^{2}+y^{2} = a^{2} \\
u \text{ bounded as } & x^{2}+y^{2}\to \infty
\end{cases}
$$
Separate variables in polar coordinates $u(r, \theta)= R(r)\Theta(\theta)$

Then, we have:
$$
u_{xx} + u_{yy} = u_{rr} + \frac{1}{r} u_{r} + \frac{1}{r^{2}} u_{\theta\theta} =0
$$
So,
$$
R''\Theta + \frac{1}{r} R'\Theta + \frac{1}{r^{2}} R\Theta''
$$
Divide everything by $R\Theta$ and multiply everything by $r^{2}$
$$
r^{2} \frac{R''}{R} + r \frac{R'}{R} + \frac{\Theta''}{\Theta} =0
$$
Which gives us the eigenvalue problem:
$$
\begin{align}
\Theta'' + \lambda \Theta & =0 \\
r^{2} R'' + rR' - \lambda R & =0
\end{align}
$$
Begin with the analysis of the comparatively simpler $\Theta$ equation. Recall the periodic boundary equations:
$$
\begin{align}
\Theta(0) & = \Theta(2\pi) \\
\Theta'(0) & = \Theta'(2\pi)
\end{align}
$$
Check if the boundary conditions are symmetric. Define $X_{1}$ and $X_{2}$ as two functions which satisfy the boundary conditions. Then, we have:
$$
\left[ X_{1}'X_{2} - X_{1}X_{2}' \right] ^{2\pi}_{0} = X_{1}'(2\pi)X_{2}(2\pi) - X_{1}(2\pi) X_{2}'(2\pi) - X_{1}'(0)X_{2}(0) + X_{1}(0)X_{2}'(0)
$$
From the periodic boundary conditions we have:
$$
X_{1}'(0)X_{2}(0) - X_{1}(0) X_{2}'(0) - X_{1}'(0)X_{2}(0) + X_{1}(0)X_{2}'(0) =0
$$
So, the boundary conditions are symmetric. Let $X$ satisfy the boundary conditions, we have:
$$
\left[ XX' \right] ^{2\pi}_{0} = X(2\pi)X'(2\pi) - X(0)X'(0) = X(0)X'(0) - X(0)X'(0) =0
$$
By the "negative eigenvalue" theorem, we conclude that there are no negative eigenvalues.

Check if $\lambda=0$ is an eigenvalue.
$$
\Theta''=0 \Rightarrow \Theta(\theta) = C+D\theta
$$
From the boundary conditions:
$$
C = C+2\pi D \Rightarrow D=0
$$
This leaves $C$ as an arbitrary variable. Therefore zero is an eigenvalue. The corresponding eigenfunction is any constant.

Check if $\lambda=\beta^{2}>0$
$$
\Theta'' = -\beta^{2}\Theta \Rightarrow \Theta(\theta) = C \cos(\beta\theta) + D \sin(\beta\theta)
$$
From the boundary conditions:
$$
C = C \cos(2\pi \beta) + D \sin(2\pi \beta)
$$
$$
\beta D = -\beta C \sin(2\pi \beta) + \beta D \cos(2\pi \beta)
$$
If $\beta=n$ where $n\in \mathbb{N}$, then $C$ and $D$ can be any arbitrary value. Therefore, there are positive eigenvalues, with $\lambda_{n}=n^{2}$ with the eigenfunctions:
$$
\Theta_{n}(\theta) = A_{n} \cos(n\theta) + B_{n} \sin(n\theta)
$$
Now, look at $R$. With the eigenvalues $n=1, 2, 3, \dots$ we have:
$$
r^{2} R'' + r R' - n^{2} R =0
$$
Look for solutions in the form,
$$
R(r) = r^{\alpha}
$$
Substitute this into the equation, you should find that:
$$
\alpha^{2} = n^{2} \Rightarrow \alpha = \pm n
$$
So the corresponding eigenfunctions are:
$$
R_{n}(r) = C_{n} r^{n} + D_{n} r^{-n}
$$
We require bounded solutions as $r\to \infty$ and so $C_{n}=0$. This means $R_{n}(r)=D_{n}r^{-n}$.

For $\lambda=0$ we have:
$$
R_{0}(r) = C_{0} + D_{0} \ln r
$$
Since $\ln r$ will blow up as $r\to \infty$, we require $D_{0}=0$. Collecting all admissible solutions into an infinite sum,
$$
u(r, \theta) = \frac{1}{2} A_{0} + \sum_{n=1}^{\infty} r^{-n}(A_{n} \cos(n\theta) + B_{n} \sin(n\theta))
$$
Now, use the remaining boundary condition to determine the coefficients. Setting $r=a$ we have:
$$
h(\theta) = \frac{1}{2} A_{0} \sum_{n=1}^{\infty} a^{-n} (A_{n} \cos(n\theta) + B_{n} \sin(n\theta))
$$
Which is identical to the full Fourier series. Thus,
$$
A_{n} = \frac{a^{n}}{\pi} \int_{0}^{2\pi} h(\theta) \cos(n\theta) \, d\theta
$$
$$
B_{n} = \frac{a^{n}}{\pi} \int_{0}^{2\pi} h(\theta) \sin(n\theta) \, d\theta
$$
---
$$
\begin{cases}
X'' + \lambda X=0 & x \in(0, l) \\
X(0)=0 & X'(l)+ X(l)=0
\end{cases}
$$
Check for $\lambda=0$. Then,
$$
X''=0 \Rightarrow X(x) = C+Dx
$$
From the boundary conditions:
$$
X(0) = C=0
$$
$$
X'(l) + X(l) = D+Dl =0 \Rightarrow D=0
$$
Therefore 0 is not an eigenvalue.

Check for $\lambda<0$. Define $X_{1}$ and $X_{2}$ which satisfy the boundary conditions. We have:
$$
\left[ X_{1}'(x)X_{2}(x) - X_{1}(x) X_{2}'(x) \right] ^{l}_{0} = 0
$$
And therefore the boundary conditions are symmetric. Now, let $X$ satisfy the boundary conditions, we have:
$$
[XX']^{l}_{0} = X(l)X'(l) - X(0)X'(0) = - X^{2}(l) < 0
$$
By "negative eigenvalue" theorem, we have no negative eigenvalues.

Check for $\lambda=\beta^{2}>0$. Then,
$$
X'' = -\beta^{2}X \Rightarrow X(x) = C \cos(\beta x) + D \sin(\beta x)
$$
From the boundary conditions:
$$
X(0) = C =0
$$
$$
X'(l) = X(l) = \beta D \cos(\beta l) + D \sin (\beta l) =0
$$
From which we obtain the relation:
$$
\beta \cos(\beta l) + \sin(\beta l) \Rightarrow \beta =-\tan(\beta l)
$$
![[Pasted image 20250818145954.png]]
Recall that $\tan x$ as asymptotes at $x=k\pi /2$ where $k$ is any odd integer. In our case, this means that the asymptotes appear at:
$$
\beta l = \frac{k\pi}{2} \Rightarrow \beta = \frac{k\pi}{2l}
$$
And so we have a sequence of intersections where $\beta_{n}$ lies within the intervals:
$$
\left( \frac{(2k-1)\pi}{2l}, \frac{(2k+1)\pi}{2l} \right)
$$
The corresponding eigenfunctions are:
$$
X_{n}(x) = \sin(\beta_{n}x)
$$

Are the positive eigenfunctions orthogonal?

Well, we know the boundary conditions are symmetric. Then, by a class theorem, then any two eigenfunctions that correspond to any two distinct eigenvalues are orthogonal.

---
Let $D$ be the spherical shell $D=\{ (x, y, z)\in \mathbb{R}^{3} , 1<r<2 \}$

Solve
$$
\begin{cases}
u_{xx} + u_{yy} + u_{zz} =0 & \text{ in }D \\
u=100 & r=1 \\
\frac{ \partial u }{ \partial r } =-\gamma<0 & r=2
\end{cases}
$$
Where $\gamma$ is a constant. Hint: Try checking for solutions depending on $r$ only.

Following this hint, assume a radial solution, and, from the Laplacian we have:
$$
u_{rr} + \frac{2}{r} u_{r} =0 \Rightarrow (r^{2} u_{r})_{r} =0
$$
Which has the solution:
$$
u = -\frac{C_{1}}{r} + C_{2}
$$
From the boundary conditions:
$$
\begin{cases}
-C_{1}+C_{2} & =100 \\
\frac{C_{1}}{4} & =-\gamma
\end{cases}
$$
Therefore $C_{1}=-4\gamma$ and:
$$
C_{2} = 100 + C_{1} = 100-4\gamma
$$
Conclude that:
$$
u(r) = \frac{4\gamma}{r} + 100 - 4\gamma
$$
---
Solve
$$
\begin{cases}
u_{t} = 5 u_{xx} & x \in \mathbb{R} \\
u(x, 0) = g(x)
\end{cases}
$$
Take the Fourier transform in $x$:
$$
\hat{u}_{t} (k, t) = 5(ik)^{2} \hat{u} (k, t) = -5k^{2} \hat{u}
$$
$$
\hat{u}(k, 0) = \hat{g}(k)
$$
This is an ODE in $t$. The solution is:
$$
\hat{u}(k, t) = A(k) e^{ -5k^{2}t }
$$
And,
$$
\hat{u}(k, 0) = \hat{g}(k) = A(k) e^{ 0 } \Rightarrow A(k) = \hat{g}(k)
$$
Now, use invert FT to find the solution:
$$
u(x, t) = \left( \hat{g}(k) e^{ -5k^{2}t } \right) ^{\vee} = (e^{ -5k^{2}t })^{\vee} * g(k)
$$
This inverse FT is given:
$$
\mathcal{F}^{-1}\{ e^{ -5k^{2}t } \} = \frac{1}{\sqrt{ 4\pi(5t) }} e^{ -x^{2}/4(5t) }
$$
Therefore, from the definition of convolution:
$$
\frac{1}{\sqrt{ 20\pi t }} \int_{-\infty}^{\infty} e^{ -(x-y)^{2}/20t } g(y) \, dy
$$
---
Consider the wave equation in $D\subset \mathbb{R}^{3}$ with boundary condition:
$$
\frac{ \partial u }{ \partial n } + b \frac{ \partial u }{ \partial t } =0
$$
Where $b>0$ is a constant. Define:
$$
E(t) = \frac{1}{2} \iiint_{D} (u^{2}_{t} + c^{2} |\nabla u|^{2}) \, d\vec{x}
$$
What can we conclude about $E$?
$$
E'(t) = \frac{1}{2} \iiint_{D} (2u_{t}u_{tt} + 2c^{2} \nabla u_{t} \cdot \nabla u) \, d\vec{x}
$$
There are a lot of things to write here. I think you use the divergence theorem and Green's identities to simplify it. But you should eventually obtain:
$$
E'(t) = c^{2} \iint_{\partial D} (u_{t}\nabla u)\cdot \vec{n} \, dS = c^{2} \iint_{\partial D} u_{t} \frac{ \partial u }{ \partial n } \, dS
$$
And then, from the boundary condition:
$$
= -bc^{2} \iint_{\partial D} (u_{t})^{2} \, dS \leq 0
$$
And so $E(t)$ is non-increasing.