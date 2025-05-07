### Complex Algebra
A *complex number* is defined as any $z$ such that $z = x+iy$ where $i^2=-1$

Define some operations:

$\mathrm{Re}(z)=\frac{z+\bar{z}}{2}=x$
$\mathrm{Im}(z)=\frac{z-\bar{z}}{2}=y$
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
- REMEMBER TO ADD AN IMAGE HERE

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
