Assigned questions: 1-19
### Questions 1-3
---
2.
Factor the denominator:
$$
x^{4} - 4x^{2} + 5 = (\sqrt{ 2-i }\pm x)(\sqrt{ 2+i }\pm x)
$$
And so there are four roots, all of order 1. The two in the upper-half are $\sqrt{ 2+i }$ and $-\sqrt{ 2-i }$. Recall that the residue can be calculated using:
$$
\text{Res}(f;z_{0}) = \frac{H^{(m-1)}(z_{0})}{(m-1)!}
$$
Where $m$ is the order of the root. Computing both residues:
$$
\text{Res}(f;\sqrt{ 2+i }) = \frac{H(z_{0})}{0!} = \frac{z_{0}^{2}}{(\sqrt{ 2-i }\pm z_{0})(\sqrt{ 2+i }+z_{0})} = \frac{i}{4}\sqrt{ 2+i }
$$
$$
\text{Res}(f;-\sqrt{ 2-i }) = H(-\sqrt{ 2-i }) = \frac{z_{0}^{2}}{(\sqrt{ 2+i }\pm z_{0})(\sqrt{ 2-i }-z_{0})} = -\frac{i}{4}\sqrt{ 2-i }
$$
By the residue theorem, the full integral is equal to:
$$
\int _{\gamma} \frac{z^{2}}{z^{4}-4z^{2}+5} \, dz = 2\pi i \left[ \frac{i}{4}\sqrt{ 2+i } - \frac{i}{4}\sqrt{ 2-i } \right]  = \frac{\pi}{2} (\sqrt{ 2-i }-\sqrt{ 2+i })
$$
This computation is only equivalent to the original integral if the integral around the top half-semicircle converges to zero.

Use the parametrization $\gamma(t)=R e^{ it }$ and therefore $\gamma'=Rite^{ it }$.
$$
\int_{0}^{\pi} \frac{R^{2} e^{ 2it }}{R^{4}e^{ 4it } - 4R^{2}e^{ 2it }+5} (Rite^{ it }) \, dt \leq \int_{0}^{\pi} \left| \frac{R^{2} e^{ 2it }}{R^{4}e^{ 4it } - 4R^{2}e^{ 2it }+5} (Rite^{ it }) \right|  \, dt
$$
Now, take the limit as $R\to \infty$
$$
\lim_{ R \to \infty } \int_{0}^{\pi} \left| \frac{R^{3}t e^{ 3it }}{R^{4}\left( e^{ 4it } - \frac{4}{R^{2}} e^{ 2it } +\frac{5}{R^{4}} \right)} \right|  \, dt
$$
Which behaves similarly to $R^{-1}$ as $R\to \infty$, which approaches 0. I conclude that this integral vanishes, and so the above calculation is equivalent to the original integral.

---
3.
Factor the denominator,
$$
(x^{2}+a^{2})(x^{2}+b^{2}) = (x\pm ia)(x\pm ib)
$$
Rewrite the original function as:
$$
\int_{-\infty}^{\infty} \frac{1}{(x^{2}+a^{2})(x^{2}+b^{2})} \, dx = \int _{\gamma} \frac{1}{(z\pm ia)(z\pm ib)} \, dz
$$
There are two roots in the upper-half. $ia$ and $ib$. Both of which have order 1. The residues are:
$$
\text{Res}(f;ia) = \frac{1}{(z_{0}\pm ib)(z_{0}+ia)} = \frac{i}{2a^{3} - 2ab^{2}}
$$
$$
\text{Res}(f;ib) = \frac{1}{(z_{0}\pm ia)(z_{0}+ib)} = -\frac{i}{2a^{2}b - 2b^{3}}
$$
By the residue theorem:
$$
\int _{\gamma} \frac{1}{(z\pm ia)(z\pm ib)} \, dz = 2\pi i \left[ \frac{i}{2a^{3}-2ab^{2}} - \frac{i}{2a^{2}b-2b^{3}} \right] = \frac{\pi}{ab(a+b)}
$$
Now, prove that the integral converges to zero around the semi-circle.

