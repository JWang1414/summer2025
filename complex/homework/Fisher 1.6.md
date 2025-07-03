Questions 1-10
### Question 1
Parametrize the curve with $\gamma(t)=e^{ it }$ where $t \in[\pi /2, 3\pi /2]$

Recall that line integrals can be computed as:
$$
\int_{\gamma} u(z) \, dz = \int_{a}^{b} u(\gamma(t))\gamma'(t) \, dt
$$
The derivative of this parametrization is:
$$
\gamma'(t)=ie^{ it }
$$
The line integral is now:
$$
\int_{\pi /2}^{3\pi  /2} e^{ it }(ie^{ it }) \, dt = i \int_{\pi /2}^{3\pi /2} e^{ 2it } \, dt = \frac{i}{2i} \left[ e^{ 2it } \right] ^{3\pi /2}_{\pi /2} =0
$$
### Question 2
Let $z,w\in \mathbb{C}$, the straight line from $z$ to $w$ has parametrization
$$
\gamma(t) = (1-t)z+tw\text{, with }t\in[0,1]
$$
Therefore, in this case, we have $\gamma(t)=(1-t)(0)+tz_{0}=tz_{0}$

The line integral is:
$$
\int_{0}^{1} e^{ tz_{0} }z_{0} \, dt = z_{0} \int_{0}^{1} e^{ tz_{0} } \, dt = z_{0} \left[ \frac{1}{z_{0}}e^{ tz_{0} } \right] ^1_{0} = \left[ e^{ tz_{0} } \right] ^1_{0} = e^{ z_{0} } - e^{ 0 } = e^{ z_{0} }-1
$$
### Question 3
Parametrize:
$$
\gamma(t) = (1-t)(2) + t(3+i) = 2+(1+i)t
$$
Derivative:
$$
\gamma'(t) = 1+i
$$
Line integral:
$$
\int_{0}^{1} |2+(1+i)t|^{2}(1+i) \, dt = (1+i) \int_{0}^{1} 2t^{2}+4t+4 \, dt
$$
Split this integral calculation:
$$
2 \int_{0}^{1} t^{2} \, dt = 2 \left[ \frac{t^3}{3} \right] ^1_{0} = \frac{2}{3}
$$
$$
4 \int_{0}^{1} t \, dt = 4 \left[ \frac{t^2}{2} \right] ^1_{0} = 2
$$
$$
4 \int_{0}^{1}  \, dt = 4
$$
Sub back into the original problem:
$$
(1+i) \left[ \frac{2}{3} + 2 + 4 \right] = \frac{20}{3} (1+i)
$$
### Question 4
Parametrize:
$$
\gamma(t) = e^{ it }-4 \implies \gamma'(t) = ie^{ it }
$$
Line integral:
$$
\int_{0}^{2\pi} \frac{1}{e^{ it }-4+4}(ie^{ it }) \, dt = \int_{0}^{2\pi} \frac{1}{e^{ it }}(ie^{ it }) \, dt = i \int_{0}^{2\pi}  \, dt = 2\pi i
$$
### Question 5
Parametrize:
$$
\gamma(t) = (1-t)(1) + t(i) = 1-t+ti \implies \gamma'(t) = -1+i
$$
Line integral:
$$
\int_{0}^{1} \mathrm{Re}\left\{ 1-t+ti \right\} (-1+i) \, dt = (-1+i) \int_{0}^{1} 1-t \, dt
$$
Compute:
$$
\int_{0}^{1} 1 \, dt = 1
$$
$$
\int_{0}^{1} -t \, dt = - \int_{0}^{1} t \, dt = - \left[ \frac{t^2}{2} \right] ^1_{0} = -\frac{1}{2}
$$
Sub back in:
$$
(-1+i) \left[ 1-\frac{1}{2} \right] = \frac{1}{2} (i-1)
$$
### Question 6
Parametrize:
$$
\gamma(t) = 2e^{ it } \implies \gamma'(t) = 2ie^{ it }
$$
Line integral:
$$
\int_{0}^{2\pi} \left[ (2e^{ it })^{2} + 3(2e^{ it }) + 4 \right](2ie^{ it })  \, dt = 2i \int_{0}^{2\pi} \left[ 4e^{ 2it } + 6e^{ it } + 4 \right] e^{ it } \, dt
$$
Compute:
$$
\int_{0}^{2\pi} 4e^{ 2it }e^{ it } \, dt = 4 \int_{0}^{2\pi} e^{ 3it } \, dt = \frac{4}{3i} \left[ e^{ 3it } \right] ^{2\pi}_{0} = 0
$$
$$
\int_{0}^{2\pi} 6e^{ it }e^{ it } \, dt = 6 \int_{0}^{2\pi} e^{ 2it } \, dt = \frac{6}{2i} \left[ e^{ 2it } \right] ^{2\pi}_{0} =0
$$
$$
\int_{0}^{2\pi} 4e^{ it } \, dt = 4 \int_{0}^{2\pi} e^{ it } \, dt = \frac{4}{i} \left[ e^{ it } \right] ^{2\pi}_{0} = 0
$$
Sub back in:
$$
2i(0+0+0) = 0
$$
### Question 7
Because $z^{2}$ is a holomorphic function, its integrals are independent of our choice of parametrization, and do not depend on the curve, only the start and end points. However, $\bar{z}$ is not a holomorphic function, and so this does not apply.
### Question 8
- This question looks very boring and do not want to do it after completing all those other line integrals already
### Question 9
---
a.
$$
\frac{1}{2\pi} \int_{0}^{2\pi} e^{ ik\theta } \, d\theta = \frac{1}{2\pi ik} \left[ e^{ ik\theta } \right] ^{2\pi}_{0} = \frac{1}{2\pi ik} \left[ e^{ 2\pi ik } - 1 \right] =0
$$
This is zero, but cannot be evaluated in the case when $k=0$. Isolating this case, we can compute:
$$
\frac{1}{2\pi} \int_{0}^{2\pi} e^{ 0 } \, d\theta = \frac{1}{2\pi} \int_{0}^{2\pi}  \, d\theta =1
$$
As needed.

