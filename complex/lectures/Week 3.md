Recall that a function is a rule that assigns some complex $z$ to another value
- The domain $D$ is the possible values a function can accept
- The range is a collection of all possible values of the function

For functions in a real space, we are used to plotting them out in a 2-D or 3-D plane. However, for complex functions, it is often more useful to plot the domain and range separately, to visualize how the function transforms the data

Real example:
![[Pasted image 20250527142756.png]]

Complex example:
![[Pasted image 20250527142806.png]]
### Limits
Virtually identical to their definition for real numbers

For a given sequence $\{ z_{n} \}^{\infty}_{n=1}$, we claim that this sequence has the limit $A$ if for any $\varepsilon>0$, there exists some $N\in \mathbb{Z}$ such that $|z_{n}-A|<\varepsilon$ for all $n\geq N$

The limit for a sequence is written as:
$$
\begin{align}
\lim_{ n \to \infty } z_{n}=A &  & \text{or} &  &  z_{n}\to A
\end{align}
$$
- Sequences that do not *converge* are called *divergent*

Define $z_{n}=x_{n}+iy_{n}$ and $A=s+it$, then, if $z_{n}$ is a convergent sequence, we can claim that:
$$
\begin{align}
|x_{n}-s|\leq|z_{n}-A| &  & |y_{n}-t|\leq|z_{n}-A|
\end{align}
$$
$$
|z_{n}-A|\leq |x_{n}-s| + |y_{n}-t|
$$
Visually, a sequence $\{ z_{n} \}$ converges to number $A$ whenever $D$ is any open disc centred at $A$ such that all but a finite number of points $\{ z_{n} \}$ line inside $D$

Given two convergent sequences $\{ z_{n} \}$ and $\{ w_{n} \}$, that have limits $A$ and $B$, then we know:
- $\{ z_{n}+\lambda w_{n} \}$ converges to $A+\lambda B$, where $\lambda$ is some complex number
- $\{ z_{n}w_{n} \}$ converges to $AB$

Functions have a limit $L$ if, for some $\varepsilon>0$, there exists some $\delta>0$ such that $|f(z)-L|<\varepsilon$ whenever $z\in S$ and $|z-z_{0}|<\delta$
- Since the complex plane has two dimensions, there is an infinite number of direction a limit can approach from

The limit for a function is written as:
$$
\begin{align}
\lim_{ z \to z_{0} } f(z)=L &  & \text{or} &  & f(z)\to L\text{ as }z\to z_{0}
\end{align}
$$
Uniquely, the limit
$$
\lim_{ z \to \infty } f(z)=L
$$
Is defined to be:
$$
\begin{align}
|f(z)-L|<\varepsilon \text{ whenever }|z|\geq M
\end{align}
$$
For some very large number $M$

Similarly to sequences, if $f$ and $g$ are functions with limits $L$ and $M$ at $z_{0}$, then
- $f+\lambda g$ has limit $L+\lambda M$
- $fg$ has limit $LM$

Familiarly, we define continuity to be:
$$
\lim_{ z \to z_{0} } f(z)=f(z_{0})
$$
Given two functions $f$ and $g$, both continuous at the point $z_{0}$, then $f+\lambda g$ and $fg$ are also continuous.
- If $h$ is some functions continuous at each point of some disc centred at the point $w_{0}=f(z_{0})$, then $h(f(z))$ is also continuous at $z_{0}$
- This fact allows us to assert that all polynomials are continuous

Add series notes here