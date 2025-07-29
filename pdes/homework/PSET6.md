### Question 1
This is a problem that has been solved in class before. The solution is in the form:
$$
u(r, \theta) = \sum_{n=1}^{\infty} A_{n} r^{n\pi/\beta} \sin\left( \frac{n\pi \theta}{\beta} \right)
$$
The coefficients can be determined from the boundary condition:
$$
\frac{ \partial u }{ \partial r } (a, \theta) = \sum_{n=0}^{\infty} A_{n} \left( \frac{n\pi}{\beta} \right) a^{(n\pi/\beta) -1} \sin\left( \frac{n\pi \theta}{\beta} \right) = \theta
$$
Which is now a Fourier sine series on the interval $[0, \beta]$ with the known coefficients:
$$
\begin{align}
A_{n} \left( \frac{n\pi}{\beta} \right)a^{(n\pi/\beta)-1} & = \frac{2}{\beta} \int_{0}^{\beta} \theta \sin\left( \frac{n\pi\theta}{\beta} \right) \, d\theta \\
A_{n} & = a^{1-n\pi/\beta} \left( \frac{2}{n\pi} \right) \int_{0}^{\beta} \theta \sin\left( \frac{n\pi\theta}{\beta} \right) \, d\theta
\end{align}
$$
### Question 2
