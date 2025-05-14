### Complex Algebra
A *complex number* is defined as any $z$ such that $z = x+iy$ where $i^2=-1$

Define some operations:

$\mathrm{Re}(z)=\frac{z+\bar{z}}{2}=x$
$\mathrm{Im}(z)=\frac{z-\bar{z}}{2i}=y$
$z+w = x+iy + u+iv = (u+v)+i(y+v)$
$zw=(x+iy)(u+iv)=xu+iyu+ixv+iiyv=(xu-yv)+i(yu+xv)$
$\frac{z}{w}=\frac{x+iy}{u+iv}=\frac{(xu+yv)+i(yu-xv)}{u^2+v^2}$

- It's pretty intuitive

Recall: the *complex conjugate* of a complex number $z=x+iy$ is another complex number $z^*=\bar{z}=x-iy$

Properties of conjugates:
$$
\begin{align}
\overline{z+w}=\bar{z}+\bar{w} &  & \overline{zw}=\bar{z}\bar{w} &  & \overline{\left( \frac{z}{w} \right)}=\frac{\bar{z}}{\bar{w}}
\end{align}
$$
### Complex plane
- Complex number are represented on a 2-D cartesian plane
	- $\mathbb{C}$ can be imagined as a 2-D vector space over $\mathbb{R}$
	- You can write vector and matrix analogs for complex numbers and complex operations
- Where we have $x+iy \equiv (x, y)$
![[Pasted image 20250512214558.png]]

It is easier to define multiplication if we use the polar plane, instead of the cartesian plane. In this case the magnitude of a complex number is the radius $r$, and it has an angle to the real-axis, $\theta$
- $z=x+iy=r(\cos \theta+i\sin \theta)$
	- $r=|z|$ is often called the absolute value, length, or modulus
	- $\theta=arg(z)$ is often called the argument or angle

Algebra in the complex plane
- $\begin{bmatrix}x \\ y\end{bmatrix} + \begin{bmatrix}u \\ v\end{bmatrix} = \begin{bmatrix}x+u \\ y+v\end{bmatrix}$
- $\overline{\begin{bmatrix}x \\ y\end{bmatrix}}=\begin{bmatrix}x \\ -y\end{bmatrix}$
	- Physically, this is a reflection over the real-axis
- $zw=r(\cos \theta+i\sin \theta)s(\cos \phi+i\sin \phi)=rs(\cos(\theta+\phi)+i\sin(\theta+\phi))$
	- Notice, after multiplication, the final angle is the sum of the previous two

Swapping between the cartesian and polar representations
- $x=r\cos \theta$
- $y=r\sin \theta$

- $\theta=\arctan\left( \frac{y}{x} \right)$ if $z\neq 0$
	- $sign(y)\cdot \frac{\pi}{2}$ if $z=0$ and $y\neq 0$
- $r^2=|z|^2=x^2+y^2=z\bar{z}$

Roots
- $(\cos \theta+i\sin \theta)^n=\cos(n\theta)+i\sin (n\theta)$
- When you take the square root of a complex number, you get two valid results, $\theta/2$ and $\theta/2+\pi$
	- You get even more if you go up to $n$ roots
	- $(\theta+2\pi k)/n$ where $n$ is the degree of the root, and $k\in \left\{ 1, 2, \dots , n-1 \right\}$
### Euler's Identity
Definition for $\theta\in \mathbb{R}$
$$
e^{ i\theta } = \cos \theta + i \sin \theta
$$
Without any proof we will define, for $x, y\in \mathbb{R}$
$$
e^{ x+iy } = e^{ x }e^{ iy } = e^{ x }(\cos y + i \sin y)
$$
Common values
$$
\begin{align}
e^{ \pi i} & = \cos \pi + i\sin \pi = -1 \\
e^{ 2\pi i } & = \cos 2\pi + i \sin 2\pi = 1 \\
e^{ \pi i/2 }  &  = \cos \frac{\pi}{2} + i \sin \frac{\pi}{2} = i
\end{align}
$$
Properties
$$
\begin{align}
\left| e^{ i\theta } \right|  & = 1 \\
e^{ z+w }  & = e^{ z }e^{ w } & , \text{ for }z,w\in \mathbb{C} \\
\overline{e^{ z }}  & = e^{ \bar{z} } \\
|e^{ x+iy }|  = |e^{ x }||e^{ iy }|  & = |e^{ x }| = e^{ x }
\end{align}
$$
### Logarithms
Definition
$$
e^{ z }=w \Rightarrow \ln(w)=z
$$
Lets define some $w\in \mathbb{C}$ where $z = x+iy$
$$
w = e^{ z } = e^{ x }e^{ iy } = e^{ x }(\cos y + i \sin y)
$$
Then, we can see that
$$
e^{ x } = |w| = \sqrt{ w\bar{w} }
$$
Which gives us the properties
$$
\begin{align}
x & =\log|w| \\
y & = \arg(w)
\end{align}
$$
And so,
$$
\log (w) = z = \log|w| + i \arg(w)
$$
However, in this case, $\theta$ is not unique, we can add any arbitrary number of $2\pi$ and it'll remain valid. This can be more easily seen in the example
$$
w = re^{ i\theta }\Rightarrow \log(w) = \log(r) + i\theta
$$
We do not have the resources to solve this issue, instead we will make a choice for what $\theta$ to use. This is called choosing a *branch*
- Eg: in this case, we would be choosing a branch of log
- Otherwise, you would claim that the log of a complex number results in a set of numbers
The typical logarithm properties apply, but instead, the equivalence is stated for an infinite set of numbers, as opposed to just one
$$
\begin{align}
\log(zw) & = \log z + \log w \\
\overline{\log z}  & = \log \bar{z}
\end{align}
$$
### Trig Functions
For $\theta\in \mathbb{R}$, we have,
$$
\begin{align}
\cos \theta  & = \frac{1}{2}(e^{ i\theta } + e^{ -i\theta }) = \mathrm{Re}(e^{ i\theta }) \\
\sin \theta  & = \frac{1}{2i}(e^{ i\theta } - e^{ -i\theta }) = \mathrm{Im}(e^{ i\theta })
\end{align}
$$
- Typical trig identities hold for all complex numbers

Hyperbolic trig functions
$$
\begin{align}
\cosh  & = \frac{1}{2} (e^{ z } + e^{ -z })  \\
\sinh  & = \frac{1}{2} (e^{ z } - e^{ -z })
\end{align}
$$
### Inequalities
$$
\begin{align}
-|z| \leq \mathrm{Re}(z) \leq |z| &  & -|z| \leq \mathrm{Im}(z) \leq |z|
\end{align}
$$
Triangle inequality still holds
$$
|z_{1}+z_{2}+\dots+z_{n}| \leq |z_{1}| + |z_{2}| +\dots+ |z_{n}|
$$
Also
$$
|z|-|w| \leq |z-w|
$$
### Circles and Lines
Write a line as the set of values
$$
\{ z : |z-c| = |z-q| \}
$$
Where $p,q$ are two points on a cartesian plane. This line is defined by claiming: "All points that are the same distance from $p$ and $q$"

Furthermore, write a circle as
$$
\{ z : |z-c| = r \}
$$
Which defines a circle centred at the point $c$, with radius $r$

The equation for a line can be manipulated to transform it into an equation for a circle, it looks like this
$$
\{ z : |z-p| = \lambda|z-q| \}
$$
- We'll come back to this later
### Stereographic projection
Identify the complex plane as a sphere instead of a plane. By convention, we ignore the north pole
- $0\in \mathbb{C}$ corresponds to the south pole
