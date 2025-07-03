### Question 1
---
a.
Recall:
$$
a^{3}+b^{3}=(a+b)(a^{2}-ab+b^{2})
$$
Factor the original function:
$$
(z-e^{ i\pi/3 }) \frac{z}{(z+1)(z^{2}-z+1)}
$$
Apply the quadratic formula:
$$
z = \frac{-b\pm \sqrt{ b^{2}-4ac }}{2a} = \frac{-(-1)\pm \sqrt{ (-1)^{2}-4(1)(1) }}{2(1)} = \frac{1\pm \sqrt{ -3 }}{2} = \frac{1}{2} \pm i \frac{\sqrt{ 3 }}{2} = e^{ \pm i\pi/3 }
$$
This function cannot be evaluated at $z=-1, e^{ \pm i\pi/3 }$. At the limit, we are greeted with a 0/0 indeterminate form. I will try to use L'Hopital's rule:
$$
\lim_{ z \to e^{ i\pi/3 } } \left[ z-e^{ -i\pi/3 } \right] \frac{z}{z^{3}+1} = \lim_{ z \to e^{ i\pi/3 } } \frac{2z-e^{ i\pi/3 }}{3z^{2}} = \frac{e^{ i\pi/3 }}{3e^{ 2i\pi/3 }}
$$
Simplify:
$$
= \frac{1}{3}e^{ i\pi/3 }e^{ -2i\pi/3 } = \frac{1}{3} e^{ i\pi/3 - 2i\pi/3 } = \frac{1}{3}e^{ -i\pi/3 }
$$
---
b.
Recall Euler's identity:
$$
e^{ in } = \cos n + i \sin n
$$
Apply the limit laws to the original limit:
$$
\lim_{ n \to \infty } e^{ in } = \lim_{ n \to \infty } (\cos n + i \sin n) = \lim_{ n \to \infty } \cos n + i \lim_{ n \to \infty } \sin n
$$
Both $\cos$ and $\sin$ are periodic functions, and so, as $n\to \infty$, their limit DNE. Therefore, I can conclude that as $n\to \infty$, $e^{ in }$ also DNE.

---
c.
Recall:
$$
e^{ x } = \sum_{k=0}^{\infty} \frac{x^k}{k!}
$$
Therefore, we have:
$$
e^{ -1/|z| } = \sum_{k=0}^{\infty} \frac{(-1 /|z|)^k}{k!} = \sum_{k=0}^{\infty} \frac{(-1)^k}{|z|^kk!}
$$
We are interested in the limit of:
$$
\lim_{ z \to 0 } \sum_{k=0}^{\infty} \frac{(-1)^k}{z|z|^kk!}
$$
- I know that the limit of this is zero. The exponential will decay far quicker than a linear function, and so overpower it. But I cannot for the life of me figure out how to show it's true
### Question 2
---
a.
Assume $\lim_{ z \to z_{0} }f(z)=w$ for some $z_{0}, w\in \mathbb{C}$.

WTS $\lim_{ z \to z_{0} }|f(z)|=|w|$

Case 1:
- Both $f(z)$ and $w$ are positive
- This means that $|f(z)|=f(z)$ and $w=|w|$
- In this case, it is trivially true that $\lim_{ z \to z_{0} }|f(z)| = |w|$

Case 2:
- One of $f(z)$ and $w$ is positive, the other is negative
- This cannot happen unless the limit is at zero
- If the limit is at zero, than is it trivial that $\lim_{ z \to z_{0} }f(z)=0\implies \lim_{ z \to z_{0} }|f(z)|=0$

Case 3:
- Both $f(z)$ and $w$ are negative
- Since both are negative, we have: $f(z)=-|f(z)|$ and $w=-|w|$
- Therefore, the limit simplifies into: $\lim_{ z \to z_{0} }-|f(z)|=-|w|\implies \lim_{ z \to z_{0} }|f(z)|=|w|$

In all cases, we have shown:
$$
\lim_{ z \to z_{0} } f(z)=w\implies \lim_{ z \to z_{0} } |f(z)|=|w|
$$
---
b.
A simple example along the real line would be the function:
$$
f(z) = \frac{|z|}{z}
$$
Which jumps from 1 to -1 at $z=0$. The absolute value, however, would always be 1.

