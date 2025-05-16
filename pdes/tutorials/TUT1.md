### PDE types
Take for example $\mathcal{L}[u]=u_{x}+u_{yy} = f(x, y)$
- This is a linear PDE

Linearity allows us to say a lot of things. For example, if we have $f(x,y)=0$, then we can claim that $\mathcal{L}[u] + \mathcal{L}[v] = \mathcal{[u+v]} = 0$
- Similarly, we can also say the above is equal to $f_{1}+f_{2}$

Now, lets imagine that we have $a,b,c,d$, all functions of $x, y$. Then, we can try to write a (pretty) general first-order equation like:
$$
au_{x} + bu_{y} = cu + d
$$

Worked example: $yu_{x}+xu_{y}=0$
- We have learned two ways of solving this: method of characteristics, and change of variables
	- Change of variables is pretty much guess and check, so our TA recommends against relying on it
- The method of characteristics is based on the idea that there exists a "characteristic curve" along which our PDE is constant

Example 2: $-yu_{x}+xu_{y}=0$ and $u(x,0)=x^3$

This function can be rewritten as
$$
\begin{bmatrix}
-y \\
x
\end{bmatrix} \cdot \begin{bmatrix}
u_{x} \\
u_{y}
\end{bmatrix} = 0
$$
So, it is parallel to these lines. From here, we conclude that
$$
\frac{dy}{dt} = x\text{ and } \frac{dx}{dt}=-y
$$
The characteristics curves for this function are $C = x^2+y^2$. You can imagine these curves as a series of circles
- Note that there are several points where the initial condition is satisfied, when $y=0$.
- There is no unique solution, both with different results. In this case, we claim that we understand the behaviour of the PDEs locally, around the places where the condition is satisfied
- if the condition were changed to be uniquely for $x\geq 0$, for example, then we would have a unique solution, and this headache completely avoided

If the characteristic curves were $y = Ce^{ x }$, with an initial condition requiring $y=0$, then where would be no solution, instead of several

Take away: The characteristic curves and initial condition are also very important in PDEs

Example 3: $au_{x} + bu_{y} - cu = 0$

Try change of variables:
- $\omega=ax+by$
- $\eta = bx-ay$

Use chain rule for both:
$$
\begin{align}
u_{x}  & = \frac{du}{d\omega} \frac{d\omega}{dx} + \frac{du}{d \eta} \frac{d \eta}{dx} = au_{\omega} + bu_{\eta} \\
u_{y}  & = bu_{\omega} - au_{\eta}
\end{align}
$$
Substituting this back into the original equation, we get
$$
a(au_{\omega}+bu_{\eta} )+b(bu_{\omega}+au_{\eta}) = (a^2+b^2)u_{\omega} - cu=0
$$
And so we have reduced the original equation to an ODE. The solution is
$$
u=e^{ \frac{c}{a^2+b^2}\omega } f(\eta) \Rightarrow u(x, y) = f(bx-ay) e^{ \frac{c}{a^2+b^2}(ax+by) }
$$
