# The Schrödinger Equation

Nonrelativistic quantum mechanics follows from two principles:
1. Matter behaves like a wave with a wavelength given by the de Broglie
   wavelength,

   $$
   \lambda = \frac{h}{p} = \hbar k.
   $$ (eq:deBroglie-wl)
1. Energy is quantized according to the Planck relation

   $$
   E = hf = \hbar\omega.
   $$ (eq:planck-rel)
Here $\lambda$ is the wavelength, $f$ is the wave frequency, $p$ is the wave's momentum, $E$ is its energy,

$$
h = 6.626\ 070\ 15\times 10^{-34}~{\rm J\, s}
$$ (eq:planck-const)
is Planck's constant, and

$$
\hbar = \frac{h}{2\pi} = \frac{h}{\tau} \approx 1.054\ 572\times10^{-34}~{\rm J\, s}
$$
is the reduced Planck constant. If matter behaves like a wave, there must be a wave equation that it obeys. Consider a wave in one dimension. The simplest form it can have is that of a plane wave,[^plane-waves]

[^plane-waves]: If restricting ourselves to one type of wave bothers you, don't fret. As with classical waves, matter waves can be constructed by the principle of *superposition*, so that we can add together plane waves of different frequencies to create almost arbitrary wave shapes.

$$
\Psi(x, t) = Ae^{i(kx-\omega t)}.
$$ (eq:matter-plane-wave)
To get a wave equation, we want to take derivatives with respect to position and time and relate them to each other in analogy to the classical wave equation,

$$
\frac{1}{v^2} \frac{\partial^2 \Psi}{\partial t^2} =
\frac{\partial^2 \Psi}{\partial x^2},
$$ (eq:classical-wave)
where $v$ is the speed of the wave. For our matter wave, let's look at what we get when we take derivatives of $\Psi$. First, taking the time derivative, we get

$$
\frac{\partial\Psi}{\partial t} = -i\omega Ae^{i(kx-\omega t)} = \frac{\omega}{i} \Psi(x,t) = \frac{E}{i\hbar}\Psi(x, t),
$$
where I used the Planck relation to get the last expression. Taking the $x$-derivative of our matter wave and invoking the de Broglie relation gives

$$
\frac{\partial\Psi}{\partial x} = ik Ae^{i(kx-\omega t)} = ik\Psi(x, t) = \frac{ip}{\hbar}\Psi(x,t).
$$
To relate these derivatives to each other, we invoke the classical definition of the total energy,

$$
E = T + V = \frac{1}{2}mv^2 + V = \frac{p^2}{2m} + V,
$$
where $T$ is the **kinetic energy**, $V$ is the **potential energy**,  and $m$ is the mass of our object behaving like a wave (e.g. an electron). Putting this together and replacing $E$ and $p$ with their derivative counterparts, we get

$$
\boxed{
i\hbar \frac{\partial\Psi}{\partial t} = -\frac{\hbar^2}{2m} \frac{\partial^2\Psi}{\partial x^2} + V\Psi.}
$$ (eq:schrodinger-eqn)
This is the Schrödinger equation. The function that describes the matter wave, which we've called $\Psi$, is the **wave function**.

## The Wave Function
This function possesses all the information we could possibly know about the object it describes.