Fisher 3.1 Questions 1-2
### Questions 1-2
---
1.
Recall the use of the argument principle:
$$
\frac{1}{2\pi} (\Delta \text{arg}(h(z))) = \text{No. zeroes} - \text{No. poles}
$$
By observation, for this function, it is simple to see that there are no poles.

On the interval $0\leq z\leq R$ the function is real valued and non-zero for all values.

On the quarter circle, use the parametrization $z=R e^{ it }$ with $t\in[0, \pi /2]$
$$
f(R e^{ it }) = (R e^{ it })^{2} - R e^{ it } +1 = R^{2} e^{ 2it } \left[ 1 - \frac{1}{R e^{ it }} + \frac{1}{R^{2} e^{ 2it }} \right]
$$
In the limit as $R\to \infty$ this is approximately $R^{2} e^{ 2it }$. Which has $\text{arg}(e^{ 2it })=2t$ and therefore goes from 0 to $\pi$ as $t$ goes from 0 to $\pi /2$.

On the interval $0\leq y\leq R$ with $z=iy$ the function is:
$$
(iy)^{2}-iy+1 = -y^{2}-iy+1
$$
The real and imaginary parts of this function are:
$$
\begin{align}
\mathrm{Re}\{ f(iy) \} & = -y^{2}+1 \\
\mathrm{Im}\{ f(iy) \} & = -y
\end{align}
$$
Which implies that, when $R\to \infty$ $f(iy)$ lies somewhere in the third quadrant, and goes to 1 as $y\to 0$. I suspect that, since $R$ is arbitrarily large, the value of $f$ lies somewhere on the negative real line. And so the change in the argument from there to 1 on the real line is $\pi$.

Based on this assumption, the change in $\text{arg}\{ f(z) \}$ is $\pi+\pi=2\pi$ and so there is just one zero.

---
2.
Given function is
$$
z^{4} - 3z^{2} + 3
$$
This function has no poles, and has no zeroes on the real line.

On the quarter circle, with parametrization $z=R e^{ it }$ we have,
$$
(R e^{ it })^{4} - 3(R e^{ it })^{2}+3 = R^{4} e^{ 4it } \left[ 1 - \frac{3}{R^{2} e^{ 2it }} + \frac{3}{R^{4} e^{ 4it }} \right]
$$
Which, as $R\to \infty$ has the argument approximately equal to $\text{arg}\{ e^{ 4it } \}=4t$. Therefore, as $t$ goes from 0 to $\pi /2$ the change in the argument is $2\pi$.

Now for the line from $0\leq y\leq R$ with the substitution $z=iy$, the function becomes:
$$
(iy)^{4} - 3(iy)^{2} + 3 = y^{4} + 3y+3
$$
Which is an entirely real valued function, one without any zeroes. Therefore by the argument principle we have:
$$
\frac{1}{2\pi} \left[ \Delta \text{arg}\{ f(z) \} \right] = \frac{2\pi}{2\pi} = 1 = \text{No. zeroes} - \text{No. poles} = \text{No. zeroes} -0
$$
I conclude that this function has 1 zero.
