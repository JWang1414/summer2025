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
---
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
---
Example
$$
\begin{cases}
u_{t}=ku_{xx},  & 0<x<l, t>0 \\
u_{x}(0,t) = u_{x}(l,t)=0,  & t>0 \\
u(x,0)=x,  & 0<x<l
\end{cases}
$$
We have done the separation of variables for this already, the solution is of the form
$$
u(x, t) = \frac{1}{2}A_{0} + \sum_{n=1}^{\infty} A_{n}\exp \left[ -\frac{n^{2}\pi^{2}kt}{l^{2}} \right] \cos\left( \frac{n\pi x}{l} \right)
$$
We can solve for the values of $A_{n}$ with:
$$
A_{n} = \frac{2}{l} \int_{0}^{l} \phi(x)\cos\left( \frac{n\pi x}{l} \right) \, dx
$$
For $n=0$
$$
A_{0} = \frac{2}{l} \int_{0}^{l} x \, dx =l
$$
For $n\geq_{1}$
$$
\begin{align}
A_{n} & =\frac{2}{l} \int_{0}^{l} x \cos\left( \frac{n\pi x}{l} \right) \, dx  \\
 & = \frac{2l}{n^{2}\pi^{2}} \left[ \cos(n\pi)-1 \right]  \\
 & = \begin{cases}
0,  & n \text{ is even} \\
-\frac{4l}{n^{2}\pi^{2}},  & n \text{ is odd}
\end{cases}
\end{align}
$$
Therefore,
$$
u(x, t) = \frac{l}{2} + \sum_{n\text{ is odd}} -\frac{4l}{n^{2}\pi^{2}} \exp \left[ -\frac{n^{2}\pi^{2}kt}{l^{2}} \right] \cos\left( \frac{n\pi x}{l} \right)
$$
---
Example
$$
\begin{cases}
u_{t}=ku_{xx},  & 0<x<l, t>0 \\
u_{x}(0,t)=u_{x}(l,t)=0, l>0 \\
u(x,0)=4+2\cos\left( \frac{3\pi x}{l} \right),  & 0<x<l
\end{cases}
$$
The solution for this one is the same as the previous sample. The coefficients are:
$$
\begin{align}
A_{0}  & = \frac{2}{l} \int_{0}^{l} \left[ 4+2\cos\left( \frac{3\pi x}{l} \right) \right]  \, dx  \\
 & = \frac{2}{l} \left[ 4x+2 \frac{l}{3\pi} \sin\left( \frac{3\pi x}{l} \right) \right] ^l_{0} \\
 & = 8
\end{align}
$$
And,
$$
\begin{align}
A_{n} & = \frac{2}{l} \int_{0}^{l} \left( 4+2\cos\left( \frac{3\pi x}{l} \right) \right)\cos\left( \frac{n\pi x}{l} \right) \, dx  \\
 & = \frac{8}{l} \int_{0}^{l} \cos\left( \frac{n\pi x}{l} \right) \, dx + \frac{4}{l} \int_{0}^{l} \cos\left( \frac{3\pi x}{l} \right)\cos\left( \frac{n\pi x}{l} \right) \, dx  \\
 & = 0 + \frac{4}{l} \frac{l}{2} \\
 & = 2
\end{align}
$$
Where we have used the orthogonality equation in step 2-3. This value is only valid for $n=3$
$$
A_{n} = \begin{cases}
8,  & n=0 \\
2,  & n=3 \\
0,  & \text{otherwise}
\end{cases}
$$
Therefore the full series is
$$
u(x, t) = 4 + 2\exp \left[ -\frac{3^{2}\pi^{2}kt}{l^{2}} \right]  \cos\left( \frac{3\pi x}{l} \right)
$$
---
### Mixed Boundary Conditions
$$
\begin{cases}
u_{t}=ku_{xx},  & 0<x<l, t>0 \\
u(0,t)=0, u_{x}(l,t)=0,  & t>0 \\
u(x,0)=\phi(x),  & 0<x<l
\end{cases}
$$
We have to go through the separation of variables routine for this. Define $u(x, t) = X(x)T(t)$
$$
X(x)T'(t) = kX''(x)T(t)
$$
Which gives us the equations
$$
\begin{align}
X''+\lambda X=0 \\
T'+\lambda kT=0
\end{align}
$$
Where $\lambda$ is a constant (and the eigenvalue). By the boundary conditions: $X(0)T(t)=X'(l)T(t)=0$. Which gives us the relation
$$
X(0)=X'(l)=0
$$
Case 1: Check for $\lambda=0$
$$
X''+\lambda X=X''=0\Rightarrow X(x)=C+Dx
$$
For some constants $C$ and $D$. The results in:
$$
\begin{align}
X(0)=C=0 &  & X'(l)=D=0
\end{align}
$$
And so zero is not an eigenvalue

