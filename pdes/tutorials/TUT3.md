Problems related to diffusion on the half line

---
Initial conditions
$$
\phi _\text{odd} = \begin{cases}
e^{ -x } &  & x>0 \\
-e^{ -x } &  & x<0
\end{cases}
$$
Recall the solution equation for the diffusion equation:
$$
\frac{1}{\sqrt{ 4kt }} \int_{-\infty}^{\infty} \exp \left[ -\frac{(x-y)^{2}}{4kt} \right] \phi _\text{odd/even}(y) \, dy
$$
Substitute our defined initial conditions:
$$
\frac{1}{\sqrt{ 4kt }}\left[ \int_{0}^{\infty} e^{ -(x-y)^{2}/4kt }e^{ -y } \, dy + \int_{-\infty}^{0} e^{ -(x-y)^{2}/4kt }(-e^{ -y }) \, dy  \right]
$$
Using a change of variables, we obtain:
$$
\frac{1}{\sqrt{ 4kt }}\int_{0}^{\infty} -e^{ -(x+y)^{2}/4kt }e^{ y } + e^{ -(x-y)^{2}/4kt }e^{ -y } \, dy
$$
---
Now, try thinking on the heat equation, and how reflection can help solve it

In 2-D, for example, on the half-plane, we can simply use reflection because the boundary is a well defined line in the Cartesian plane.

However, we can also do the same if the area if a disk. Since if we use a polar transformation, we can reflect the conditions however we want by this boundary
- Mapping with a function like $f(r)=1 /r$ 

Now, what about for some irregular shape? Well, we can find a function $f$ that maps this shape into a shape we are familiar with, like a circle, plane, sphere, etc.
- There is a complex analysis proof that shows this functions $f$ always exists
1. Map into a familiar shape
2. Solve on the familiar shape
3. Map back to the irregular shape
