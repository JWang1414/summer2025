### Green's First Identity
First, we need to recall a few identities:
$$
grad(f) = \nabla f = \text{vector}(f_{x}, f_{y}, f_{z})
$$
$$
div(\vec{F}) = \nabla \cdot \vec{F} = \frac{ \partial F_{1} }{ \partial x } + \frac{ \partial F_{2} }{ \partial y } + \frac{ \partial F_{3} }{ \partial z }
$$
Where the function $\vec{F}$ is defined as: $\vec{F}=(F_{1}, F_{2}, F_{3})$
$$
\left| \nabla f \right| ^{2} = f_{x}^{2} + f_{y}^{2} + f_{z}^{2}
$$
$$
\Delta f = div(grad(f)) = \nabla \cdot \nabla f = f_{xx} + f_{yy} + f_{zz}
$$
Integrals over a 3D region or solid:
$$
\int _{D}\dots \, d\vec{x} = \iiint_{D} \dots \, dxdydz
$$
Over a flat surface:
$$
\iint_{D} \dots \, dS
$$
Divergence theorem:
$$
\iiint_{D} \nabla \cdot \vec{F} \, d\vec{x} = \iint_{\partial D} \vec{F}\cdot \hat{n} \, dS
$$
Where $\vec{F}$ is any smooth vector field, $D$ is a bounded region, and $\hat{n}$ is unit outer normal on $\partial D$
### Derivation of Green's First identity
Start with the product rule. For some vector $\vec{x}=(x_{1}, x_{2}, x_{3})$
$$
(vu_{x_{i}})_{x_{i}} = v_{x_{i}}u_{x_{i}} + vu_{x_{i}x_{i}}
$$
Sum over $i=1, 2, 3$ we get:
$$
div(v\nabla u) = \nabla v \cdot \nabla u + v \Delta u
$$
Integrate over the domain $D$
$$
\iiint_{D} div(v\nabla u) \, d\vec{x} = \iiint_{D} \nabla v\cdot \nabla u \, d\vec{x} + \iiint_{D} v\Delta u \, d\vec{x}
$$
Apply the divergence theorem to the left side to obtain:
$$
\iint_{\partial D} v\nabla u\cdot \hat{n} \, dS = \iint_{\partial D} v \frac{ \partial u }{ \partial n } \, dS
$$
This is Green's first identity, which we will call G1:
$$
\iiint_{D} v\Delta u \, d\vec{x} = \iint_{\partial D} v \frac{ \partial u }{ \partial n } \, dS - \iiint_{D} \nabla v\cdot \nabla u \, d\vec{x}
$$
### Mean Value Property
Let $u$ be a smooth harmonic function, then the average value of $u$ over any sphere equals its value at the centre
- This is the mean value property in 3D as opposed to 2D
### Dirichlet's Principle
Among all smooth functions $w(\vec{x})$ in $D$ that satisfy the Dirichlet boundary condition
$$
w=h(\vec{x}) \qquad \text{on }\partial D
$$
the lowest energy occurs for the harmonic function satisfying the boundary condition.

That is, for any two functions that satisfy the Dirichlet boundary conditions $u, v$, if $u$ is also a harmonic function, then:
$$
E[u] \leq E[v]
$$
The energy of one of these functions is defined to be the potential energy:
$$
E[w] := \frac{1}{2} \iiint_{D} \left| \nabla w \right| ^{2} \, d\vec{x}
$$
In physics, systems often tend to the ground state, the state of lowest energy. This statement tell us that the harmonic function is the preferred physical ground state.
