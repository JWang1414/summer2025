For $r>0$ and $z_{0}\in \mathbb{C}$, we define the *open disk*, of radius $r$ centred at $z_{0}$ as:
$$
D_{r}(z_{0}) = \{ z\in \mathbb{C} : |z-z_{0}|<r \}
$$
A subset $S\subseteq \mathbb{C}$ is *open* if
$$
\forall z_{0}\in S, \exists r>0 s.t. D_{r}(z_{0})\subseteq S
$$
- For all points in the set, it is possible to find a small disk that still fits within the plane
- Think about how you can dissect real numbers into infinitely small chunks. If we specify a boundary with a strict inequality, then it's probably open
On the contrary, if it is not open, it is *closed*
- A boundary specified with a non-strict inequality, for example, will likely result in this
A *closed disk* is specified as:
$$
\overline{D_{r}(z_{0})} = \{ z\in \mathbb{C} : |z-z_{0}| \leq r \}
$$
For some subset $S\subseteq \mathbb{C}$, its boundary, denoted as $\partial S$ is the set of all points $z_{0}\in \mathbb{C}$ such that every open disk around $z_{0}$ contains points in $S$ and not in $S$
- "Not in $S$" is sometimes denoted as: $S^c$, the complement of $S$
- $\partial S$ does not have to be in $S$
- $\partial S = \partial S^c$
- The boundary for an open disk is basically the area surrounding the edges
A set can also considered to be closed if it contains all of its boundary points

The *closure* of a set $S\subseteq \mathbb{C}$ is $S\cup \partial S$
- The closure of a closed set is itself

The interior of $S\subseteq \mathbb{C}$ are the points in $S$ that are not in the boundary
- $S\setminus \partial S$

Other notes:
- It appears there are strange exceptions, like $\mathbb{C}$, $\emptyset$, and a single point, which are all considered to be open and closed
- It is possible to have a set that is not open and not closed

Consequential theorems:
1. $S$ is open $\iff$ $S\cap \partial S = \emptyset$
2. $S$ is closed $\iff$ $S^c$ is open

A set $S\subseteq \mathbb{C}$ is *connected* if $\forall p,q\in S$ there is a *polygonal path* between $p$ and $q$
- A polygonal path is a series of straight lines, like a zig-zag
- Continuous paths also work, but we have not defined those yet
- DRAWING SOME DIAGRAMS MIGHT HELP HERE