Case 2: Check for $\lambda=-\gamma^{2}<0$
$$
X''=\gamma^{2}X \Rightarrow X(x) = C\cosh(\gamma x) + D\sinh(\gamma x)
$$
Therefore,
$$
\begin{align}
X(0)=C=0 & \Rightarrow X(x)=D\sinh(\gamma x) \\
X'(x)=\gamma D\cosh(\gamma x) & \Rightarrow X'(l)=\gamma D\cosh(\gamma l)=0
\end{align}
$$
This ultimately implies that $C=D=0$. So there are no negative eigenvalues.

Case 3: Check for $\lambda=\beta^{2}>0$
$$
X''+\beta^{2}X\Rightarrow X''=-\beta^{2}X
$$
Which has the solution
$$
X(x) = C\cos(\beta x) + D\sin(\beta x)
$$
Calculate the derivative for convenience
$$
X'(x) = -C\beta \sin(\beta x) + \beta D\cos(\beta x)
$$
Use the initial conditions to limit options
$$
\begin{align}
X(0)=C=0 &  & X'(l) = \beta D\cos(\beta l)=0
\end{align}
$$
We require the cosine to be zero.
$$
\beta l = \left( n+\frac{1}{2} \right)\pi
$$
For $n \in \mathbb{N}$

The eigenvalues and eigenfunctions are therefore
$$
\begin{align}
\lambda_{n} = \left( \frac{(n+1 /2)\pi}{l} \right)^{2} &  & X_{n}(x) = \sin\left( \frac{(n+1 /2)\pi x}{l} \right)
\end{align}
$$
For the temporal part, we have to solve the problem:
$$
T'+k\lambda T=0\Rightarrow T_{n}(t) = A_{n}\exp \left[ -\frac{(n+1 /2)^{2}\pi^{2}kt}{l^{2}} \right]
$$
The full solution is
$$
u(x, t) = \sum_{n=0}^{\infty} A_{n}\exp \left[ -\frac{(n+1 /2)^{2}\pi^{2}kt}{l^{2}} \right]  \sin\left(  \frac{(n+1 /2)\pi x}{l} \right)
$$
Solve for the initial conditions
$$
\phi(x) = \sum_{n=0}^{\infty} A_{n}\sin\left( \frac{(n+1 /2)\pi x}{l} \right)
$$
With coefficients
$$
A_{n} = \frac{2}{l} \int_{0}^{l} \phi(x)\sin\left( \frac{(n+1 /2)\pi x}{l} \right) \, dx
$$
### The Robin Boundary Condition
$$
\begin{cases}
-X''=\lambda X \\
X'-a_{0}X=0 & \text{ at }x=0 \\
X'+a_{l}X=0 & \text{ at }x=l
\end{cases}
$$
Where $a_{0}$ and $a_{l}$ are both constants. Experimentally, these constants would just be some relevant number.
- Notice, if $a_{0}=a_{l}=0$, then this reduces to the Neumann boundary conditions

Case 1: Check $\lambda=0$
$$
X''=0\Rightarrow X(x)=Cx+D
$$
And for the two boundary conditions
$$
X'(0)-a_{0}X(0)=C-a_{0}D=0 \Rightarrow C=a_{0}D
$$
The above relationship will be plugged into the next equations:
$$
\begin{align}
X'(l)+a_{0}X(l)=C+a_{l}(Cl+D)=0 \\
a_{0}D+a_{l}(a_{0}Dl+D)=0 \\
a_{0}+a_{l}a_{0}l+a_{l}=0
\end{align}
$$
And so $\lambda=0$ is an eigenvalue iff $a_{0}+a_{l}=-a_{0}a_{l}l$

