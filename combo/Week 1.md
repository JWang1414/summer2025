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
