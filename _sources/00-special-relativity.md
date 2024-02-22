# Special Relativity
Einstein's Special Theory of Relativity follows from two postulates:
1. The laws of physics are the same in all inertial (non-accelerating)
   reference frames.
2. The speed of light in vacuum

   $$
   c = 299\ 792\ 458~{\rm m/s} \approx 3.00 \times 10^8~{\rm m/s}
   $$
   is the same in all inertial reference frames.
<!-- Insert light clock argument! -->
$$
r'^\mu = {\Lambda^\mu}_\nu r^\nu
$$ (eq:4-vec-transform)
where ${\Lambda^\mu}_\nu$ is the standard Lorentz transformation matrix. For
boosts in the $r^1 = x$ direction, $\Lambda$ takes the form

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