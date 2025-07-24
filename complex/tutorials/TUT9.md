Fisher 2.6
### Questions 4-6
---
4.
Factor this function into:
$$
\frac{\cos \alpha x}{(x-i)(x+i)(x-2i)(x+2i)}
$$

Now use the substitution $y=\alpha x$ to change this function into:
$$
\frac{\cos y}{\left( \frac{y}{\alpha}-i \right)\left( \frac{y}{\alpha}+i \right)\left( \frac{y}{\alpha}-2i \right)\left( \frac{y}{\alpha}+2i \right)}
$$
Which has two poles in the upper half plane: $y=i\alpha, 2i\alpha$. Use the new, simpler function:
$$
f(z) = \frac{e^{ iz }}{\left( \frac{z}{\alpha}-i \right)\dots}
$$
Compute the residues:
$$
\text{Res}(f;i\alpha) = \frac{e^{ i(i\alpha) }}{\left( \frac{i\alpha}{\alpha}+i \right)\left( \frac{i\alpha}{\alpha}-2i \right)\left( \frac{i\alpha}{\alpha}+2i \right)} = \frac{e^{ -\alpha }}{6i}
$$
$$
\text{Res}(f;2i\alpha) = \frac{e^{ i(2i\alpha) }}{\left( \frac{2i\alpha}{\alpha}-i \right)\left( \frac{2i\alpha}{\alpha}+i \right)\left( \frac{2i\alpha}{\alpha}+2i \right)} = -\frac{e^{ -2\alpha }}{12i}
$$
And the real part of this is 0

---
5.
Compute the imaginary portion of the new integral:
$$
\int_{-\infty}^{\infty} f(z) \, dz
$$
For the function:
$$
f(z) = \frac{x}{x^{4}+1} e^{ iz }
$$
Factor.
$$
x^{4}+1 = (x - e^{ i\pi/4 }) (x + e^{ i\pi/4 }) (x - e^{ 3i\pi/4 }) (x + e^{ 3i\pi/4 })
$$