Case 2: Check $\lambda=-\gamma^{2}<0$
$$
X''=\gamma^{2}X\Rightarrow X(x)=C\cosh(\gamma x)+D\sinh(\gamma x)
$$
Apply boundary conditions:
$$
X'(0)-a_{0}X(0)=\gamma C\sinh 0 + \gamma D \cosh 0 - a_{0}(C \cosh 0 + D \sinh 0) = \gamma D-a_{0}C=0
$$
$$
X'(l) + a_{l}X(l) = \gamma C \sinh(\gamma l) + \gamma D\cosh(\gamma l) + a_{l}(C \cosh(\gamma l) + D\sinh(\gamma l))=0
$$
These two equations tell us
$$
D=\frac{a_{0}}{l}C
$$
And,
$$
\begin{align}
\gamma C \sinh(\gamma l) + a_{0}C \cosh(\gamma l) + a_{l}C \cosh(\gamma l) + \frac{a_{l}a_{0}}{l} C \sinh(\gamma l) & =0 \\
\sinh(\gamma l)\left( \gamma+\frac{a_{0}a_{l}}{l} \right) + \cosh(\gamma l)(a_{0}+a_{l}) & =0
\end{align}
$$
Which can eventually be simplified into
$$
\tanh(\gamma l) = -\frac{(a_{0}+a_{l})\gamma}{\gamma^{2}+a_{0}a_{l}}
$$
So, we can obtain $\gamma$ by solving this relationship. However, this is incredibly challenging to solve analytically. There are two common approaches: computational approximations, and graph analysis. Unfortunately, this shows up often in Robin condition problems.

---
Example:
Consider the Robin eigenvalue problem.

If $a_{0}<0$, $a_{l}<0$ and $-a_{0}-a_{l}<a_{0}a_{l}l$, show that there are two negative eigenvalues

Look for intersections of the graph on each of the tangent function above for $\gamma>0$

Define,
$$
\begin{align}
y(\gamma) = -\frac{(a_{0}+a_{l})\gamma}{\gamma^{2}+a_{0}a_{l}} &  & f(l) = \tanh(\gamma l)
\end{align}
$$
INSERT IMAGES HERE!!

How do we know these are the intersections?
$$
y'(l) = -\frac{(a_{0}+al)(a_{0}a_{l}-\gamma^{2})}{(a_{0}a_{l}+\gamma^{2})^{2}}
$$
Notice that $y'$ vanishes at $\gamma=\sqrt{ a_{0}a_{l} }$ and $y(\sqrt{ a_{0}a_{l} })=-\frac{(a_{0}+al)}{2\sqrt{ a_{0}a_{l} }}$. Since $a_{0}$ and $a_{l}$ are both negative, we can re-write this as:
$$
y(\sqrt{ a_{0}a_{l} }) = \frac{|a_{0}|+|a_{l}|}{2\sqrt{ |a_{0}||a_{l}| }}
$$
Use the inequality $a^{2}+b^{2}\geq 2ab$, which gives us
$$
y(\sqrt{ a_{0}a_{l} })\geq \frac{|a_{0}|+|a_{l}|}{|a_{0}|+|a_{l}|}=1
$$
Furthermore, the $\tanh$ function is always less than 1 for $\gamma \in[0, \infty)$. Which we use to conclude there is a point such that $y$ is greater than $f$

Now,
$$
f'(0)=l\sinh ^{2}(0)=l> -\frac{a_{0}+a_{l}}{a_{0}a_{l}}
$$
And,
$$
y'(0) = -\frac{a_{0}+a_{l}}{a_{0}a_{l}}
$$
Therefore, on the interval $(0,\sqrt{ a_{0}a_{l} })$ we have had at least one swap between the two functions.

Now, furthermore, note that $\lim_{ \gamma \to \infty }f(\gamma)=1$ and $\lim_{ \gamma \to \infty }y(\gamma)=0$. So, in the interval $(\sqrt{ a_{0}a_{l} }, \infty)$ there is another crossing point, or intersection

These two swaps are the eigenvalues we need. We can denote them $\gamma_{1}$ and $\gamma_{2}$

Conclusion: we have the two negative eigenvalues $-\gamma_{1}^{2}$ and $-\gamma_{2}^{2}$

---
Example: What about a simple example with positive eigenvalues?
$$
\begin{cases}
-X''=\lambda X \\
X(0)=0 \\
X(1)+X'(1)=0
\end{cases}
$$
- The third condition here is indicative of a Robin problem

Check for positive eigenvalues $\lambda=\beta^{2}$
$$
X''=-\beta^{2}X\Rightarrow X(x) = C\cos(\beta x) + D\sin(\beta x)
$$
Use the given conditions:
$$
X(0)=C=0\Rightarrow X(x)=D\sin(\beta x)
$$
$$
X(1)+X'(1)=D\sin(\beta)+\beta D\cos(\beta)=0
$$
Which gives us
$$
\sin \beta+\beta \cos \beta=0\Rightarrow \beta=-\tan \beta
$$
- This problem looks simple, but is still incredibly challenging to solve

Well, if we imagine the linear function $\beta$, and the function $-\tan \beta$, then we can see that there is an endless number of intersections. Hence, there is a sequence of eigenvalues $\lambda_{n}=\beta_{n}^{2}$ where $n \in \mathbb{N}$