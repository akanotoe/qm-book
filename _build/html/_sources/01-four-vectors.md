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
$$ (eq:contravar-transformation)
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
rotations.[^time-rotation] For example, the inner product of the position
four-vector with itself gives the invariant quantity

$$
(ct)^2 - x^2 - y^2 - z^2.
$$
if we have two events in spacetime separated in time by $\Delta t$ and in space
by $\Delta \mathbf{r}$, we get the quantity known as the **spacetime interval**

$$
(\Delta s)^2 = (c\Delta t)^2 - (\Delta \mathbf{r})^2 = (c\Delta t)^2 -
(\Delta x)^2 - (\Delta y)^2 - (\Delta z)^2,
$$
where the sign of $\Delta s$ describes how the two events are separated.

$$
\begin{cases}
\Delta s > 0 & \text{timelike separated}\\
\Delta s = 0 & \text{lightlike separated}\\
\Delta s < 0 & \text{spacelike separated}.
\end{cases}
$$
Under Lorentz transformations, events that are timelike separated can occur in
the same place, but never simultaneously, whereas spacelike separated events
can occur simultaneously, but never at the same location.

### The Metric
As a shorthand, we can keep track of the negative
signs in the inner product with the (**Minkowski**) **metric**,[^metric-conv]

$$
\eta_{\mu\nu} = \eta^{\mu\nu} =
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
which has its spatial components (1, 2, 3) flipped in sign but the temporal
component preserved. Note that under Lorentz transformations, covariant vectors
transform according to the rule

$$
a'_\nu = \eta_{\rho\nu}{\Lambda^\rho}_\sigma \eta^{\mu\sigma} a_\mu =
{(\Lambda^{-1})^\mu}_\nu a^{}_\mu.
$$ (eq:covar-transform)
The four-vectors with upper indices we worked with earlier are known as
**contravariant vectors**. Contracting a covariant vector with a contravariant
vector gives the inner product

$$
\eta_{\mu\nu}a^\mu b^\nu = a^\mu b_\mu = a_\mu b^\mu =
a^0b^0 - a^1b^1 - a^2b^2 - a^3b^3.
$$
This notation requires care with the upperness or lowerness of the indices on
four-vectors. Because the index is repeated in the inner product, and that the
upperness of the first vector cancels with the lowerness of the second, we end
up with a *scalar product* (one component). The combination $a^\mu b^\nu$,
which neither repeats indices nor mixes upper and lower indices, is a
second-rank **tensor** ($T^{\mu\nu}$) which is *contravariant* in both indices.
This object transforms as

$$
{a'}^\mu{b'}^\nu = ({\Lambda^\mu}_\rho a^\rho) ({\Lambda^\nu}_\sigma b^\sigma)=
{\Lambda^\mu}_\rho {\Lambda^\nu}_\sigma T^{\rho\sigma}.
$$
Using the metric, we can mix contravariance and covariance in tensors:

$$
\eta_{\nu\rho}T^{\mu\rho} = {T^\mu}_\nu.
$$

#### Momentum 4-vector
Velocity in special relativity follows the Einstein velocity addition rule
(Eq. [](eq:einstein-vel)), which means that velocity is not a four-vector. What
is needed is either a distance or a time which can be agreed upon by all
inertial reference frames. If you are moving with some velocity $u$ relative to
Earth, the clock on your wall reads time in the *lab frame*, while the watch on
your wrist reads your **proper time**,

$$
d\tau = \sqrt{1-u^2/c^2}\,dt.
$$ (eq:proper-time)
The lab time depends on your speed $u$, but everyone can use the equations for
Lorentz transformations to determine your proper time. Thus, proper time is an
*invariant*. In fact, for an object at rest ($dx = dy = dz = 0$) the proper
time is the spacetime invariant,

$$
dr^\mu dr_\mu = (c\,dt)^2 - (dx)^2 - (dy)^2 - (dz)^2 = (c\,d\tau)^2\quad
\text{(rest frame)}.
$$
This means that the quantity

$$
w^\mu = \frac{dr^\mu}{d\tau}
$$
transforms as a four-vector,

$$
{w'}^\mu = {\Lambda^\mu}_\nu w^\nu.
$$
We call $w^\mu$ the **proper velocity** four-vector. Its zeroth (temporal)
component is

$$
w^0 = \frac{dr^0}{d\tau} = c\frac{dt}{d\tau} = \gamma c
$$
and its inner product with itself is

$$
w^\mu w_\mu = \gamma^2(c^2 - v^2) = c^2
$$
which is invariant (as it should be!). The momentum four-vector is mass times
proper velocity:

$$
p^\mu = m w^\mu = \gamma m
\begin{pmatrix}
c \\ w_x \\ w_y \\ w_z
\end{pmatrix}.
$$
Defining $p^0 = E/c$ as the relativistic energy (divided by $c$), we get

$$
p^\mu =
\begin{pmatrix}
E/c \\ p_x \\ p_y \\ p_z
\end{pmatrix}
$$
with

$$
E = \gamma mc^2.
$$
When an object is at rest ($\gamma = 1$), the energy is nonzero. We define the
rest energy as

$$
E_{\rm rest} = mc^2.
$$ (eq:Emc2)
The **kinetic energy** is the total energy minus the rest energy,

$$
E_{\rm kin} = E - mc^2 = (\gamma - 1)mc^2.
$$
Note that in the nonrelativistic limit, the kinetic energy is

$$
E_{\rm kin} = \left(1 + \frac{1}{2}\frac{v^2}{c^2} +\ldots -1 \right) mc^2
\simeq \frac{1}{2}mv^2
$$
which matches the classical kinetic energy. Additionally, the inner product of
the momentum four-vector with itself is

$$
p^\mu p_\mu = \left(\frac{E}{c}\right)^2 - p^2 = (mc)^2,
$$ (eq:pmu-pmu)
which is known as the **relativistic energy-momentum relation**.

[^superscript]: Here superscripts are an index rather than an exponent. In
special relativity, we have to be explicit about exponents vs. upper indices.

[^einstein-sum]: Einstein apparently  considered this one of his greatest
contributions.

[^time-rotation]: Lorentz transformations can be considered **time rotations**.

[^metric-conv]: The spacetime metric merely needs the spatial components to
have an opposite sign compared to the time component. The matrix
$\operatorname{diag}(-1, 1, 1, 1)$ is an equally valid convention that is more
common in general relativity. This text uses the metric more common in particle
physics and quantum field theory.