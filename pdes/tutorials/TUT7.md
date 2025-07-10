### Orthogonality of Functions, and Separation of Variables
Using separation of variables, we typically get functions in the form
$$
u(x, t) = \sum A_{n}\phi_{n}(x)T_{n}(t)
$$
And, in order to determine the coefficients $A_{n}$ we use orthogonality. So, how do we define orthogonality for functions?
$$
\text{On }F = \{ f:[-1, 1]\to \mathbb{R} \}
$$
We claim that some function $f_{1}$ is orthogonal to $f_{2}$ if:
$$
\int_{-1}^{1} f_{1}(x)f_{2}(x) \, dx =0
$$
Following this definition, you can show that $f_{1}(x)=1$ and $f_{2}(x)=x$, for example, are orthogonal.

Now, how would we find some function $f_{3}(x)=ax^{2}+bx+c$ that is orthogonal to $f_{1}$ and $f_{2}$?
$$
\begin{align}
\int_{-1}^{1} (ax^{2}+bc+c) \, dx =0 \\
\int_{-1}^{1} x(ax^{2}+bx+c) \, dx =0
\end{align}
$$
Evaluating the above, we obtain the system of equations:
$$
\begin{align}
\frac{2}{3}a+c=0 \\
\frac{2}{3}b=0
\end{align}
$$
And so we conclude that:
$$
f_{3}(x) = ax^{2} - \frac{1}{3}a
$$
Now, notice that the set of orthogonal functions is a vector space. For functions, the inner product is defined to be:
$$
\left< f_{1}, f_{2} \right>   = \int_{-1}^{1} f_{1}(x)f_{2}(x) \, dx
$$
And so we can use the familiar Gram-Schmidt method to determine more and more orthogonal vectors:
$$
v_{1}=u_{1}, \qquad v_{2} = u_{2} \frac{\left< u_{1}, u_{2} \right> }{\left< u_{1}, u_{1} \right> }u_{1}, \qquad v_{3} = u_{3} - \frac{\left< u_{1}, u_{2} \right> }{\left< u_{2}, u_{2} \right> }u_{2} - \dots
$$
---
Solve for $f_{3}(x)=ax^{2}+bx+c$ again, but with the Gram-Schmidt method:
$$
u_{1}=1 \qquad u_{2}=x \qquad u_{3}=x^{2}
$$
And so we have:
$$
f_{3} = x^{2} - \frac{\left< 1, x^{2} \right> }{\left< 1, 1 \right> }(1) - \frac{\left< x, x^{2} \right> }{\left< x, x \right> }x = x^{2}-\frac{1}{3}
$$
Which is identical to the previous solution, if we chose $a=1$.

---

These orthogonal polynomials are called the Legendre polynomials
- There is another called the Chebyshev polynomials
- They're just different orthogonal basis for functions