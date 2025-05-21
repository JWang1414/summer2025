### Question 1
a.
$$
z+3w=(1+2i)+3(2-i) = 1+2i+6-3i = 7-i
$$
c.
$$
z^2=(1+2i)^2=(1+2i)(1+2i) = 1+2i+2i-4 = -3+4i
$$
e.
$$
\mathrm{Re}(\xi ^{-1}) = \mathrm{Re}\left( \frac{1}{4+3i} \right) = \mathrm{Re}\left( \frac{4-3i}{(4+3i)(4-3i)} \right) = \mathrm{Re}\left( \frac{4-3i}{25} \right) = \frac{4}{25}
$$
g.
$$
\xi^2 + 2\bar{\xi} + 3 = (4+3i)^2 + 2(4-3i) + 3 = 16 + 24i - 9 + 8-6i+3 = 18+18i
$$
### Question 2
Quadratic formula is given by:
$$
\frac{-b\pm \sqrt{ b^2-4ac }}{2a}
$$
a.
We have $a=1$ and $c=36$. $b=0$. The roots are:
$$
\pm \frac{12i}{2} = \pm 6i
$$
c.
$a=5$, $b=4$, $c=1$.
$$
\frac{-4\pm \sqrt{ 4^2-4(5)(1) }}{2(5)} = \frac{-4\pm \sqrt{ -4 }}{10} = -\frac{2}{5} \pm \frac{i}{5}
$$
e.
$$
z^2=2z \Rightarrow z^2-2z=0
$$
We have $a=1$, $b=-2$, $c=0$
$$
\frac{2\pm \sqrt{ 4 }}{2} = 1\pm \frac{2}{2} = 1\pm 1
$$
### Question 3
d.
$$
|x+iy+2| = |x+iy-2| \Rightarrow \sqrt{ (x+2)^2+y^2 } = \sqrt{ (x-2)^2+y^2 } \Rightarrow (x+2)^2 = (x-2)^2
$$
$$
x^2 + 4x + 4 = x^2 - 4x + 4 \Rightarrow 8x=0\Rightarrow x=0
$$
e.
Find the roots of this equation. We have $a=1$, $b=-2$, and $c=-1$
$$
\frac{2\pm \sqrt{ 8 }}{2} = 1\pm \sqrt{ 2 }
$$
This function will be zero for these values of $w$. Therefore, that is the locus
g.
True whenever $\mathrm{Re}(z)=0$, and therefore is composed of a line on the complex axis
### Question 7
The roots of this quadratic can be expressed with the quadratic equation
$$
\frac{-b\pm \sqrt{ b^2-4ac }}{2a} = -\frac{b}{2a} \pm \frac{\sqrt{ b^2-4ac }}{2a}
$$
Notice that the first term $-b / 2a$ is real, and the second term, $\sqrt{ b^2-4ac } / 2a$ is always complex. From this, we can assert that
$$
\overline{-\frac{b}{2a} + \frac{\sqrt{ b^2-4ac }}{2a}} = -\frac{b}{2a} - \frac{\sqrt{ b^2-4ac }}{2a}
$$
And so the two roots are always complex conjugates of each other
### Question 8
Suppose that $z\in \mathbb{C}$ and $z=x+iy$

Right-side
$$
\begin{align}
|z+A|^2 - 2\mathrm{Re}(Az) & = |x+iy+A|^2 - 2\mathrm{Re}(A(x+iy)) \\
 & =x^2+y^2+A^2+2xA - 2\mathrm{Re}(Ax+iAy) \\
 & =|z|^2 + A^2 + 2xA - 2xA = |z|^2 + A^2
\end{align}
$$
Therefore, we have $\mathrm{LS=RS}$, as needed

For the second part, we have $z,B\in \mathbb{C}$. I will write $B=a+ib$

Left-side
$$
\begin{align}
|z|^2 + 2\mathrm{Re}(Bz) & =|z|^2 + 2\mathrm{Re}\left[ (a+ib)(x+iy) \right]  \\
 & =|z|^2 + 2\mathrm{Re}(ax-by+iay+ibx) \\
 & = |z|^2 + 2(ax-by)
\end{align}
$$
Right-side
$$
\begin{align}
|z+\bar{B}|^2 - |B|^2 & = |(x+iy)+(a-ib)|^2 - |B|^2 \\
 & = |z|^2 + |B|^2 + 2(ax-by) - |B|^2 \\
 & =|z|^2 + 2(ax-by)
