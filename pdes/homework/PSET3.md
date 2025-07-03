### Question 1
Define $y=x-at$. Now, to express the PDE in terms of $u(y, t)$, I will apply the chain rule to the relevant derivatives:
$$
\begin{align}
u_{x} & = \frac{ \partial u }{ \partial y } \frac{ \partial y }{ \partial x } = u_{y} \frac{ \partial  }{ \partial x } (x-at) = u_{y} \\
u_{t} & = \frac{ \partial u }{ \partial y } \frac{ \partial y }{ \partial t } = u_{y} \frac{ \partial  }{ \partial t } (x-at) = -au_{y}
\end{align}
$$
With the newly acquired quantity $u_{x}=u_{y}$, I can also conclude:
$$
u_{xx} = \frac{ \partial u_{x} }{ \partial y } \frac{ \partial y }{ \partial x } = \frac{ \partial  }{ \partial y } u_{y} \frac{ \partial  }{ \partial x } (x-at) = u_{yy}
$$
The new PDE is:
$$
u_{t} - u_{xx} + au_{x} = (-au_{y}) - (u_{yy}) + a(u_{y}) = au_{y} - au_{y} - u_{yy} = -u_{yy} = 0
$$
The problem has now been simplified to:
$$
u_{yy}=0
$$
Which has the solution
$$
u(y, t) = F(t)y + G(t) \implies u(x, t) = F(t)(x-at) + G(t)
$$
Where $F$ and $G$ are two arbitrary functions of $t$. The initial conditions require:
$$
u(x, 0) = F(0)x+G(0)
$$
### Question 2
From the given equation:
$$
\begin{align}
c=3 &  & f(x, t) = t \sin x &  & \phi(x) = e^{ x } &  & \psi(x)=x
\end{align}
$$
Recall:
$$
u(x, t) = \frac{1}{2}\left[ \phi(x+ct)+\phi(x-ct) \right]  + \frac{1}{2c} \int_{x-ct}^{x+ct} \psi(y) \, dy + \frac{1}{2c}\iint_{D} f(y, s) \, dyds
$$
Compute first part:
$$
\frac{1}{2} \left[ \phi(x+ct) + \phi(x-ct) \right] = \frac{1}{2} \left[ e^{ x+ct } + e^{ x-ct } \right] = e^{ x } \frac{e^{ ct } + e^{ -ct }}{2} = e^{ x } = e^{ x } \cosh(ct)
$$
Compute second part:
$$
\begin{align}
\int_{x-ct}^{x+ct} \psi(y) \, dy & = \int_{x-ct}^{x+ct} y \, dy = \frac{1}{2} \left[ y^{2} \right] ^{x+ct}_{x-ct} \\
 & = \frac{1}{2} \left[ (x+ct)^{2}-(x-ct)^{2} \right] = \frac{1}{2}(4ctx) \\
 & = 2ctx
\end{align}
$$
$$
\frac{1}{2c} \int_{x-ct}^{x+ct} \psi(y) \, dy = \frac{1}{2c}(2ctx) = tx
$$
Compute the third part:
$$
\begin{align}
\iint_{D} f(y, s) \, dyds  & = \int_{0}^{t} \int_{x-c(t-s)}^{x+c(t-s)} f(y, s) \, dy  \, ds \\
 & = \int_{0}^{t} \int_{x-c(t-s)}^{x+c(t-s)} s \sin y \, dy \, ds  \\
 & = -\int_{0}^{t} s \left[ \cos y \right] ^{x+c(t-s)}_{x-c(t-s)} \, ds  \\
 & = - \int_{0}^{t} s\left[ -2\sin x \sin(c(t-s)) \right]  \, ds  \\
 & = 2 \sin x \int_{0}^{t} s \sin(c(t-s)) \, ds  \\
 & = \frac{2}{c^{2}} \sin x \left[ cs \cos(c(t-s)) - \sin(c(s-t)) \right] ^t_{0} \\
 & = \frac{2}{c^{2}} \sin x (ct-\sin(ct))
\end{align}
$$
$$
\frac{1}{2c}\iint_{D} f(y, s) \, dyds = \frac{1}{2c}\frac{2}{c^{2}} \sin x (ct-\sin(ct)) = \frac{\sin x}{c^{3}} (ct-\sin (ct))
$$
Sub back into original equation:
$$
\begin{align}
u(x, t)  & = e^{ x }\cosh(ct) + \frac{1}{2c}(2ctx) + \frac{1}{2c} \frac{2}{c^{2}} \sin x (ct-\sin(ct)) \\
& = e^{ x }\cosh(ct) + tx + \frac{\sin x}{c^{3}} (ct-\sin (ct)) \\
 & = e^{ x }\cosh(3t) + 3x + \frac{\sin x}{27} (3t-\sin(3t))