A similar complex equivalent would be:
$$
f(z)=\frac{\bar{z}}{z}
$$
Which has the same behaviour along the purely complex line, jumping from 1 to -1
### Question 3
---
a.
$$
\begin{align}
u_{x}=v_{y} &  & v_{x}=-u_{y}
\end{align}
$$
---
b.
Define $z=x+iy$. Then,
$$
f(z)=e^{ (x+iy)^{3} } = \exp \left( x^{3}+i(3x^{2}y-y^{3})-3xy^{2} \right) = \exp \left( x^{3}-3xy^{2} \right) \exp \left( i(3x^{2}y-y^{3}) \right)
$$
Which can be split into the real and complex functions:
$$
\exp \left( x^{3}-3xy^{2} \right) \left[ \cos(3x^{2}y-y^{3}) + i \sin(3x^{2}y-y^{3}) \right]
$$
Compute derivatives:
$$
\begin{align}
u_{x} & = -3\exp \left( x^{3}-3xy^{2} \right) \left[ 2xy \sin(3x^{2}y-y^{3}) + (y^{2}-x^{2}) \cos(3x^{2}y-y^{3}) \right]   \\
u_{y} & =-3\exp \left( x^{3}-3xy^{2} \right) \left[ (y^{2}-x^{2})\sin(y^{3}-3x^{2}y) + 2xy \cos(y^{3}-3x^{2}y) \right] 
\end{align}
$$
- I don't want to write out the other two, the bottom line is that I checked, and they're the same
---
c.
Define $f(z)=z$. Then, $g(z)=f(\bar{z})=\bar{z}$.

If you check, the C-R equations will hold for $f(z)$, but they will not for $g(z)$. Therefore, if $f(z)$ is an analytic function, then $f(\bar{z})$ is not also analytic.
### Question 4
- I did this one on paper
### Question 5
Define $z=x+iy$. Therefore,
$$
f(z) = e^{ -z^{2} } = e^{ -(x+iy)^{2} } = \exp \left( -(x^{2}+2ixy-y^{2}) \right) = \exp \left( -(x^{2}-y^{2}) - i(2xy) \right) 
$$
Which can now be split into the function
$$
e^{ -(x^{2}-y^{2}) }e^{ -i(2xy) } = e^{ y^{2}-x^{2} }\left[ \cos(2xy) - i \sin(2xy) \right]
$$
The range of this function is $\mathbb{C}\setminus \{ 0 \}$

Explanation:

Define $e^{ -z^{2} }=w$ where $w\in \mathbb{C}$. I want to find the possible ways to express $z$ to get any given $w$.

Using algebra:
$$
e^{ -z^{2} }=w\implies-z^{2} = \ln w \implies z = i\sqrt{ \ln w }
$$
The square root function is defined for all $\mathbb{C}$. However, the logarithm is not defined for $w=0$. Hence, there exists no $z$ such that $w=0$.
### Question 6
---
a.
Recall: A function $f(x_{1}, x_{2},\dots) : \mathbb{R}^n\to \mathbb{R}$ is called harmonic if:
$$
\frac{ \partial^{2}f }{ \partial x_{1}^{2} } + \frac{ \partial^{2}f }{ \partial x_{2}^{2} } + \dots + \frac{ \partial^{2}f }{ \partial x^{2}_{n} } =0
$$
Two functions $u, v$ are called harmonic conjugates if they satisfy the Cauchy-Riemann equations

Verify $u$ is harmonic:
$$
\frac{ \partial^{2} }{ \partial x^{2} } (x-2xy) + \frac{ \partial^{2} }{ \partial y^{2} } (x-2xy) = 0-0+0-0=0
$$
The Cauchy-Riemann equations are:
$$
\begin{align}
u_{x}=v_{y} &  & v_{x}=-u_{y}
\end{align}
$$
Solve for $v$:
$$
v = \int u_{x} \, dy = \int \frac{ \partial  }{ \partial x } (x-2xy) \, dy = \int 1-2y \, dy = y-y^{2}+F(x)
$$
$$
v = \int -u_{y} \, dx = -\int \frac{ \partial  }{ \partial y } (x-2xy) \, dx = -\int -2x \, dx = x^{2}+F(y)
$$
I conclude that:
$$
v = x^{2}+y-y^{2}+C
$$
Where $C\in \mathbb{C}$

---
b.
Verify $u$ is harmonic:
$$
\frac{ \partial^{2} }{ \partial x^{2} } \left[ \cos x \sinh y+x \right] + \frac{ \partial^{2} }{ \partial y^{2} } \left[ \cos x \sinh y + x \right] = -\cos x \sinh y + \cos x \sinh y = 0
$$
Compute $v$:
$$
v = \int u_{x} \, dy = \int \frac{ \partial  }{ \partial x } \cos x \sinh y + x \, dy = \int 1-\sin x\sinh y \, dy = y - \sin x \cosh y + F(x)
$$
$$
v = - \int u_{y} \, dx = - \int \frac{ \partial  }{ \partial y } \left[ \cos x\sinh y + x \right]  \, dx = -\int \cos x\cosh y \, dx = -\sin x\cosh y + F(y)
$$
I conclude that:
$$
v = y - \sin x\cosh y + C
$$
Where $C\in \mathbb{C}$
### Question 7
---
a.
Recall that the parametrization of a line between two points $z$ and $w$ is:
$$
\gamma(t) = (1-t)z+tw
$$
With $t\in[0, 1]$

In this case, parametrizing the line from 0 to $2+i$, we have:
$$
\gamma(t) = (1-t)(0) + t(2+i) = (2+i)t
$$
Recall that for a smooth curve, the line integral in the complex plane is:
$$
\int_{\gamma} u(z) \, dz = \int_{a}^{b} u(\gamma(t))\gamma'(t) \, dt
$$
For some function $u(z)$ along the curve $\gamma$.

