Questions 1-17
### Questions 1-8
---
1.
This function has zeroes at all $2\pi k$ where $k\in \mathbb{Z}$, except for $k=0$.

Taking the first derivative of this function:
$$
\frac{d}{dz} \frac{\sin z}{z} = \frac{\cos z}{z} - \frac{\sin z}{z^{2}}
$$
Which is non-zero for all possible zeroes, implying that the zeroes are of order 1.

---
2.
One zero at $z=0$

Expand this function:
$$
(e^{ z }-1)^{2} = e^{ 2z } - 2e^{ z } + 1
$$
First few derivatives are:
$$
f'=2e^{ 2z } - 2e^{ z } \qquad f'' = 4e^{ 2z } - 2e^{ z }
$$
Second derivative is non-zero, so this is a zero of order 2.

---
3.
Factor the given function:
$$
(z^{2}+z-2)^{3} = \left[ (z+2)(z-1) \right] ^{3} = (z+2)^{3}(z-1)^{3}
$$
By observation, we can see this has two zeroes at $z=-2, 1$. Both of them have order 3.

---
4.
Factor.
$$
(z^{2}-4z+4)^{3} = \left[ (z-2)(z-2) \right] ^{3} = (z-2)^{6}
$$
This function has one zero at $z=2$ with an order of 6

---
5.
This function has zeroes at $z=2\pi k$ where $k\in \mathbb{Z}$

Expand this function:
$$
z^{2}(1-\cos z) = z^{2}-z^{2}\cos z
$$
Take derivatives:
$$
\begin{align}
\text{First:} &  & z^{2} \sin z - 2\cos z + 2z \\
\text{Second:} &  & 4z \sin z + (z^{2}-2) \cos z + 2
\end{align}
$$
All zeroes have order 1.

---
6.
This function has one zero at $z=0$

First derivative is:
$$
\frac{1}{z-1}
$$
Which for $z=0$ is $-1$ and therefore this zero is of order 1.

---
7.
Factor the function:
$$
e^{ 2z } - 3e^{ z } - 4 = (e^{ z }-4)(e^{ z }+1)
$$
So there are two zeros. When $z=\ln 4$ and $z=\pi i$. The first derivative is:
$$
e^{ z }(2e^{ z }-3)
$$
Which isn't zero for both zeroes. So, both of zeroes are of order 1.

---
8.
This function has a zero at $z=0$ and two poles at $z=\pm i$. Factor this function:
$$
\frac{z}{z^{2}+1} = \frac{z}{(z+i)(z-i)}
$$
By observation, all zeroes and poles are of order 1.

### Question 9-16
---
9.
Recall that the Taylor series for $e^{ z }$ around $z_{0}=0$ is:
$$
e^{ z } = \sum_{k=0}^{\infty} \frac{z^{k}}{k!} = 1 + x + \dots
$$
Notice that the first term of this series is 1. Therefore,
$$
z(e^{ z }-1) = z \left[ \sum_{k=0}^{\infty} \frac{z^{k}}{k!} -1 \right] = z \left[ \sum_{k=1}^{\infty} \frac{z^{k}}{k!} \right] = \sum_{k=1}^{\infty} \frac{z^{k+1}}{k!}
$$
This series is valid for all $\mathbb{C}$

---
10.
Recall that the coefficients of a series centred at $z_{0}$ are:
$$
\frac{f^{(n)}(z_{0})}{n!} = a_{n}
$$
The derivatives of $e^{ z }$ are always itself, and therefore we have the coefficients:
$$
\frac{e^{ z_{0} }}{n!} = \frac{e^{ \pi i }}{n!} = -\frac{1}{n!} = a_{n}
$$
Furthermore, recall that power series have the structure:
$$
f(z) = \sum_{k=0}^{\infty} a_{k}(z-z_{0})^{k}
$$
Combining this with the found coefficients:
$$
e^{ z } = \sum_{k=0}^{\infty} -\frac{1}{k!} (z-z_{0})^{k} = \sum_{k=0}^{\infty} -\frac{(z-\pi i)^{k}}{k!}
$$
Which is the Taylor series for $e^{ z }$ about $\pi i$

---
11.
There will be a finite number of non-zero derivatives, and therefore a finite number of coefficients.

