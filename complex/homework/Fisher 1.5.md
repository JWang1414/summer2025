### Question 1
Equivalently
$$
\frac{1}{\sqrt{ 2 }}(1+i)
$$
### Question 2
$$
\frac{1}{\sqrt{ 2 }}(-1-i) = -\frac{1}{\sqrt{ 2 }}(1+i)
$$
### Question 3
$$
\log(1+i\sqrt{ 3 }) = \log |1+i\sqrt{ 3 }| + i \arg(1+i\sqrt{ 3 }) = \log 2 + \frac{i\pi}{3}
$$
### Question 4
In polar coordinates:
$$
-i = e^{ 3\pi i/2 }
$$
Compute
$$
\log -i = \log |e^{ 3\pi i/2 }| + i \arg(e^{ 3\pi i/2 }) = \frac{3\pi i}{2}
$$
### Question 5
$$
(1+i)^i = e^{ \ln(1+i)^i } = e^{ i(\ln(1+i)) }
$$
Evaluating this logarithm
$$
\ln(1+i) = \ln|1+i| + i\arg(1+i) = \ln \sqrt{ 2 } + \frac{i\pi}{4}
$$
Therefore,
$$
e^{ i(\ln \sqrt{ 2 } + i\pi/4) }
$$
### Question 6
$$
\exp(\ln(2^{-1-i})) = \exp \left[ (-1-i)\ln 2 \right] = e^{ -(1+i)\ln 2 }
$$
### Question 7
$$
\frac{1}{2} + \frac{i\sqrt{ 3 }}{2}
$$
### Question 8
$$
e^{ \ln(3+2i) } = 3+2i
$$
### Question 9
$$
\log(4(1-i)) = \log|4(1-i)| + i \arg(4(1-i)) = \log 4\sqrt{ 2 } + i \left( -\frac{\pi}{4} \right) = \log 4\sqrt{ 2 } - \frac{i\pi}{4}
$$
### Question 10
In polar coordinates
$$
-1 = e^{ i\pi }
$$
Therefore
$$
\log (-1) = \log(e^{ i\pi }) = i\pi \log e = i\pi
$$
### Question 11
$$
i^{\sqrt{ 3 }} = e^{ \log(i^{\sqrt{ 3 }}) } = e^{ \sqrt{ 3 } \log i }
$$
Evaluate the exponent
$$
\sqrt{ 3 }\log i = \sqrt{ 3 } \log e^{ i\pi/2 } = \sqrt{ 3 }\left( \frac{i\pi}{2} \right)
$$
The full answer is:
$$
\exp \left[ \frac{\sqrt{ 3 }i\pi}{2} \right]
$$
### Question 12
$$
\log |\sqrt{ 3 }-i| + i \arg(\sqrt{ 3 }-i) = \log 2 + i \left( -\frac{\pi}{6} \right) = \log 2 - \frac{i\pi}{6}
$$
### Question 13
Move the exponent using the properties of the logarithm
$$
\log((1-i)^4) = 4 \log (1-i)
$$
Transform this value into polar coordinates
$$
1-i = \frac{1}{\sqrt{ 2 }} e^{ -i\pi/4 }
$$
Evaluate:
$$
4 \log (1-i) = 4 \log \left( \frac{1}{\sqrt{ 2 }} e^{ i\pi/4 } \right) = 4\left[ \log \frac{1}{\sqrt{ 2 }} + \log e^{ i\pi/4 } \right] = 4 \left[ \log \frac{1}{\sqrt{ 2 }} + \frac{i\pi}{4} \right]
$$
### Question 14
Convert the inside term into polar coordinates
$$
\frac{1}{\sqrt{ 2 }}(1+i) = e^{ i\pi/4 } \implies \left( \frac{i+1}{\sqrt{ 2 }} \right)^4 = (e^{ i\pi/4 })^4 = e^{ i\pi }
$$
And so, the full expression is
$$
\exp \left[ \pi e^{ i\pi } \right] = \exp \left[ -\pi \right] \equiv e^{ -\pi }
$$
### Question 16
---
Using the definition of $\cosh$ and $\sinh$, expand the right side:
$$
\cos x \cosh y-i \sin x\sinh y = \frac{1}{2}\cos x (e^{ y }+e^{ -y }) - \frac{i}{2}\sin x (e^{ y }-e^{ -y })
$$
Factor out the $1 /2$, and expand what remains within the brackets:
$$
\frac{1}{2}\left[ e^{ y }\cos x + e^{ -y }\cos x - ie^{ y }\sin x + i e^{ -y }\sin x \right]
$$
Group the trig functions together, factoring out the exponentials:
$$
\frac{1}{2}\left[ e^{ y }(\cos x-i\sin x) + e^{ -y }(\cos x+i\sin x) \right]
$$
Apply Euler's identity, and simplify the result:
$$
\frac{1}{2}\left[ e^{ y }e^{ -ix } + e^{ -y }e^{ ix } \right]  = \frac{1}{2}\left[ e^{ y-ix } + e^{ ix-y } \right]  = \frac{1}{2}\left[ e^{ -(ix-y) } + e^{ ix-y } \right]
$$
Replacing the existing exponentials with equivalent complex exponentials, we get:
$$
\frac{1}{2}\left[ e^{ -i(x+iy) } + e^{ i(x+iy) } \right] = \cos(x+iy)
$$
---
I assume the other identity is roughly the same thing.
$$
\sin x \cosh y + i \cos x \sinh y = \frac{1}{2}\sin x (e^{ y } + e^{ -y }) + \frac{i}{2} \cos x(e^{ y }-e^{ -y })
$$
$$
\frac{1}{2}\left[ e^{ y }\sin x + e^{ -y }\sin x + i e^{ y }\cos x - i e^{ -y }\cos x \right]
$$
$$
\frac{1}{2}\left[ e^{ y }(\sin x + i \cos x) + e^{ -y }(\sin x - i\cos x) \right]
$$
$$
\frac{i}{2}\left[ e^{ y }(\cos x - i\sin x) - e^{ -y }(\cos x + i\sin x) \right]
$$
$$
\begin{align}
\frac{i}{2}\left[ e^{ y }e^{ -ix } - e^{ -y }e^{ ix } \right]  & = \frac{i}{2}\left[ e^{ y-ix } - e^{ ix-y } \right]  \\
 & =\frac{i}{2}\left[ e^{ i(x+iy) } - e^{ -i(x+iy) } \right]  \\
 & =\sin(x+iy)
\end{align}
$$
### Question 20
Fix $z\in \mathbb{C}$. Notice that:
$$
\cos ^{2}z+\sin ^{2}z = (\cos z)^{2}+(\sin z)^{2} = (\cos z+i \sin z)(\cos z -i \sin z)
$$
Applying Euler's identity, we have:
$$
\cos ^{2}z + \sin ^{2}z = e^{ iz }e^{ -iz } = e^{ iz }\overline{e^{ iz }} = |e^{ iz }|
$$
It is known that, for all $z$:
$$
|e^{ iz }| = 1
$$
### Question 22
For $\sin z$
$$
\sin(-z) = \frac{i}{2} \left( e^{ -i(-z) } - e^{ i(-z) } \right) = \frac{i}{2} \left( e^{ iz } - e^{ -iz } \right) = -\frac{i}{2} \left( e^{ -iz } - e^{ iz } \right) = -\sin z
$$
As needed.

For $\cos z$
$$
\cos(-z) = \frac{1}{2}\left( e^{ -i(-z) } + e^{ i(-z) } \right) = \frac{1}{2} \left( e^{ iz } + e^{ -iz } \right) = \cos z
$$
As needed.
