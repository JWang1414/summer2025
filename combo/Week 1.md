How many 6 letter combinations can we make in the English languages? Answer: $26^6$ combinations.

We know this because this combination of letters is called an order 6 *tuple*

We can formalize this by calling $x_{n}\in X$ where the set $X$ is the English alphabet. So, our 6 letter combination is a function defined as:
$$
f: \left\{ 1,2,3,4,5,6 \right\} \to X
$$

Def:

Let $n\in \mathbb{N}$, then $[n]:=\left\{ 1,2,3,\dots,n \right\}$

We are interested in the size of the set such that
$$
\left\{ f:[6]\to X, |X|=26 \right\}
$$
So, how many functions that make 6 letters into the English alphabet? We already solved this question
$$
\left| \left\{ f:[6]\to X, |X|=26 \right\}  \right| = 26^6
$$
What if we have no repeat letters?
$$
\left| \left\{ f:[n]\to X : f\text{ is injective} \right\}  \right|  = \frac{|X|!}{(|X|-n)!}
$$

Definition of *injective*

Let $X,Y$ be non-empty sets. Then, $f:X\to Y$ is called 1-1 or injective if
$$
\forall a,b\in X, f(a)=f(b) \Rightarrow a=b
$$

Definition of onto or *surjective*
$$
\forall y \in Y, \exists x\in X s.t. f(x)=y
$$
A function is called onto a set $Y$, if for every value in $Y$, you can find a value in that function that corresponds to it

If a function is injective and surjective, or onto and 1-1, then it is called bijective. If $|X|=|Y|=n$, then a bijection is also called a permutation $(\sigma)$

Define $m,n\in \mathbb{N}$, $m\geq n$, then the number of permutations
$$
P(m,n) = \left| \left\{ f:[n]\to[m], f\text{ is 1-1} \right\} \right| = \frac{m!}{(m-n)!}
$$
This is the exact same as the example with the alphabet!

Define a set $X$ such that $|X|=n$. Then, how many subsets of length $k$ can you make from the original set $X?$ Assume $0\leq k\leq n$.
$$
\begin{pmatrix}
n \\
k
\end{pmatrix} = \frac{n!}{k!(n-k)!}
$$

Example: Let $X=\left\{ a, b, c, d \right\}$. Let $A=\left\{ b, d \right\}$; $B=\left\{ a, b \right\}$, $A, B\subseteq X$.

Lets enumerate $X$ to make it a little easier to read: $X\to \{ x_{1}, x_{2}, x_{3}, x_{4} \}$.

Under this enumeration, $A$ can be identified by $\{ x_{2}, x_{4} \}\to(0, 1, 0, 1)$

Define the cartesian product:
- Let $X, Y$ be sets. Then $X\times Y = \{ (x, y) : x\in X, y\in Y \}$

Expanding the cartesian product to $n$ number of sets, we have
$$
X_{1}\times X_{2}\times\cdots \equiv \{ (x_{1}, x_{2}, \dots, x_{n}) : x_{i}\in X_{i}, i\in \mathbb{N} \}
$$
Uniquely, we denote $X\times X\times\cdots \equiv X^n$

Note that $f : [n]\to X$ is bijective to $(f(1), f(2), \dots, f(n))\in X^n$

Definition of an enumeration:

Let $X$ be a finite set with $|X|=n$, then a bijection $h : [n]\to X$ is called an enumeration of $X$

Definition of a power set

Let $X$ be a set. Then, $\mathcal{P}(x)=\{ A\subseteq X \}$ is the power set of $X$

Theorem: Let $X$ be a finite set such that $|X|=n$. Then, there is a bijection between $\mathcal{P}(x)$ and $\{ 0,1 \}^n$
