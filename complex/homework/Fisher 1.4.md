Assigned Questions: 1-25, 27-28, 31-40
### Questions 1-8
1. Converges to 0
2. Diverges. This is because $|1+i| = \sqrt{ 2 }$, and so the portion in the brackets has magnitude 1. However, because of the complex value it will "spin around" the origin
3. Converges to 0
4. Converges to 0
5. Diverges, because of the linear $n$ term
6. Converges to 0
7. Converges to 0
---
8.
$$
z_{n} = n\left[ 1-\left( \cos\left( \frac{\theta}{n} \right) +i \sin\left( \frac{\theta}{n} \right) \right) \right] = n\left[ 1-e^{ i\theta/n } \right]
$$
We have $\infty \cdot 0$, which is in-determinant. I will use L'Hopital's rule
$$
\frac{1-e^{ i\theta/n }}{1 /n}
$$
The derivative of the top is:
$$
\frac{d}{dn} 1-e^{ i\theta/n } = \frac{d}{dn}1 - \frac{d}{dn}e^{ -i\theta/n } = -e^{ i\theta/n } \frac{d}{dn}\left( \frac{i\theta}{n} \right) = -e^{ i\theta/n } (i\theta)(-n^{2})
$$
The derivative of the bottom is
$$
\frac{d}{dn}n^{-1} = -n^{2}
$$
Therefore, we have:
$$
\lim_{ n \to \infty } z_{n} = \frac{-e^{ i\theta/n }(i\theta)(-n^{2})}{-n^{2}} = -i\theta e^{ i\theta/n }
$$
As $n\to \infty$, $e^{ i\theta/n }$ will approach $e^{ 0 }=1$, and so the final limit is $-i\theta$
### Question 9
Function is continuous and defined at this point.
$$
|1-z_{0}|^{2} = (1-i)(1+i) = 1+1=2
$$
### Question 10
Function is continuous and defined everywhere.
$$
z_{0}=-1=e^{ -i\pi } \implies \arg z=-\pi
$$
Various different arguments, like $-\pi+2k\pi$ where $k\in \mathbb{Z}$ would have worked, but I'm assuming a domain of $0<\theta<2\pi$ here
### Question 11
This function is continuous, but undefined at $\mathrm{Im}z=1$. First, we have:
$$
(1-\mathrm{Im}(8))^{-1} = (1-0)^{-1}=1
$$
Second, we have
$$
(1-\mathrm{Im}\{ 8+i \})^{-1} = (1-1)^{-1} = 0^{-1}
$$
Which is undefined. In this case, the limit DNE
### Question 12
Manipulate the logarithm
$$
(z-2)\log|z-2| = \log \left[ |z-2|^{z-2} \right]
$$
Which, evaluated at $z_{0}=2$ is:
$$
\log(0^0) = \log 1 = 0
$$
### Question 13
$$
\frac{|z|^{2}}{z} = \frac{z\bar{z}}{z} = \bar{z}
$$
Therefore, the limit at $z_{0}=0$ is $\overline{z_{0}}=\bar{0}=0$
### Question 14
$$
\frac{z^{3}-8i}{z+2i} = \frac{z^{3}+(2i)^{3}}{z+2i} = \frac{(z+2i)(z^{2}-2iz-4)}{z+2i} = z^{2}-2iz-4
$$
For this new function:
$$
(-2i)^{2}-2i(-2i)-4 = -12
$$
### Question 15
$$
z^{3}-i^{3} = (z-i)(z^{2}+iz-1)
$$
Therefore,
$$
\frac{z^{3}+i}{z-i} = z^{2}+iz-1
$$
Evaluate at the point $z=i$
$$
z^{2}+iz-1 = i^{2}+ii-1 = -3
$$
Which means that the piece-wise function $f(z)$ is continuous everywhere
### Question 16
$$
(z^4-1) = (z^{2}-1)(z^{2}+1) = (z^{2}-1)(z+i)(z-i)
$$
So,
$$
\frac{z^4-1}{z-i} = (z+i)(z^{2}-1)
$$
Set $z=i$
$$
(i+i)(i^{2}-1) = -4i
$$
I conclude that $f(z)$ is continuous everywhere except $z=i$
### Question 17
Define $z=x+iy$, where $x, y\in \mathbb{R}$. Then, if $x=y$ we have:
$$
(\mathrm{Im}z - \mathrm{Re}z)^{-1} = (y-x)^{-1} = 0^{-1}
$$
I conclude this function is continuous everywhere, except for the line $y=x$ in the complex plane
### Question 18
Discontinuous specifically at $1-|z|^{2}=0$, or $z\bar{z}=1$. This region can be seen as a small circle centred around the origin
### Question 19
Discontinuous at all points on the circle $|z|=1$, except for one point. This point is $z=1$
### Question 20
Continuous everywhere
### Question 21
$$
\lim_{ z \to \infty } f(z) \to \frac{1}{|\infty|} \to 0
$$
### Question 22
$$
\begin{align}
\lim_{ z \to +\infty } \frac{|z|}{z} = 1 &  & \lim_{ z \to -\infty } \frac{|z|}{z}=-1
\end{align}
$$
Limit DNE
### Question 23
$$
g(z) = \frac{4z^6-7z^3}{z^6-12z^4+48z^{2}-64} \implies \lim_{ z \to \infty } =4
$$
### Question 24
Limit DNE. The value of $\arg(z)$ will change depending on the direction of $\infty$. That is, the limit as $z\to-\infty$ is not the same as $z\to +\infty$