\end{align}
$$
And so we have $\mathrm{LS=RS}$.
### Question 9
Show that $|z|=1 \implies \frac{1}{z}=\bar{z}$. Note that we can write any arbitrary complex number with magnitude 1 in polar coordinates as:
$$
re^{ i\theta } = |z|e^{ i\theta } = e^{ i\theta }
$$
In this case, we have:
$$
\frac{1}{z} = \frac{1}{e^{ i\theta }} = e^{ -i\theta } = \overline{e^{ i\theta }}
$$
Which is what we wanted to show

Show that $\frac{1}{z}=\bar{z}\implies|z|=1$. Fix $z\in \mathbb{C}$, and express it as an arbitrary complex number in polar coordinates
$$
\frac{1}{z} = \bar{z} \Rightarrow \frac{1}{|z|e^{ i\theta }} = \overline{|z|e^{ i\theta }} \Rightarrow \frac{1}{|z|}e^{ -i\theta } = |z|e^{ -i\theta } \Rightarrow \frac{1}{|z|} = |z| \Rightarrow |z|^2 = 1
$$
Which implies that $|z|=1$, as needed
### Question 11
Left side is
$$
\begin{align}
|z+w|^2 - |z-w|^2 & = |z|^2 + |w|^2 + z\bar{w} + \bar{z}w - \left[ |z|^2 + |w|^2 - z\bar{w} - \bar{z}w \right]  \\
 & =2z\bar{w}+2\bar{z}w = 2(z\bar{w}+\bar{z}w) \\
 & =2\left[ 2(xa+yb) \right]  \\
 & =4(xa+yb)
\end{align}
$$
Right side is
$$
\begin{align}
4\mathrm{Re}(z\bar{w}) & =4\mathrm{Re}((x+iy)(a-ib)) \\
 & =4\mathrm{Re}\left[ xa-ixb+iya+yb \right]  \\
 & = 4(xa+yb)
\end{align}
$$
Therefore, we have $\mathrm{LS=RS}$ and this equality is true.
### Question 17
Fix $z,w\in \mathbb{C}$ such that $w\neq 0$

Define $z=x+iy$ and $w=u+iv$.

Left-side
$$
\begin{align}
\left| \frac{z}{w} \right|  & = \left| \frac{x+iy}{u+iv} \right| = \left| \frac{(x+iy)(u-iv)}{(u+iv)(u-iv)} \right|  \\
 & = \left| \frac{xu+yv-ixv+iyu}{u^{2}+v^{2}} \right|  \\
 & = \frac{1}{u^{2}+v^{2}} \sqrt{ (x^{2}+y^{2})(u^{2}+v^{2}) } \\
 & =\frac{\sqrt{ x^{2}+y^{2} }}{\sqrt{ u^{2}+v^{2} }}
\end{align}
$$
Right-side
$$
\begin{align}
\frac{|z|}{|w|} & = \frac{|x+iy|}{|u+iv|} \\
 & = \frac{\sqrt{ x^{2}+y^{2} }}{\sqrt{ u^{2}+v^{2} }}
\end{align}
$$
$\mathrm{LS=RS}$ as needed.
### Question 19
De Moivre's theorem:
$$
(\cos x+i \sin x)^n=\cos nx+i \sin nx
$$
For any integer $n$ and real number $x$

Recall that:
$$
\sin ^{2}\theta+\cos ^{2}\theta=1
$$
Binomial formula
$$
(x+y)^n = \sum_{k=0}^{n} \begin{pmatrix}
n \\
k
\end{pmatrix}x^{n-k}y^k
$$
Where the binomial coefficient is defined to be
$$
\begin{pmatrix}
n \\
k
\end{pmatrix} = \frac{n!}{k!(n-k)!}
$$
Manipulate de Moivre's theorem to solve for $\cos n\theta$
$$
\cos n\theta = \frac{1}{2}(\cos n\theta+i\sin n\theta+\cos n\theta - i\sin n\theta)
$$
Which can be split into
$$
\frac{1}{2}\left[ (\cos \theta+i\sin \theta)^n + (\cos \theta+i\sin \theta)^{-n} \right]
$$
For one term, this can be expressed as
$$
(\cos \theta+i\sin \theta)^n = \sum_{k=0}^{n} \begin{pmatrix}
n \\
k
\end{pmatrix} \cos^{n-k}\theta (i\sin \theta)^k
$$
