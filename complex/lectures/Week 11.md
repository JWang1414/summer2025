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
Theorem:
> Linear fractional transformations always send circles and lines to other circles and lines

To develop an intuition, first imagine the case for $c=0$. We effectively have the transformation:
$$
\frac{az+b}{cz+d} = \frac{az+b}{d} = \frac{a}{d}z + \frac{b}{d} = \alpha z + \beta
$$
Which is a transformation that is easy to imagine. the $\alpha$ term scales the given $z$ portion, and the $\beta$ represents a translation. Now the case for $c\neq 0$. We have:
$$
\frac{az+b}{cz+d} = \frac{1}{c} \left[ \frac{acz+ad-ad+bc}{cz+d} \right] = \frac{1}{c} \left( a + \frac{bc-ad}{cz+d} \right)
$$
And so we have now isolated the nasty division term. Tracking the change in the $z$, we can see this is simply a composition of transformations:
$$
z \to cz+d = \omega \to \frac{1}{\omega} = \eta \to \frac{1}{c}(a + (bc-ad)\eta)
$$
The first and third parts of this transformation are just the same as the previous transformation. So we know they send circles to circles and lines to lines.

We are interested in proving that the transformation $\omega \to 1 /\omega$ has the same properties. Lets first consider two simple examples. The circle $R e^{ i\theta }$ and the line $\omega$.

We have:
$$
R e^{ i\theta } \to \frac{1}{R e^{ i\theta }} = \frac{1}{R} e^{ -i\theta }
$$
Which is another circle, just in the opposite orientation. For the line, recall that:
$$
\omega \bar{\omega} = \left| \omega \right| ^{2} \Rightarrow \frac{1}{\omega} = \frac{\bar{\omega}}{|\omega|^{2}}
$$
And so the transformation for the line simply reflects it by taking the complex conjugate.
- You can prove that this transformation has the desired properties, but the proof kind of sucks and doesn't mean anything
### Cross Ratios
Consider three distinct points $z_{2}, x_{3}, x_{4}$ in $\mathbb{C}\cap \{ \infty \}$. Consider:
$$
M : z\to \frac{z-z_{3}}{z-z_{4}} \frac{z_{2}-z_{4}}{z_{2}-z_{3}}
$$
$$
\begin{align}
z_{2} & \to 1 \\
z_{3} & \to 0 \\
z_{4} & \to \infty
\end{align}
$$
If...
$$
\begin{align}
z_{2}=\infty & & \text{use} &   & \frac{z-z_{3}}{z-z_{4}} \\
z_{3}=\infty  & & \text{use} &  & \frac{z_{2}-z_{4}}{z-z_{4}} \\
z_{4}=\infty &  & \text{use} &  & \frac{z-z_{3}}{z_{2}-z_{3}}
\end{align}
$$
Definition:
> Given $z_{1}, z_{2}, z_{3}, z_{4}$ distinct in $\mathbb{C}\cap \{ \infty \}$. Their cross-ratio is
$$
(z_{1}, z_{2}, z_{3}, z_{4}) := Mz_{1} = \frac{z_{1}-z_{3}}{z_{1}-z_{4}} \cdot \frac{z_{2}-z_{4}}{z_{2}-z_{3}}
$$

Theorem:
> If $T$ is a linear fractional transformation, then
$$
(Tz_{1}, Tz_{2}, Tz_{3}, Tz_{4}) = (z_{1}, z_2, z_{3}, z_{4})
$$

Theorem:
> $(z_{1}, z_{2}, z_{3}, z_{4})$ is real $\iff$ All 4 points lie on a circle/line
- Note that this is the exact same as the theorem in the previous section about circles and lines.

$z$ and $z^*$ are *symmetric* with respect to the general circle $C$ through $z_{1}$, $z_{2}$, $z_{3}$. That is:
$$
(z^*, z_{1}, z_{2}, z_{3}) = \overline{(z, z_{1}, z_{2}, z_{3})} = (\bar{z}, \bar{z}_{1}, \bar{z}_{2}, \bar{z}_{3})
$$
What do symmetric points look like geometrically?

Case 1: $C$ is a line

Pick $z_{3}=\infty$ and therefore:
$$
M(z) = \frac{z-z_{2}}{z_{1}-z_{2}}
$$
So,
$$
\frac{z^* -z_{2}}{z_{1}-z_{2}} = \overline{\left( \frac{z-z_{2}}{z_{1}-z_{2}} \right)} = \frac{\bar{z}-\bar{z}_{2}}{\bar{z}_{1}-\bar{z}_{2}}
$$
Take the norm of both:
$$
\left| z^*-z_{2} \right|  = \left| z-\bar{z}_{2} \right|
$$
And so we have $z^*$ and $z$ equidistant from $z_{2}$. Furthermore, taking the imaginary part of both we have:
$$
\mathrm{Im}\left( \frac{z^*-z_{2}}{z_{1}-z_{2}} \right) = \mathrm{Im}\left( \frac{\bar{z}-\bar{z}_{2}}{\bar{z}_{1}-\bar{z}_{2}} \right) = -\mathrm{Im}\left( \frac{z-z_{2}}{z_{1}-z_{2}} \right)
$$
The combination of this result and the previous tells us that $z$ and $z^*$ are equidistant and on opposite side of a line.

Case 2: $C$ is a circle centred at $a$ with radius $R$

We have:
$$
\overline{(z, z_{1}, z_{2}, z_{3})} = (\bar{z}, \bar{z}_{1}, \bar{z}_{2}, \bar{z}_{3}) = (\bar{z}-\bar{a}, \bar{z}_{1}-\bar{a}, \bar{z}_{2}-\bar{a}, \bar{z}_{3}-\bar{a})
$$
Define $z_{i}=R e^{ i\theta_{i} }$. Recall the identity $\bar{\omega} = |\omega|^{2} /\omega$ and therefore we have:
$$
= \left( \bar{z}-\bar{a}, \frac{R^{2}}{z_{1}-a}, \frac{R^{2}}{z_{2}-a}, \frac{R^{2}}{z_{3}-a} \right) = \left( \frac{R^{2}}{\bar{z}-a^{2}}+a, z_{1}, z_{2}, z_{3} \right)
$$
And so we have:
$$
z^* = \frac{R^{2}}{\bar{z}-\bar{a}}+a \implies (z^*-a)(\bar{z}-\bar{a}) = R^{2}
$$
Taking the absolute value of both sides, we obtain:
$$
\left| z^*-a \right| \left| z-z \right|  = R^{2}
$$
And so the product of the distances is $R^{2}$. Which implies that if $z$ is in $C$, then $z^*$ is outside of $C$, and vice versa.

Furthermore,
$$
z^*-a = \frac{R^{2}}{|\bar{z}-\bar{a}|} = \frac{R^{2}}{|\bar{z}-\bar{a}|^{2}} (z-a) \Rightarrow \frac{z^*-a}{z-a} = \frac{R^{2}}{|\bar{z}-\bar{a}|^{2}}
$$
Which tells us that $z^*$ and $z$ lie on the same line going through $a$.

So, imagine a circle centred at a point $a$. Draw a line emanating from this circle. $z$ and $z^*$ will lie on that line.

It is possible to find $z^*$ explicitly on a circle. You can show, using similar triangles, that:
$$
\frac{|z^*-a|}{R} = \frac{R}{|z-a|} \Rightarrow \frac{|z^*-a|}{|z-a|} = R^{2}
$$
