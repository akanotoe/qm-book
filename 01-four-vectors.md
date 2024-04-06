### Four-vectors
We can simplify the Lorentz transformations by defining the
quantities[^superscript]

$$
r^0 = ct, \qquad r^1 = x, \qquad r^2 = y, \qquad r^3 = z,
\qquad \beta = \frac{v}{c}.
$$
Note that $ct$ is the distance light travels in $t$ units of time. By reframing
time in terms of distance, we can express the Lorentz transformations as

$$
\left.
\begin{array}{l}
{r'}^0 = \gamma(r^0 - \beta r^1)\\[8pt]
{r'}^1 = \gamma(r^1 - \beta r^0)\\[8pt]
{r'}^2 = r^2 \\[8pt]
{r'}^3 = r^3.
\end{array}
\right\}
$$
Putting this in matrix form, we get

$$
\begin{pmatrix}
ct' \\ x' \\ y' \\ z'
\end{pmatrix}
=
\begin{pmatrix}
\gamma & -\gamma\beta & 0 & 0 \\
-\gamma\beta & \gamma & 0 & 0 \\
0 & 0 & 1 & 0 \\
0 & 0 & 0 & 1
\end{pmatrix}
\begin{pmatrix}
ct \\ x \\ y \\ z
\end{pmatrix}
$$
We can write this using summation notation letting Greek letter indices run
from 0 to 3,

$$
{r'}^\mu = \sum_{\nu = 0}^3 ({\Lambda^\mu}_\nu)r^\nu,
$$
where we define $\Lambda$ as the **Lorentz transformation matrix**. The index
$\mu$ indicates the row, while $\nu$ indicates the column. This can be further
simplified by the **Einstein summation convention**[^einstein-sum], where
summation is implied over any Greek index that is repeated. Under this
convention, the matrix multiplication is written as

$$
{r'}^\mu = {\Lambda^\mu}_\nu r^\nu.
$$ (eq:4-vec-transform)
One advantage of this reframing of the Lorentz transformations is that a
general Lorentz transformation takes this form, not just Lorentz
transformations along the $x$-axis. Additionally, we can define *any*
four-vector $a^\mu$ as an object that transforms according to
Eq. [](eq:4-vec-transform),

$$
{a'}^\mu = {\Lambda^\mu}_\nu a^\nu.
$$
Like normal vectors, four-vectors have an analog to the dot product (or inner
product), given by

$$
a^0b^0 - a^1b^1 - a^2b^2 - a^3b^3.
$$
This inner product is *invariant* under Lorentz transformation,

$$
{a'}^0{b'}^0 - {a'}^1{b'}^1 - {a'}^2{b'}^2 - {a'}^3{b'}^3 =
a^0b^0 - a^1b^1 - a^2b^2 - a^3b^3,
$$
the same way that normal (3-)vectors are invariant under spatial
rotations.[^time-rotation] As a shorthand, we can keep track of the negative
signs in the inner product with the (**Minkowski**) **metric**,

$$
\eta_{\mu\nu} =
\left(
\begin{array}{rrrr}
1 & 0 & 0 & 0 \\
0 & -1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{array}
\right)
$$
so that

$$
a^0b^0 - a^1b^1 - a^2b^2 - a^3b^3 =
\eta_{\mu\nu}a^\mu b^\nu.
$$
Using the metric, we can define the **covariant vector**

$$
a_\mu = \eta_{\mu\nu} a^\nu,
$$
which we contract with a **contravariant vector** $b^\mu$ to get the inner
product

$$
\eta_{\mu\nu}a^\mu b^\nu = a^\mu b_\mu = a_\mu b^\mu =
a^0b^0 - a^1b^1 - a^2b^2 - a^3b^3.
$$
This notation requires care with the upperness or lowerness of the indices on
four-vectors. Because the index is repeated in the inner product, and that the
upperness of the first vector cancels with the lowerness of the second, we end
up with a *scalar product* (one component). The combination
$a^\mu b^\nu$
is a second-rank **tensor** ($T^{\mu\nu}$) since there is no repeated index.
This object transforms as

$$
{a'}^\mu{b'}^\nu = ({\Lambda^\mu}_\rho a^\rho) ({\Lambda^\nu}_\sigma b^\sigma)=
{\Lambda^\mu}_\rho {\Lambda^\nu}_\sigma T^{\rho\sigma}.
$$

[^superscript]: Here superscripts are an index rather than an exponent. In
special relativity, we have to be explicit about exponents vs. upper indices.

[^einstein-sum]: Einstein apparently  considered this one of his greatest
contributions.

[^time-rotation]: Lorentz transformations can be considered **time rotations**.