---
b.
Parametrize the circle:
$$
\gamma(t) = e^{ it } \implies \gamma'(t) = ie^{ it }
$$
We are interested in proving:
$$
\frac{1}{2\pi i} \int_{\gamma} \frac{1}{z-p} \, dz = \begin{cases}
0 & \text{if }p\text{ is outside }\gamma \\
1 & \text{if }p\text{ is inside } \gamma
\end{cases}
$$
Re-write the integral with the parametrization:
$$
\frac{1}{2\pi i} \int_{0}^{2\pi} \frac{ie^{ it }}{e^{ it }-p} \, dt = \frac{1}{2\pi} \int_{0}^{2\pi} \frac{e^{ it }}{e^{ it }-p} \, dt
$$
Since $|e^{ it }|=1$. We can apply the summation identities.

Case 1: $0\leq |p|<1$
- In this case, $p$ is inside the boundary
$$
\frac{1}{2\pi} \int_{0}^{2\pi} e^{ it } \sum_{k=0}^{\infty} \frac{p^k}{e^{ i(k+1)t }} \, dt = \frac{1}{2\pi} \int_{0}^{2\pi} \sum_{k=0}^{\infty} \frac{p^k}{e^{ ikt }} \, dt = \sum_{k=0}^{\infty} p^k \left[ \frac{1}{2\pi} \int_{0}^{2\pi} e^{ -ikt } \, dt  \right]
$$
Since the summation term collapses to the single term with $k=0$, the final answer is $p^0=1$. As needed.

Case 2: $1<|p|<\infty$
- In this case, $p$ is outside the boundary
$$
\frac{1}{2\pi} \int_{0}^{2\pi} e^{ it }\left[ -\sum_{k=0}^{\infty} \frac{e^{ ikt }}{p^{k+1}} \right]  \, dt = -\frac{1}{2\pi} \int_{0}^{2\pi} \sum_{k=0}^{\infty} \frac{e^{ i(k+1)t }}{p^{k+1}} \, dt = - \sum_{k=0}^{\infty} p^{-k-1} \left[ \frac{1}{2\pi} \int_{0}^{2\pi} e^{ i(k+1)t } \, dt  \right]
$$
In this case, notice that $k$ will never be 0, and therefore all terms of the summation collapse to 0. As needed.

---
### Question 10
- This question looks hard and I'm kind of tired so I don't wanna do it
