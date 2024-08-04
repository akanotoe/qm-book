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
$$ (eq:rel-vel-gal)
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
$$ (eq:galilean-transformations)
The first equation seems like a tautology – of course the rock's time looks no
different in the moving frame! However, due to the invariance of the speed of
light with respect change in reference frame, we have to challenge this
assumption. Since the invariant thing is a *speed*, we have to consider that a
change to a position to a change in reference frame must be compensated by a
change in temporal position, or, if you prefer, a change in clock reading.
<!-- Insert light clock argument! -->
Consider a **light clock** – an object that bounces a short pulse of
light between two mirrors set a certain distance $L$ apart which
ticks time forward after every round trip of the light pulse.
![]()

When the clock is at rest, the light clock ticks after the light pulse travels
a distance of $2L$,

$$
c\Delta t = 2L.
$$
When the light clock travels in the $+x$-direction at a velocity $v$, the light
makes a round trip to tick after it travels a distance

$$
c\Delta t' = 2\sqrt{L^2 + \left(\frac{v\Delta t'}{2}\right)^2}.
$$
With a little algebra, this produces a relationship between the ticking period
in the rest frame ($\Delta t$) and in the laboratory frame ($\Delta t'$),

$$
\Delta t' = \gamma \Delta t
$$ (eq:time-dilation)
where the quantity $\gamma$ is known as the *Lorentz factor*, defined as

$$
\gamma = \dfrac{1}{\sqrt{1-v^2/c^2}}
$$(eq:lorentz-factor)
The conclusion drawn from these relations is that *moving clocks tick more
slowly*, since $\gamma \ge 1$ for all velocities $v$. The name for this
phenomenon is **time dilation**. We can glean another relation for lengths by
turning the light clock on its side. In this scenario, when at rest, the length
of the light clock is simply

$$
L = c\Delta t.
$$
When the light clock travels at velocity $v$ in the $+x$-direction, the
distance traveled per tick is related by

$$
\frac{L'}{c-v} + \frac{L'}{c+v} = \Delta t'.
$$
After some algebra, the relationship between $L$ and $L'$ is

$$
L' = \frac{L}{\gamma}.
$$ (eq:length-contraction)
The conclusion here is that *moving objects appear shorter*. This is the
phenomenon of **length contraction** for moving objects.

As a quick aside, these are very subtle effects for everyday motion.
Considering even the fastest everyday speeds, like traveling on an airplane,
we get $v \sim 300~\text{m/s} \sim 10^{-6} c$. For small $v/c$, the binomial
theorem approximates the Lorentz factor as about $1 + v/2c$ which means that
the difference between rest times and lengths to moving times and lengths would
only be about 500 parts per billion. A one foot ruler would only contract by
a fraction of the length of a bacterium. It's only when an object approaches a
significant fraction of the speed of light that these effects are noticeable.

Using these relationships of lengths and time intervals between rest frame and
lab frame, we can transform coordinates between the two frames. Let's consider
the light clock on its side and track the rightmost side of the light clock as
being at coordinates $(t, x)$ in  the lab frame $\mathcal{S}$ while it has the
coordinates $(t', x')$ in the frame $\mathcal{S}'$ moving with the light clock
at velocity $v$ in the $+x$-direction. By this logic,

$$
L = x',\qquad L' = x-vt.
$$
So, using the equation for length contraction,

$$
x' = \gamma(x-vt).
$$
The inverse transformation arises from letting $\mathcal{S}'$ be the stationary
frame, causing frame $\mathcal{S}$ to travel at speed $v$ in the $-x$-direction.

$$
L' = x' + vt', \qquad L = x,
$$
resulting in

$$
x = \gamma(x' + vt').
$$
Note the symmetry here: swapping primes with unprimed coordinates picks up a
minus sign for the velocity, as it should. Length contraction and time dilation
occur regardless of what direction an object is traveling, so there should be
no preference in the coordinate transformation for one direction versus
another. Putting these transformations together, we have

$$
\boxed{
   \begin{array}{cl}
   \hspace{1pt}\\[-4pt]
   ({\rm i}) & x' = \gamma(x-vt) \\[12pt]
   ({\rm ii}) & y' = y \\[12pt]
   ({\rm iii}) & z' = z \\[12pt]
   ({\rm iv}) & t' = \gamma\left(t-\dfrac{vx}{c^2}\right). \\[-4pt]
   \hspace{1pt}
   \end{array}
}
$$ (eq:lorentz-transformations)
These are the **Lorentz transformations** of special relativity. Note that,
when $v \ll c$, $\gamma\to 1$ and these reduce to the Galilean relationship
(Eq. [](eq:galilean-transformations)). Also, dimensions perpendicular to the
direction of motion do not get contracted.

### Implications of Lorentz Transformations

#### Relativity of Simultaneity
   Consider two events that are simultaneous in the lab frame $\mathcal{S}$ but
   take place at two different $x$ coordinates. By the transformation equation
   for time, each event will have different $t'$ coordinates. Thus, in frame
   $\mathcal{S}'$, those events will not be simultaneous. The conclusion is
   that *simultaneous events in one frame will not be simultaneous in another*.

#### Einstein Velocity Addition
An object moving in frame $\mathcal{S}$ at velocity

$$
u = \frac{dx}{dt}
$$
has a velocity in frame $\mathcal{S}'$ of

$$
u' = \frac{dx'}{dt'} = \frac{\gamma(dx - vdt)}{\gamma(dt - vdx/c^2)}
   = \frac{u - v}{1-uv/c^2}.
$$ (eq:einstein-vel)
This is the **Einstein velocity addition rule**. Note that if $u = c$,

$$
u' = \frac{c - v}{1-cv/c^2} = c \left(\frac{1 - v/c}{1 - v/c}\right) = c,
$$
preserving the invariance of the speed of light. When $u \ll c$ and $v \ll c$,
we recover the relative velocity of Galilean relativity (Eq.
[](eq:rel-vel-gal)).