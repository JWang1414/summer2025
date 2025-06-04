Assigned homework questions: 1-15
### Question 1
Square plane in the fourth quadrant, closed, connected
### Question 2
Two circles, one centred at $(0, 0)$, and another at $(3, 0)$. One circle is open, the other is closed. This set is not connected
### Question 3
A parabola within the first and second quadrants. Looks like a large cartoon rain drop. This set is open, and the interior is connected
### Question 4
Two vertical lines at $x=\pm 2$, where $x$ is the real part of $z$. Closed, not connected.
### Question 5
This set contains $\mathbb{C}$, but has a small disk of radius 2 in the centre that is not in the set. Closed, connected.
### Question 6
A set of three distinct points, the complex roots of this function. Neither open or closed, not connected.
### Question 7
A half-plane containing quadrants two and three. This half-plane omits a small disk centred at $(-1, 0)$. Neither open nor closed, connected.
### Question 8
A thin horizontal strip across the complex plane. Neither open nor closed, connected.
### Question 9
---
a.
Multiplication by a complex number, or, the set $\alpha z$, will result in the first quadrant being rotated around the origin, and sheared by some amount. The resulting shape will look somewhat similar to a trapezoid.

Afterwards, the set $\alpha z+\beta$ will simply be the resultant set shifted around the complex plane by some constant value. This set remains open and connected, like the original quadrant

---
b.
In this case, the set $\alpha z$ will result in the half-plane being rotated about the origin, but no shearing will occur. The resultant set remains open and connected.

The addition of a constant will, once again, shift around the new half-plane by some constant value. The final set is open and connected

---
c.
Disks do not change under rotation, and so after multiplication by a complex number, only the radius of the disk will change. The resulting radius of $\alpha z$ will be $|\alpha|$.

$\alpha z+\beta$ is the same thing as before, the disk shifted around the plane. The final set is open and connected

---
### Question 10
In polar coordinates, the second quadrant is expressed as the set
$$
\left\{  z=re^{ i\theta } : \frac{\pi}{2}<\theta<\pi  \right\}
$$
Compute the difference after being squared:
$$
(re^{ i\theta })^{2} = r^{2}e^{ 2i\theta }
$$
Substituting the values $R=r^{2}$ and $\phi=2\theta$, we have the new set
$$
\left\{  z = r^{2}e^{ 2i\theta } : \frac{\pi}{2}<\theta<\pi  \right\} \Rightarrow \{ z = R e^{ i\phi } : \pi<\phi<2\pi \}
$$
Which makes it clear that the new region is the lower half-plane
### Question 11
$B$ and $F$ are bounded. The rest are unbounded.
### Question 12
$E$ contains $\infty$
### Question 13
---
a.
Define the two nonempty open sets $A, B\subseteq \mathbb{C}$. Define the new set $S=A\cap B$.

The new boundary will be defined by the boundary of $A$ and the boundary of $B$, with the parts included in both $A$ and $B$ removed. This can be formalized as:
$$
\partial S = (\partial A\setminus B)\cap(\partial B\setminus A)
$$
Notice that, the portion of the boundary around $A$ is not contained in $S$, and the portion of the boundary around $B$, is also not contained in $S$. This is the full boundary, and since none of it is contained with in $S$, it must be an open set.

---
The version with closed sets is all the same. Instead, you show that the boundary is contained in $S$, instead of not contained in $S$

---
In this case, the boundary definition would change to be around the intersection instead of the union, but it's also very similar.

---
b.
For a finite number of sets, the boundary would be increasingly complex, but since there is a finite number of open sets, you will always be able to define a boundary around all objects in the set. The same thing is repeated. This boundary is always not in the set, in the set, or whatever.
### Question 14
Since we know $D_{1}$ and $D_{2}$ are open sets, we can also be certain that $D_{1}\cap D_{2}$ will be another open set. Furthermore, since they have a non-empty intersection, a polygonal can be drawn across their intersection to connect any given point in $D_{1}$ and $D_{2}$. Therefore, $D_{1}\cap D_{2}$ is an open, connected set. That is, it is a domain
### Question 15
The sets $\Omega_{1}$ and $\Omega_{2}$ are defined with strict inequalities, and connected. They are open, connected sets, and therefore domains.

$\Omega_{1}\cup \Omega_{2}$ is not a domain because it results in two separated regions. A polygonal curve cannot be drawn between the two, and so although the set is open, it is not connected. Therefore, it is not a domain.