Take derivatives:
$$
\begin{align}
f' & = 3z^{2} + 12z - 4 \\
f'' & = 6z+12 \\
f''' & = 6 \\
f^{(4)} & = 0
\end{align}
$$
Now evaluate all these functions at $z=z_{0}=1$
$$
\begin{align}
f(z_{0}) & = 1+6-4-3 = 0 \\
f'(z_{0}) & = 3+12-4 = 11 \\
f''(z_{0}) & = 6+12 = 18 \\
f'''(z_{0}) & = 6
\end{align}
$$
And therefore the coefficients are:
$$
\begin{align}
a_{0} & = \frac{0}{0!} = 1 & a_{1} & = \frac{11}{1!} = 11 \\
a_{2} & = \frac{18}{2!} = 9 & a_{3} & = \frac{6}{3!} = 1
\end{align}
$$
Which yields the Taylor series:
$$
f(z) = 11(z-1) + 9(z-1)^{2} + (z-1)^{3}
$$
---
12.
Recall that, for $|z|<1$,
$$
\frac{1}{1-z} = \sum_{k=0}^{\infty} z^{k}
$$
Which is the geometric series. Therefore, from the properties of power series:
$$
\frac{z^{2}}{1-z} = z^{2} \sum_{k=0}^{\infty} z^{k} = \sum_{k=0}^{\infty} z^{k+2} = \sum_{k=2}^{\infty} z^{k}
$$
---
13.
- I don't know how to do this one
$$
1-u = z+3 \implies z = 1-u-3 = -2-u
$$
$$
\frac{(-2-u)+2}{1-u} = -\frac{u}{1-u}
$$
---
14.
Recall that:
$$
\log(1-z) = - \sum_{k=1}^{\infty} \frac{z^{k}}{k}
$$
Therefore,
$$
\left[ \log(1-z) \right] ^{2} = \left( -\sum_{n=1}^{\infty} \frac{z^{n}}{n} \right)\left( -\sum_{k=1}^{\infty} \frac{z^{k}}{k} \right) = \sum_{k=1}^{\infty} \frac{z^{k}}{k} \sum_{n=1}^{\infty} \frac{z^{n}}{n}
$$
Compute the first few terms of a single series to help compute the first four terms later:
$$
k=1 \implies z \qquad k=2 \implies \frac{z^{2}}{2} \qquad k=3 \implies \frac{z^{3}}{3} \qquad k=4\implies \frac{z^{4}}{4}
$$
The first four terms are therefore:
$$
z^{2} + z^{3} + \frac{11}{12}z^{4} + \frac{5}{6} z^{5}
$$
---
15.
Compute the first few derivatives:
$$
\begin{align}
f' & = \cos(\pi z)(\pi) \\
f'' & = -\sin(\pi z)(\pi^{2}) \\
f''' & = -\cos(\pi z)(\pi^{3}) \\
f^{(4)} & = \sin(\pi z)(\pi^{4})
\end{align}
$$
Notice that, at $z_{0}=1 /2$, the argument within each trig function is $\pi /2$. In which case, cosine is always zero, and sine alternates between 1 and -1. The coefficients are therefore:
$$
a_{n} = \frac{f^{(n)}(z_{0})}{n!} = \frac{(-1)^{n}\pi^{2n}}{(2n)!}
$$
Apply the power series structure to obtain:
$$
f(z) = \sum_{k=0}^{\infty} a_{k}(z-z_{0})^{k} \implies \sin(\pi z) = \sum_{k=0}^{\infty} \frac{(-1)^{k}\pi^{2k}}{(2k)!}\left( z-\frac{1}{2} \right)^{k}
$$
---
16.
By definition
$$
\tan z = \frac{\sin z}{\cos z}
$$
Recall that the Taylor series for these two functions are:
$$
\sin z = \sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k+1)!}z^{2k+1} \qquad \cos z = \sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k)!} z^{2k}
$$
Therefore we have:
$$
\tan z = \sum_{k=0}^{\infty} \frac{(-1)^{k}}{(2k+1)!} z^{2k+1} \sum_{n=0}^{\infty} \frac{(2n)!}{(-1)^{n}z^{2n}}
$$
The first few terms of these two series are:
$$
\begin{align}
\sin z & = z - \frac{z^{3}}{6} + \frac{z^{5}}{120} - \frac{z^{7}}{5040} + \dots \\
\frac{1}{\cos z} & = 1 + \frac{z^{2}}{2} + \frac{5}{24} z^{4} + \frac{61}{720} z^{6} + \dots
\end{align}
$$
And therefore the first few terms of $\tan z$ are:
$$
\tan z = z + \frac{z^{3}}{3} + \frac{2}{15} z^{5} + \frac{17}{315} z^{7}
$$
---
### Question 17
- I don't have time for this one