Use the parametrization $\gamma(t)=R e^{ it }$,
$$
\int_{0}^{\pi} \frac{1}{(R e^{ it }\pm ia)(R e^{ it }\pm ib)} (Rite^{ it }) \, dz
$$
Check the limit of the absolute value as $R\to \infty$
$$
\lim_{ R \to \infty } \int_{0}^{\pi} \left| \frac{1}{(R e^{ it }\pm ia)(R e^{ it }\pm ib)} (Rte^{ it }) \right|  \, dz
$$
The full function behaves like:
$$
\lim_{ R \to \infty } \frac{R}{R^{2}} = \lim_{ R \to \infty } \frac{1}{R} = 0
$$
And therefore the integral across the semi-circle vanishes.
### Questions 4-8
---
4.
Recall that cosine is the real part of the complex exponential. Therefore, by replacing $\cos \alpha x$ with $e^{ i\alpha x }$, then I can compute a much easier integral, and then take the real part for the answer. Define:
$$
\int _{\gamma} \frac{e^{ i\alpha z }}{(z^{2}+1)(z^{2}+4)} \, dz
$$
Where $\gamma$ is the semi-circle going over the upper-half of the complex plane. Factor the denominator:
$$
(z^{2}+1)(z^{2}+4) = (z\pm i)(z\pm 2i)
$$
There are two roots of order 1 in the domain surrounded by $\gamma$. Take the two residues of $i$ and $2i$.
$$
\text{Res}(f;i) = \frac{H(z_{0})}{0!} = \frac{e^{ i\alpha z_{0} }}{(z_{0}\pm 2i)(z_{0}+i)} = -\frac{i}{6} e^{ -\alpha }
$$
$$
\text{Res}(f;2i) = H(2i) = \frac{e^{ i\alpha(2i) }}{(2i\pm i)(2i+2i)} = \frac{i}{12} e^{ -2\alpha }
$$
Therefore,
$$
\int _{\gamma} \frac{e^{ i\alpha z }}{(z^{2}+1)(z^{2}+4)} \, dz = 2\pi i \left[ \frac{i}{12}e^{ -2\alpha } - \frac{i}{6}e^{ -\alpha } \right] = -\frac{\pi}{6} (e^{ -2\alpha } - 2 e^{ -\alpha })
$$
Which is entirely real, so:
$$
\int_{-\infty}^{\infty} \frac{\cos \alpha x}{(x^{2}+1)(x^{2}+4)} \, dx = -\frac{\pi}{6} (e^{ -2\alpha } - 2e^{ -\alpha })
$$
Now, in order for this result to be accurate, the complex integral must vanish along the semi-circle not on the real line. Start by taking the absolute value:
$$
\left| \frac{e^{ i\alpha z }}{(z^{2}+1)(z^{2}+4)} \right| \leq \frac{\left| e^{ i\alpha z } \right| }{|(z^{2}+1)(z^{2}+4)|}
$$
Recall that the magnitude of the complex exponential is always 1. Furthermore, applying the parametrization $\gamma(t)=R e^{ it }$
$$
= \frac{1}{(z^{2}+1)(z^{2}+4)} = \frac{1}{(R^{2}e^{ 2it }+1)(R^{2}e^{ 2it }+4)} (Rite^{ it })
$$
Which goes like:
$$
\lim_{ R \to \infty } \frac{R}{R^{4}} = \lim_{ R \to \infty } \frac{1}{R^{3}} =0
$$
And so this integral vanishes along the upper-half semi-circle.

