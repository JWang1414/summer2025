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