\end{align}
$$
### Question 3
Define a new function $v(x, t) = u(x, t) - (t^{2}+\sin t)$. This problem is transformed into:
$$
\begin{cases}
v_{t} - kv_{xx} = 0 & 0<x<\infty, t>0 \\
v(x, 0) = e^{ -x }  & 0<x<\infty \\
v(0, t) = 0 & t>0
\end{cases}
$$
This is now a homogeneous problem on the half-line. Which has the known solution:
$$
\begin{align}
v(x,t) & =\int_{0}^{\infty} \left[ S(x-y, t)-S(x+y, t) \right] \phi(y) \, dy \\
 & =\frac{1}{\sqrt{ 4\pi kt }} \int_{0}^{\infty} \left[ \exp\left( -\frac{(x-y)^{2}}{4kt} \right)-\exp\left( -\frac{(x+y)^{2}}{4kt} \right) \right] e^{ -y }  \, dy \\
 & = \frac{1}{\sqrt{ 4\pi kt }} \left[ \int_{0}^{\infty} \exp \left( -y-\frac{(x-y)^{2}}{4kt} \right)  \, dy - \int_{0}^{\infty} \exp \left( -y-\frac{(x+y)^{2}}{4kt} \right)  \, dy  \right] 
\end{align}
$$
The solution to both of these integrals is:
$$
\begin{align}
\int_{0}^{\infty} \exp \left[ -y-\frac{(x-y)^{2}}{4kt} \right]  \, dy  & = \sqrt{ \pi kt }e^{ kt-x } \\
\int_{0}^{\infty} \exp \left[ -y-\frac{(x+y)^{2}}{4kt} \right]  \, dy  & = \sqrt{ \pi kt }e^{ kt+x }
\end{align}
$$
Therefore,
$$
v(x, t) = \frac{1}{\sqrt{ 4\pi kt }} \left[ \sqrt{ \pi kt }e^{ kt-x } - \sqrt{ \pi kt }e^{ kt+x } \right] = -e^{ kt } \sinh x
$$
Since $v$ is defined relative to $u$, I can solve for $u$ and find:
$$
u(x, t) = v(x, t) + t^{2}+\sin t = t^{2}+\sin t - e^{ kt }\sinh x
$$
### Question 4
This is a homogeneous Dirichlet condition for the wave equation. The solutions follow the form:
$$
u(x, t) = \sum_{n=1}^{\infty} \left[ A_{n} \cos\left( \frac{n\pi ct}{l} \right) + B_{n} \sin \left( \frac{n\pi ct}{l} \right) \right] \sin\left( \frac{n\pi x}{l} \right)
$$
And the initial conditions can be represented as:
$$
\begin{align}
u(x, 0) = \phi(x) = \sum_{n=1}^{\infty} A_{n} \sin\left( \frac{n\pi x}{l} \right) &  & u_{t}(x,0)=\psi(x)=\sum_{n=1}^{\infty} \frac{n\pi c}{l} B_{n} \sin\left( \frac{n\pi x}{l} \right)
\end{align}
$$
The coefficients follow the form:
$$
\begin{align}
A_{n} & = \frac{2}{l} \int_{0}^{l} \phi(x) \sin\left( \frac{n\pi x}{l} \right) \, dx  \\
 & = \frac{2}{2} \int_{0}^{2} x^{2} \sin\left( \frac{n\pi x}{2} \right) \, dx  \\
 & = (n\pi)^{-3}(16n\pi \sin(n\pi) + (16-8n^{2}\pi^{2})\cos(n\pi)-16)
\end{align}
$$
$$
\begin{align}
B_{n} & = \frac{2}{n\pi c} \int_{0}^{l} \psi(x) \sin\left( \frac{n\pi x}{l} \right) \, dx  \\
 & = \frac{2}{n\pi} \int_{0}^{2} x \sin\left( \frac{n\pi x}{2} \right) \, dx  \\
 & = (n\pi)^{-2} (4 \sin(n\pi) - 4n\pi \cos(n\pi))
\end{align}
$$
Since $n$ will always be some natural number, both of these can be simplified into cases:
$$
\begin{align}
A_{n} = \begin{cases}
-\frac{(-1)^{n /2}8}{n\pi} & n \text{ is even} \\
\frac{(-1)^{(n-1) /2}16}{n^{3}\pi^{3}}(n\pi-1) & n \text{ is odd}
\end{cases} &  & B_{n} = \begin{cases}
-\frac{(-1)^{n /2}4}{n\pi} & n \text{ is even} \\
\frac{(-1)^{(n-1) /2}4}{n^{2}\pi^{2}} & n \text{ is odd}
\end{cases}
\end{align}
$$
