## Special Relativity
Einstein's Special Theory of Relativity follows from two postulates:
1. The laws of physics are the same in all inertial (non-accelerating)
   reference frames.
2. The speed of light in vacuum

   $$
   c = 299\ 792\ 458~{\rm m/s} \approx 3.00 \times 10^8~{\rm m/s}
   $$
   is the same in all inertial reference frames.

The second postulate follows from Maxwell's equations of
electromagnetism, which imply that waves of the electromagnetic field
propagate at the speed of light. Since Maxwell's equations do not
promote any special inertial reference frame, this speed of
propagation must be independent of reference frame. This causes a
problem for classical physics, since the classical relativity, or
**Galilean relativity**, implies

$$
v_{\rm rel} = v_1 - v_2
$$
for the relative velocity $v_{\rm rel}$ between two objects moving at
speeds $v_1$ and $v_2$. For instance, if two cars are driving down the
highway at speeds $v_1 = 25~{\rm m/s}$ and $v_2 = 30~{\rm m/s}$ in the
same direction, then the relative speed of car 1 to car 2 is
$-5~{\rm m/s}$. But if we had a near lightspeed car that traveled at
speed $0.90c$ traveling in the same direction as a beam of light from
its own headlights, then the relative velocity, according to Galilean
relativity, is $0.1c$. But this cannot be, since light must always
travel at speed $c$ according to Maxwell's equations.

The way out of this philosophical mess is to examine the assumptions
of Galilean relativity. Let's say we have an object (say, a rock)
sitting at position $x$ at rest in one reference frame $\mathcal{S}$.
Let us also consider that resting on the rock is a watch that someone
abandoned, ticking at the correct time. For a moving reference frame
$\mathcal{S}'$ moving at speed $v$ in the $+x$-direction and whose
origin lines up with $\mathcal{S}$ at $t=0$, the coordinates for the
rock are seen in the Galilean paradigm as

$$
t' = t,\qquad x' = x-vt.
$$
The first equation seems like a tautology – of course the rock's time looks no different in the moving frame! However, due to the
invariance of the speed of light with respect change in reference
frame, we have to challenge this assumption. Since the invariant thing
is a *speed*, we have to consider that a change to a position to a
change in reference frame must be compensated by a change in temporal
position, or, if you prefer, a change in clock reading.
<!-- Insert light clock argument! -->
Consider a **light clock** – an object that bounces a short pulse of
light between two mirrors set a certain distance $L$ apart which
ticks time forward after every round trip of the light pulse.
![]()

$$
r'^\mu = {\Lambda^\mu}_\nu r^\nu
$$ (eq:4-vec-transform)
where ${\Lambda^\mu}_\nu$ is the standard Lorentz transformation
matrix. For boosts in the $r^1 = x$ direction, $\Lambda$ takes the
form

$$
\Lambda =
\begin{pmatrix}
\gamma & -\gamma\beta & 0 & 0 \\
-\gamma\beta & \gamma & 0 & 0 \\
0 & 0 & 1 & 0\\
0 & 0 & 0 & 1
\end{pmatrix}
$$ (eq:lorentz-boost-x)
with $\gamma$ as the standard Lorentz factor. Carrying out the matrix
multiplication yields the set of transformations

$$
ct' = \gamma (ct - \beta x), \qquad
x' = \gamma (x - \beta ct), \qquad
y' = y, \qquad
z' = z,
$$