Compute $\gamma'(t)$
$$
\frac{d}{dt} (2+i)t = 2+i
$$
Compute the integral:
$$
\begin{align}
\int_{0}^{1} \mathrm{Im}\left[ ((2+i)t)^{2} \right] (2+i) \, dt  & = (2+i)\int_{0}^{1} \mathrm{Im}((3+4i)t^{2}) \, dt  \\
 & = (2+i)\int_{0}^{1} 4it^{2} \, dt  \\
 & = 4i(2+i)\int_{0}^{1} t^{2} \, dt  \\
 & = 4(2i-1) \left[ \frac{t^{3}}{3} \right] ^1_{0} \\
 & = \frac{4}{3}(-1+2i)
\end{align}
$$
---
b.
Recall a circle is parametrized by:
$$
\gamma(t) = e^{ it }
$$
Where $t\in[0,2\pi]$

Since we are only interested in the semi-circle passing through $i$ the the parametrization is:
$$
\gamma(t) = e^{ it }
$$
Where $t\in[0,\pi]$. It has derivative:
$$
\gamma'(t) = i e^{ it }
$$
Sub into integral:
$$
\int_{0}^{\pi} \exp \left( e^{ it } \right) (ie^{ it }) \, dt
$$
Express the first exponential as a Taylor series:
$$
i \int_{0}^{\pi} \left( \sum_{k=0}^{\infty} \left( \frac{e^{ ikt }}{k!} \right) \right) e^{ it } \, dt = i \int_{0}^{\pi} \sum_{k=0}^{\infty} \frac{e^{ i(k+1)t }}{k!} \, dt
$$
Swap the summation and integral. The integral on the inside is:
$$
\int_{0}^{\pi} e^{ i(k+1)t } \, dt = \left[ \frac{1}{i(k+1)}e^{ i(k+1)t } \right] ^\pi_{0}
$$
Which is:
$$
\sum_{k=0}^{\infty} \left[ \frac{e^{ i(k+1)t }}{(k+1)!} \right] ^\pi_{0} = \sum_{k=1}^{\infty} \frac{e^{ ik\pi }}{k!} - \sum_{k=1}^{\infty} \frac{1^k}{k!} = \sum_{k=0}^{\infty} \frac{e^{ ik\pi }}{k!} - \frac{e^{ 0 }}{0!} - \sum_{k=0}^{\infty} \frac{1^k}{k!} + \frac{1^0}{0!}
$$
Evaluating,
$$
\exp \left( e^{ i\pi } \right) - 1 - e^{ 1 } + 1 = e^{ -1 } - e
$$
---
c.
For the line from $z$ to $w$. We have $z=i$ and $w=2i$. This line is therefore:
$$
\gamma(t) = (1-t)z + tw = (1-t)(i) + 2it = it+i
$$
Derivative is:
$$
\gamma'(t) = \frac{d}{dt} (it+i) = i
$$
Compute integral:
$$
\int_{0}^{1} |e^{ it+i }+1|^{2}(i) \, dt = i \int_{0}^{1} (e^{ it+i }+1)(e^{ -it-i }+1) \, dt = i \int_{0}^{1} 2(\cos(t+1)+1) \, dt
$$
Simplify,
$$
2i \int_{0}^{1} \cos(t+1)+1 \, dt = 2i(\sin 2 - \sin 1 + 1)
$$
### Question 8
---
a.
Define $f(z)=1$. By Cauchy's formula, we have:
$$
f(a) = \frac{1}{2\pi i} \int_{\gamma} \frac{f(z)}{z-a} \, dz
$$
Using $a=1$, this turns into:
$$
f(1) = \frac{1}{2\pi i} \int _{\gamma} \frac{f(z)}{z-1} \, dz \implies 2\pi if(1) = \int _{\gamma} \frac{f(z)}{z-1} \, dz = \int _{\gamma} \frac{1}{z-1} \, dz
$$
Which is exactly the integral we are trying to solve.
$$
\int _{|z|=2} \frac{dz}{z-1} = 2\pi i
$$
- I have no clue if this is the correct way to do this
- Am I even allowed to apply this theorem for this curve?
---
b.
Simplify the function inside the integral:
$$
\frac{1}{z^{2}+z-2} = \frac{1}{(z+2)(z-1)} = -\frac{1}{3(z+2)} + \frac{1}{3(z-1)}
$$
Therefore, the integral can be re-written:
$$
\int _{\gamma} \frac{1}{z^{2}+z-2} \, dz = \int _{\gamma} \frac{1}{3(z-1)} - \frac{1}{3(z+2)} \, dz  = \int _{\gamma} \frac{1}{3(z-1)} \, dz - \int _{\gamma} \frac{1}{3(z+2)} \, dx
$$
Which can be further simplified into
$$
\frac{1}{3} \int _{\gamma} \frac{1}{z-1} \, dz - \frac{1}{3} \int_{\gamma} \frac{1}{z+2} \, dz
$$
