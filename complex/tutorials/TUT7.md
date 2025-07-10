### Questions 1-8
4.
Factor
$$
\left[ (z^{2}-4z+4) \right] ^{3}=\left[ (z-2)^{2} \right] ^{3} = (z-2)^{6}
$$
From here, you can tell that the order of this zero will be 6

5.
Use Taylor series:
$$
z^{2}(1-\cos z) = z^{2}\left( 1- \sum_{k=0}^{\infty} \frac{(-1)^{k}z^{2k}}{(2k)!} \right) = z^{2} - z^{2} \sum_{k=0}^{\infty} \frac{(-1)^{k}z^{2k}}{(2k)!}
$$
$$
z^{2} - \sum_{k=0}^{\infty} \frac{(-1)^{k}z^{2k+2}}{(2k)!}
$$
Write it out explicitly
$$
z^{2} - \left[ z^{2} - \frac{z^{4}}{2} + \dots \right] = -\frac{z^{4}}{2} + \dots
$$
This function has periodic zeroes at every $2\pi n$ for all $n\in \mathbb{Z}$. These zeros are all of the same order, 4

6.
Since we have $|z|<1$. We can use Taylor series:
$$
\log(1-z) = - \sum_{n=1}^{\infty} \frac{z^{n}}{n} = -z - \frac{z^{2}}{2} - \dots
$$
The zero at $z=0$ has order 1

1.
The zeroes for this function are located at all odd multiples of $\pi$. They are periodic, with the same order. I will use the one centred at $z=\pi$ to determine the order of all of them.
$$
\frac{d}{dz} \frac{\sin z}{z} = \frac{z\cos z - \sin z}{z^{2}}
$$
Which is non zero at $z=\pi$
$$
\frac{\pi \cos \pi - \sin \pi}{\pi^{2}} = \frac{\pi(-1)-0}{\pi^{2}} = -\frac{\pi}{\pi^{2}} = -\frac{1}{\pi} \neq 0
$$
So this zero has order 1