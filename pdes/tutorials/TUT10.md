### Green's functions
We denote Green's functions with $G(x, x_{0})$

Defining some derivative operator $\mathcal{L}$ for a Green's function we have the condition that:
$$
\mathcal{L}[G] = \delta(x-x_{0})
$$
Where $\delta$ is the delta function:
$$
\delta(x-x_{0}) = \begin{cases}
1 & x=x_{0} \\
0 & \text{otherwise}
\end{cases}
$$
Furthermore we require that:
$$
G(x, x_{0})=0 \text{ on } x \in \partial \Omega
$$

---
Suppose we have $G_{1}$ and $G_{2}$. Consider $W=G_{1}-G_{2}$ and $\mathcal{L}[G]=\Delta G$.
$$
\begin{cases}
\Delta W=0 & \text{on }\Omega \\
W=0 & \text{on } \partial \Omega
\end{cases}
$$
And so $W\Delta W=0$.

Using Green's identities we obtain:
$$
0 = \int _{\Omega} w\Delta w \, dx = \int _{\partial \Omega} w \frac{ \partial w }{ \partial n }  \, dS - \int _{\Omega} \nabla w \cdot \nabla w \, dx = 0 - \int _{\Omega}\left| \nabla w \right| ^{2} \, dx \Rightarrow \nabla w=0
$$
Which means that $W$ must be a constant function. Since it's zero on the boundary, we conclude that $W=0$ and the solutions to the Green's functions are unique.

---

