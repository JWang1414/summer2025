A linear fractional transform $T$ is:
$$
T(z) = \frac{az+b}{cz+d}
$$
Where $a,b,c,d\in \mathbb{C}$ and $ad-bc\neq 0$. We can show that $T$ is one-to-one and (almost) onto. The inverse of $T$ is:
$$
T^{-1}(\omega) = \frac{d\omega-b}{-c\omega+a}
$$
Which is only valid if $-c\omega+a\neq 0$ or $\omega \neq a /c$.

Note that:
$$
\lim_{ z \to \infty } T(z) = \frac{a}{c}
$$
And
$$
\lim_{ z \to -d /c } T(z) = \infty
$$
Since $T$ appears to include $\infty$ in its domain, we define $T$ to be a bijection from $\mathbb{C}\cap \{ \infty \}\to \mathbb{C}\cap \{ \infty \}$. In other words, the Riemann sphere to the Riemann sphere
- I suspect that the union symbol here is wrong but I don't have the time to check it rn

The inverse of a linear fractional transform is yet another linear fractional transformation. What about the composition of one? Define the two linear fraction transformations:
$$
S(z) = \frac{\alpha z+\beta}{\gamma z+\delta} \qquad T(z) = \frac{az+b}{cz+d}
$$
Then, we have:
$$
S(T(z)) = \frac{(\alpha a+\beta c)z+(\alpha b+\beta d)}{(\gamma a+\delta c)z+(\gamma b+\delta d)}
$$
Yet another linear fractional transformation.

Linear fractional transformations are not matrices, that is, they do not act upon $\mathbb{C}$ linearly. However, the coefficients can be computed with the use of matrices
$$
M = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix} \qquad M^{-1} = \begin{bmatrix}
d & -b \\
-c & a
\end{bmatrix}
$$
- We assume that the determinant is 1 for linear fractional transformations
Furthermore, the composition of two linear fractional transformations is the matrix multiple:
$$
M_{S}M_{T} = \begin{bmatrix}
a & b \\
c & d
\end{bmatrix} \begin{bmatrix}
\alpha & \beta \\
\gamma & \delta
\end{bmatrix}
$$
### Fixed Points
$$
T(z) = \frac{az+b}{cz+d} = z \Rightarrow cz^{2}+(d-a)z-b=0
$$
And so $T$ fixes $z$ iff $z$ is a root of $cz^{2}+(d-a)z-b=0$. By observation, $T$ has at most 2 fixed points, unless $T(z)=z$ is identity.

The above also shows us that, if $T=S$ at 3 points, then $T=S$ everywhere.

Given 3 points, how can we find the $L$ that sends $z_{i}\to w_{i}$? Define the new transformation:
$$
T(z) = \frac{z-z_{1}}{z-z_{3}} \left( \frac{z_{2}-z_{3}}{z_{2}-z_{1}} \right)
$$
And use:
$$
\begin{align}
T: z_{1} & \to 0 \\
z_{2} & \to 1 \\
z_{3} & \to \infty
\end{align}
$$
Do something similar for:
$$
S(w) = \frac{w-w_{1}}{w-w_{3}} \left( \frac{w_{2}-w_{3}}{w_{2}-w_{1}} \right)
$$
With:
$$
\begin{align}
S:w_{1} & \to 0 \\
w_{2} & \to 1 \\
w_{3} & \to \infty
\end{align}
$$
And now we can find out desired linear transformation:
$$
L(z) = S^{-1}(T(z))
$$
- This is a tedious computation, but it isn't that challenging. This is largely because we have a known equation to invert linear fractional transformations

When finding transforms, notice that if we are given 3 real points being send to 3 real points, the coefficients are all real. In this particular case, we have:
$$
T(\bar{z}) = \frac{a\bar{x}+b}{c\bar{z}+d} = \overline{T(z)}
$$
