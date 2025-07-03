Exercises: 1-6, 16, 18, 20, 23
### Question 1
---
a.
Definition of differentiation:
$$
\lim_{ h \to 0 } \frac{f(z_{0}+h) - f(z_{0})}{h}
$$
For $\sin z$
$$
\lim_{ h \to 0 } \frac{\sin(z_{0}+h) - \sin z_{0}}{h}
$$
Apply trig identity:
$$
\sin(a+b) = \sin a \cos b + \cos a \sin b
$$
Therefore:
$$
\sin(z_{0}+h) = \sin z_{0}\cos h + \cos z_{0}\sin h
$$
Subbing back in:
$$
\lim_{ h \to 0 } \frac{\sin z_{0} \cos h + \cos z_{0} \sin h - \sin z_{0}}{h} = \lim_{ h \to 0 } \frac{\sin z_{0} \cos h - \sin z_{0}}{h} + \lim_{ h \to 0 } \frac{\cos z_{0} \sin h}{h}
$$
Which can be simplified into:
$$
\sin z_{0} \lim_{ h \to 0 } \frac{\cos h -1}{h} + \cos z_{0} \lim_{ h \to 0 } \frac{\sin h}{h}
$$
These limits converge to well known values:
$$
\begin{align}
\lim_{ h \to 0 } \frac{\cos h -1}{h} = 0 &  & \lim_{ h \to 0 } \frac{\sin h}{h} = 1
\end{align}
$$
So the final expression reduces to $\cos z_{0}$. As needed.
$$
(\sin z)' = \lim_{ h \to 0 } \frac{\sin(z_{0}+h) - \sin z_{0}}{h} = \cos z
$$
---
c.
Recall:
$$
\begin{align}
\sinh z = \frac{e^{ z } - e^{ -z }}{2} &  & \cosh z = \frac{e^{ z } + e^{ -z }}{2}
\end{align}
$$
Therefore:
$$
(\sinh z)' = \lim_{ h \to 0 } \frac{\sinh(z_{0}+h) - \sinh z_{0}}{h} = \lim_{ h \to 0 } \frac{1}{h}\left[ \frac{1}{2}(e^{ z_{0}+h } - e^{ -(z_{0}+h) }) - \frac{1}{2}(e^{ z_{0} } - e^{ -z_{0} }) \right]
$$
Factoring out the 1/2
$$
\lim_{ h \to 0 } \frac{1}{2h} \left[ e^{ z_{0}+h } - e^{ -(z_{0}+h) } - e^{ z_{0} } + e^{ -z_{0} } \right]
$$
Gathering like terms:
$$
\lim_{ h \to 0 } \frac{1}{2h} \left[ e^{ z_{0}+h } - e^{ z_{0} } - e^{ -(z_{0}+h) } + e^{ -z_{0} } \right] = \lim_{ h \to 0 } \frac{1}{2h} \left[ e^{ z_{0} }(e^{ h }-1) + e^{ -z_{0} }(1-e^{ -h }) \right]
$$
Which can be split up into smaller limits:
$$
\frac{1}{2}e^{ z_{0} } \lim_{ h \to 0 } \frac{e^{ h }-1}{h} + \frac{1}{2}e^{ -z_{0} } \lim_{ h \to 0 } \frac{1-e^{ -h }}{h}
$$
Both of these limits converge to 1
$$
(\sinh z)' = \frac{1}{2}e^{ z_{0} } + \frac{1}{2}e^{ -z_{0} } = \cosh z
$$
---
- To be honest this question kind of sucks. I'll do more of it if I feel like it
### Questions 2-6
---
2.
$$
\frac{d}{dz} \left[ z^{2}+10z \right] = 2z+10
$$
---
3.
$$
\frac{d}{dz} \left[ e^{ z^{3}-z } \right] = e^{ z^{3}-z } \frac{d}{dz} \left[ z^{3}-z \right] = e^{ z^{3}-z } \left[ 3z^{2}-1 \right]
$$
---
4.
$$
\frac{d}{dz} \left[ \cos z^{2} \right] ^{3} = 3\left[ \cos z^{2} \right] ^{2} \frac{d}{dz}\left[ \cos z^{2} \right] = 3\left[ \cos z^{2} \right] ^{2} \sin z^{2}(2z) = 6z \sin z^{2} \cos ^{2}z^{2}
$$
---
5.
$$
\frac{d}{dz} (z^{3}+100)^{-4} = -4(z^{3}+100)^{-5} \frac{d}{dz} (z^{3}+100) = -4(z^{3}+100)^{-5} (3z^{2}) = -12z^{2}(z^{3}+100)^{-5}
$$
---
6.
$$
\frac{d}{dz} (\log z)^{3} = 3(\log z)^{2} \frac{d}{dz}\log z = 3(\log z)^{2} \left( \frac{1}{x} \right) = \frac{3}{x} (\log z)^{2}
$$
- This function is valid on the plane minus the negative reals
---
### Question 16
Recall:
$$
\frac{d}{dz} \frac{f(z)}{g(z)} = \frac{f'(z)g(z) - f(z)g'(z)}{(g(z))^{2}}
$$
Now,
$$
\frac{d}{dz}T(z) = \frac{d}{dz} \frac{az+b}{cz+d}
$$
Apply the quotient rule:
$$
T'(z) = \frac{a(cz+d) - (az+b)(c)}{(cz+d)^{2}} = \frac{acz+ad-acz-bc}{(cz+d)^{2}} = \frac{ad-bc}{(cz+d)^{2}}
$$
For $T'(z)=0$, we require $ad-bc=0$, however, from the given condition, this is not possible. Hence, it is never zero.
### Question 18
Recall the Cauchy-Riemann equations:
$$
\begin{align}
u_{x}=v_{y} &  & v_{x}=-u_{y}
\end{align}
$$
Now, I intend to rewrite $h(z)$ in terms of two functions $u(z)$ and $v(z)$, where $u$ is the real part, and $v$ is the complex part. Define $z = x+iy$
$$
h(z) = \bar{z} = x-iy = u(z) + iv(z)
$$
Which implies that
$$
\begin{align}
u(z) = x \\
v(z) = -y
\end{align}
$$
Compute the derivatives:
$$
\begin{align}
u_{x} & =1 &  v_{x} & =0 \\
u_{y} & =0 & v_{y} & =-1
\end{align}
$$
Applying the Cauchy-Riemann equations:
$$
\begin{align}
u_{x}=v_{y}\implies 1=-1 &  & v_{x}=-u_{y}\implies 0=0
\end{align}
$$
The Cauchy-Riemann equations are violated, and so this function is not analytic on any domain.
### Question 20
---
a.
Compute the derivatives of $u$
$$
u_{x} = \frac{ \partial  }{ \partial x } x^{2}-y^{2} = 2x
$$
$$
u_{y} = \frac{ \partial  }{ \partial y } x^{2}-y^{2} = -2y
$$
Use the Cauchy-Riemann equations:
$$
v_{y} = u_{x} = 2x \implies v = \int 2x \, dy = 2x \int dy = 2xy + F(x)
$$
$$
v_{x} = -u_{y} \implies v = -\int u_{y} \, dx = -\int -2y \, dx = 2y \int dx = 2xy + G(y)
$$
Therefore, we conclude that:
$$
v = 2xy+C
$$
Where $C$ is some constant

---
e.
Compute derivatives:
$$
u_{x} = \frac{ \partial  }{ \partial x } \cosh x \cos y = \cos y \frac{d}{dx} \cosh x = \sinh x \cos y
$$
$$
u_{y} = \frac{ \partial  }{ \partial y } \cosh x \cos y = \cosh x \frac{d}{dy} \cos y = \cosh x (-\sin y) = -\cosh x \sin y
$$
Apply Cauchy Riemann equations:
$$
v_{y} = u_{x} \implies v = \int u_{x} \, dy = \int \sinh x \cos y \, dy = \sinh x \int \cos y \, dy = \sinh x \sin y + F(x)
$$
$$
v_{x}=-u_{y} \implies v = -\int u_{y} \, dx = \int \cosh x \sin y \, dx = \sin y \int \cosh x \, dx = \sinh x \sin y + G(y)
$$
I conclude that:
$$
v = \sinh x \sin y + C
$$
Where $C$ is some constant
### Question 23
- Try using the Cauchy-Riemann equations
- Define what it means to have the range of $f$ be a straight line or circle
- After completing that definition, use it to prove that $f'=0$
- I'm not entirely sure how to do it though