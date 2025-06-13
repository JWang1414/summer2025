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
### Infinite Series
An $n$th partial sum is defined as:
$$
s_{n} = \sum_{i=1}^{n} z_{i} = z_{1}+z_{2}+\dots z_{n}
$$
Just like real series, for complex, the infinite series is this same sum for $n\to \infty$.
- Definitions of convergent and divergent sums are as expected

For complex numbers, we can defined $z_{j} = x_{j}+i y_{j}$. Which leads us to:
$$
s_{n} = \sum_{j=1}^{n} z_{j} = \sum_{j=1}^{n} x_{j} + i \sum_{j=1}^{n} y_{j} \equiv \sigma_{n}+i\tau_{n}
$$
Where we have defined the two sequences $\{ \sigma_{n} \}$ and $\{ \tau_{n} \}$.
- Note that $\{ s_{n} \}$ converges only if both of these sequences converge
- $s = \lim_{ n \to \infty } s_{n} = \lim_{ n \to \infty }\sigma_{n} + i \lim_{ n \to \infty }\tau_{n}$

Recall a property of series:
$$
|s_{n}| = \left| \sum_{j=1}^{n} z_{j} \right| \leq \sum_{j=1}^{n} \left| z_{j} \right|
$$
- If $\sum|z_{j}|$ converges, then the series is called *absolutely convergent*, and $\sum z_{j}$ also converges
### Geometric Series
Recall the identity
$$
1+x+x^{2}+\dots+x^n = \frac{1-x^{n+1}}{1-x}
$$
Which is valid for any $x \in \mathbb{R}$ and $x\neq 0$

If we, say, differentiation both sides with respect to $x$, multiply both sides by $x$, and add 1, then the results is
$$
1+x+2x^{2}+3x^{3}+\dots+nx^n = 1-(n+1) \frac{x^{n+1}}{1-x} + x \frac{1-x^{n+1}}{(1-x)^{2}}
$$
The same steps can be repeated again to receive an identity for the series $n^2x^n$