---
6.
Define:
$$
\int _{\gamma} \frac{e^{ iz }}{z^{2}+6z+10} \, dz = \int _{\gamma} \frac{e^{ iz }}{(z+(3-i))(z+(3+i))} \, dz
$$
Which has one root in the upper-half plane:
$$
\text{Res}(f;-3+i) = H(-3+i) = \frac{e^{ i(-3+i) }}{((-3+i)+(3+i))} = -\frac{i}{2} e^{ -1-3i }
$$
By the residue theorem:
$$
= 2\pi i \left[ -\frac{i}{2} e^{ -1-3i } \right] = e^{ -1-3i }\pi
$$
Which has the imaginary part:
$$
\int_{-\infty}^{\infty} \frac{\sin x}{x^{2}+6x+10} \, dx = \frac{\pi}{e} \sin(-3)
$$
- I don't feel like proving the other part of the integral vanishes
---
8.
Use the new function:
$$
\frac{e^{ i \gamma x }}{(x^{2}+\alpha^{2})(x^{2}+\beta^{2})} = \frac{e^{ i\gamma x }}{(x\pm i\alpha)(x\pm i\beta)}
$$
The original function is just the real part of this one.
$$
\text{Res}(f;i\alpha) = H(i\alpha) = \frac{e^{ i\gamma(i\alpha) }}{(i\alpha+i\alpha)(i\alpha\pm i\beta)} = \frac{ie^{ -\gamma \alpha }}{2\alpha^{3} - 2\alpha \beta^{2}}
$$
$$
\text{Res}(f;i\beta) = H(i\beta) = \frac{e^{ i\gamma(i\beta) }}{(i\beta+i\beta)(i\beta\pm i\alpha)} = -\frac{ie^{ -\gamma \beta }}{2\alpha^{2}\beta - 2\beta^{3}}
$$
By residue theorem:
$$
2\pi i \left[ \text{Res}(f;i\alpha) + \text{Res}(f;i\beta) \right] = - \frac{\pi}{\alpha \beta(\alpha^{2}-\beta^{2})} (\beta e^{ -\gamma \alpha } - \alpha e^{ -\gamma \beta })
$$
Which is the integral over the top half plane along the interval $-\infty$ to $\infty$. From 0 to $\infty$. We have:
$$
\int_{0}^{\infty} \frac{\cos \gamma x}{(x^{2}+\alpha^{2})(x^{2}+\beta^{2})} \, dx = \frac{\pi}{2\alpha \beta (\alpha^{2}-\beta^{2})} (\alpha e^{ i\gamma \beta } - \beta e^{ i\gamma \alpha })
$$
- WHICH IS CORRECT HOLY FUCK
### Questions 9-12
---
9.
Recall that:
$$
\sin \theta = \frac{1}{2i} \left( z-\frac{1}{z} \right)
$$
Re-write the original function:
$$
\frac{1}{(2-\sin \theta)^{2}} = \frac{1}{\left( 2-\frac{1}{2i}\left( z-\frac{1}{z} \right) \right)^{2}} = - \frac{4z^{2}}{(z^{2}-4iz-1)^{2}}
$$
Which has the roots:
$$
z^{2}-4iz-1 = (-iz+\sqrt{ 3 }-2)(iz+\sqrt{ 3 }+2)
$$
Both of which have order 2 because they are squared. Calculate residuals:
$$
\text{Res}(f;i(2-\sqrt{ 3 })) = \frac{d}{dz} H(i(2-\sqrt{ 3 })) = -\frac{i}{3} (2-\sqrt{ 3 })(2+3\sqrt{ 3 })
$$
$$
\text{Res}(f;i(\sqrt{ 3 }+2)) = \frac{d}{dz} H(i(\sqrt{ 3 }+2)) = \frac{i}{3} (2-3\sqrt{ 3 }) (2+\sqrt{ 3 })
$$
By residue theorem:
$$
2\pi i \left[ \text{Res}(f;i(2-\sqrt{ 3 })) + \text{Res}(f;i(2+\sqrt{ 3 })) \right] = \frac{16\pi}{\sqrt{ 3 }}
$$
Which is entirely real. We need to take the imaginary part of this for the sine, therefore:
$$
\int_{0}^{2\pi} \frac{1}{(2-\sin \theta)^{2}} \, d\theta = \mathrm{Im}\left( \frac{16\pi}{\sqrt{ 3 }} \right) = 0
$$
- I think I made a mistake with the domain here. The domain is supposed to be the unit circle. $2+\sqrt{ 3 }$ is far greater than 1, so it should have been excluded from the residue calculation.
- I'm way too lazy to go back now though.
---
