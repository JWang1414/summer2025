Questions 1-15
### Questions 1-6
---
1.
There is a single singularity at $z=0$
$$
\frac{e^{ z }-1}{z} = \frac{1}{z} \left[ \sum_{k=0}^{\infty} \frac{z^{k}}{k!} -1 \right]
$$
The first few terms of the Taylor series for $e^{ z }$ are:
$$
e^{ z } = \sum_{k=0}^{\infty} \frac{z^{k}}{k!} = 1+z+\frac{z^{2}}{2} + \dots
$$
And therefore the full representation of this function can be simplified into:
$$
\frac{1}{z} \sum_{k=1}^{\infty} \frac{z^{k}}{k!} = \sum_{k=1}^{\infty} \frac{z^{k-1}}{k!}
$$
Which has the first few terms:
$$
\frac{z^{0}}{1!} + \frac{z}{2!} + \frac{z^{2}}{3!} + \dots = 1 + 0 + 0 + \dots
$$
I have evaluated this series at $z=0$. This implies that, there is a removable singularity at the point, and the value of the function at this point is 1.

---
3.
Factor this function into:
$$
\frac{z^{4}-2z^{2}+1}{(z-1)^{2}} = \frac{(z-1)^{2}(z+1)^{2}}{(z-1)^{2}} = (z+1)^{2}
$$
I conclude that there is a removable singularity at:
$$
z-1=0 \implies z=1
$$
Where, at this point, the value of the function is:
$$
(1+1)^{2} = 2^{2} = 4
$$
---
5.
This function has a zero at $z=-1 /2$ and a pole at $z=-2$. The pole has order 1.

---
6.
This function has a singularity at $z=0$. The Taylor series for the numerator is:
$$
\sum_{k=1}^{\infty} \frac{z^{k}}{k!}
$$
For the denominator:
$$
\sum_{k=0}^{\infty} \frac{(2z)^{k}}{k!} -1 = \sum_{k=1}^{\infty} \frac{(2z)^{k}}{k!}
$$
Since the first term of this Taylor series remains 1. The first few terms for these series at $z=0$ are:
$$
\sum_{k=1}^{\infty} \frac{z^{k}}{k!} = \sum_{k=1}^{\infty} \frac{0^{k}}{k!} = \frac{0}{1} + \frac{0}{2} + \frac{0}{3!} = 0
$$
$$
\sum_{k=1}^{\infty} \frac{(2z)^{k}}{k!} = \sum_{k=1}^{\infty} \frac{0^{k}}{k!} = 0
$$
All terms of both series are 0, therefore, this is an essential singularity, and cannot be removed.
### Questions 7-13
---
7.
Used the Taylor series expansion for $e^{ z }$
$$
e^{ z }-1 = \sum_{k=0}^{\infty} \frac{z^{k}}{k!} -1 = \sum_{k=1}^{\infty} \frac{z^{k}}{k!}
$$
And therefore the series for the full function is:
$$
\frac{1}{z^{2}} \sum_{k=1}^{\infty} \frac{z^{k}}{k!} = \sum_{k=1}^{\infty} \frac{z^{k-2}}{k!} = \sum_{k=-1}^{\infty} \frac{z^{k}}{(k+2)!}
$$
The residue is the -1th term of this series:
$$
\frac{z^{-1}}{(-1+2)!} = \frac{1}{1!} z^{-1} = z^{-1}
$$
And therefore the residue is 1

---
8.
Factor.
$$
\frac{z^{2}}{z^{2}-1} = \frac{z^{2}}{(z-1)(z+1)}
$$
So there is a zero with order 1 at $z=0$. The goal now is to expand $z^{2}$ in terms of powers of $z-1$. The first few derivatives are:
$$
\begin{align}
f & = z^{2} = 1 \\
f' & = 2z = 2 \\
f'' & = 2 = 2 \\
f''' & =0=0
\end{align}
$$
And therefore the first few coefficient are:
$$
\begin{align}
\frac{1}{0!}=1 &  & \frac{2}{1!}=2 &  & \frac{2}{2!} = 1 &  & 0=0
\end{align}
$$
The series is:
$$
1 + 2(z-1) + 1(z-1)^{2}
$$
The full function is hence:
$$
\frac{1}{z+1} \left[ \frac{1}{z-1} + 2 + (z-1) \right]
$$
The residue of the function is:
$$
\frac{1}{z+1} = \frac{1}{2}
$$
---
9.
First, find the Taylor series for $\sin z$ centred around $z=\pi$. The first few derivatives evaluate at this point are:
$$
\begin{align}
f' & = \cos z = \cos \pi & = -1 \\
f'' & = -\sin z = -\sin \pi & = 0 \\
f''' & = -\cos z = -\cos \pi & = 1 \\
f^{(4)} & = \sin z = \sin \pi & = 0
\end{align}
$$
So the derivatives alternate between negative and positive. The series representation is therefore:
$$
\sum_{k=0}^{\infty} \frac{(-1)^{k+1}}{(2k)!} (z-\pi)^{2k}
$$
The full series representation of the function is:
$$
\frac{1}{(z-\pi)^{2}} \sum_{k=0}^{\infty} \frac{(-1)^{k+1}}{(2k)!} (z-\pi)^{2k} = \sum_{k=0}^{\infty} \frac{(-1)^{k+1}}{(2k)!} (z-\pi)^{2(k-1)}
$$
Which is:
$$
\sum_{k=-1}^{\infty} \frac{(-1)^{k}}{(2k+2)!} (z-\pi)^{2k}
$$
The residue is:
$$
\frac{(-1)^{-1}}{(2(-1)+2)!} = -1
$$
- This is the -1th term of my series, but I think because the power in the denominator is 2, this might actually be incorrect. The term with the -1th power is equal to 0, so maybe the residue is zero.
---
11.
The goal is first to expand $az+b$ in terms of $cz+d$ centred at $z=-d /c$. Take derivatives:
$$
\begin{align}
f' & = a \\
f'' & = 0
\end{align}
$$
The coefficients are:
$$
\frac{f^{(n)}(z_{0})}{n!} = a_{n}
$$
Which in this case are:
$$
\frac{f(z_{0})}{0!} = a\left( -\frac{d}{c} \right)+b = -\frac{ad}{c}+b \qquad \frac{f'(z_{0})}{1!} = a \qquad \frac{f''(z_{0})}{2!} = 0
$$
So the series is:
$$
\left( b-\frac{ad}{c} \right)(cz+d)^{0} + a(cz+d)^{1} + 0(cz+d)^{2} = \left( b-\frac{ad}{c} \right) + a(cz+d)
$$
- I have no idea how to do this?
I'll solve for the residue using the typical formula:
$$
\text{Res}(f;z_{0}) = \frac{H^{(m-1)}(z_{0})}{(m-1)!}
$$
Where $m$ is the order of the pole. Which is, in this case, 1. And so the residue is:
$$
H(z_{0}) = a\left( -\frac{d}{c} \right)+b = b-\frac{ad}{c}
$$
---
13.
