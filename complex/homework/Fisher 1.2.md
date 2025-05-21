### Question 11
$$
\{ z\in \mathbb{C} : |z-(4+i)|=2 \}
$$
### Question 12
In the complex plane, these numbers can be formulated as the the points $(1,0)$ and $(-1,-1)$.

The slope of this line is $1 /2$. Expressing this line as a set of points, I can use the points $p=(0,2)$ and $q=(2,-2)$.
$$
\{ z\in \mathbb{C} : |z-(2i)|=|z-(2-2i)| \}
$$
### Question 13
This is the point $(-3,-1)$ on the complex plane.
$$
\{ z\in \mathbb{C} : |z-(-4-i)|=|z-(-2-i)| \}
$$
### Question 14
This circle will be centred at $2$ and have a radius of $2$
$$
\{ z\in \mathbb{C} : |z-2|=2 \}
$$
### Question 15
$$
\left\{  z\in \mathbb{C} : \left| z-\frac{1}{2}(1+i) \right| =\frac{\sqrt{ 2 }}{2}  \right\}
$$
### Question 17
$$
\mathrm{Re}((-2+i)z+1)
$$
### Question 22
First, show that $z=sw\implies|z+w|=|z|+|w|$

Fix $z,w\in \mathbb{C}$, and $s \in \mathbb{R}$ such that $s>0$. Assume that $z=sw$. Then, we have
$$
|z+w|=|sw+w|=|w(s+1)|=|w|(s+1)=s|w|+|w|=|sw|+|w|=|z|+|w|
$$
As needed

Second, show that $|z+w|=|z|+|w|\implies z=sw$

Fix $z,w\in \mathbb{C}$. Assume that $|z+w|=|z|+|w|$.

Define $z=a+ib$ and $w=c+id$. Taking squares of both sides, we have
$$
\begin{align}
|z+w|^{2} & =|a+ib+c+id|^{2}=a^{2}+b^{2}+c^{2}+d^{2}+2ac+2bd \\
(|z|+|w|)^2 & =(|a+ib|+|c+id|)^2 = a^{2}+b^{2}+c^{2}+d^{2} + 2\sqrt{ (a^{2}+b^{2})(c^{2}+d^{2}) }
\end{align}
$$
Both of these expressions are equal, so, we have:
$$
\begin{align}
a^{2}+b^{2}+c^{2}+d^{2}+2ac+2bd  & = a^{2}+b^{2}+c^{2}+d^{2} + 2\sqrt{ (a^{2}+b^{2})(c^{2}+d^{2}) } \\
2(ac+bd) & =2\sqrt{ (a^{2}+b^{2})(c^{2}+d^{2}) } \\
ac+bd & =\sqrt{ (a^{2}+b^{2})(c^{2}+d^{2}) } \\
(ac+bd)^{2} & =(a^{2}+b^{2})(c^{2}+d^{2})
\end{align}
$$
Expanding both of these expressions
$$
\begin{align}
a^{2}c^{2}+2abcd+b^{2}d^{2}  & = a^{2}c^{2}+a^{2}d^{2}+b^{2}c^{2}+b^{2}d^{2} \\
2abcd & = a^{2}d^{2}+b^{2}c^{2}
\end{align}
$$
Which in the factor-able expression
$$
\begin{align}
a^{2}d^{2}-2abcd+b^{2}c^{2} & =0 \\
(bc-ad)^{2} & =0 \\
bc-ad & =0 \\
ad-bc & =0
\end{align}
$$
This is equivalent to the determinant
$$
\begin{vmatrix}
a & c \\
b & d
\end{vmatrix}=0
$$
Which implies that the two vectors $(a, b)$ and $(c, d)$ are linearly dependent of each other, and therefore, for some $s \in \mathbb{R}$ we have
$$
\begin{bmatrix}
a \\
b
\end{bmatrix} = s\begin{bmatrix}
c \\
d
\end{bmatrix} \Rightarrow (a+ib)=s(c+id) \Rightarrow z=sw
$$
As needed.
### Question 23
In polar coordinates:
$$
z^5=e^{ i\pi/2 }
$$
Therefore, we have
$$
z=e^{ i\pi/10 }
$$
This can be expressed more generally in the form
$$
z=e^{ i\theta }
$$
Where $\theta=\frac{1}{5}\left( \frac{\pi}{2}+2\pi k \right)$ where $k\in \mathbb{N}$
### Question 24
$$
1-i=\sqrt{ 2 }e^{ -i\pi/4 }
$$
Computing
$$
(z+1)=2^{1/8}e^{ -i(\pi/16+2\pi k/4) }\Rightarrow z=2^{1/8}e^{ -i(\pi/16+2\pi k/4) }-1
$$
Where $k\in \mathbb{N}$
### Question 25
$$
-1=e^{ i\pi }
$$
Compute
$$
z=e^{ i(\pi/8+2\pi k/8) } \equiv e^{ i\theta }
$$
Where $\theta=\frac{1}{8}(\pi+2\pi k)$ and $k\in \mathbb{N}$
### Question 26
$$
z=8^{1/3}=2
$$
