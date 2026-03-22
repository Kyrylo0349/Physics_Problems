# Task 13 – Wavefunction Probability in a 1D Box

## Problem Statement

For a particle in a one-dimensional box of length

$$
L
$$

the ground-state wavefunction is

$$
\Psi(x) = \sqrt{\frac{2}{L}} \sin\left(\frac{\pi x}{L}\right)
$$

Calculate the probability of finding the particle in:

- the region

$$
0 \le x \le \frac{L}{4}
$$

- the region

$$
\frac{L}{4} \le x \le \frac{L}{2}
$$

Determine which region is more likely.

## Theory

The probability density is

$$
|\Psi(x)|^2 = \frac{2}{L}\sin^2\left(\frac{\pi x}{L}\right)
$$

The probability in an interval is

$$
P = \int |\Psi(x)|^2 dx
$$

## Step-by-Step Solution

### 1. Probability in the region 0 to L/4

$$
P_1 = \int_0^{L/4} \frac{2}{L}\sin^2\left(\frac{\pi x}{L}\right) dx
$$

Using the standard integral of

$$
\sin^2
$$

gives

$$
P_1 = \frac{1}{4} - \frac{1}{2\pi}
$$

Numerically,

$$
P_1 \approx 0.25 - 0.159 = 0.091
$$

### 2. Probability in the region L/4 to L/2

$$
P_2 = \int_{L/4}^{L/2} \frac{2}{L}\sin^2\left(\frac{\pi x}{L}\right) dx
$$

This gives

$$
P_2 = \frac{1}{4} + \frac{1}{2\pi}
$$

Numerically,

$$
P_2 \approx 0.25 + 0.159 = 0.409
$$

## Final Result

The probability in the region

$$
0 \le x \le \frac{L}{4}
$$

is

$$
P_1 = \frac{1}{4} - \frac{1}{2\pi} \approx 0.091
$$

The probability in the region

$$
\frac{L}{4} \le x \le \frac{L}{2}
$$

is

$$
P_2 = \frac{1}{4} + \frac{1}{2\pi} \approx 0.409
$$

The second region is more likely to contain the particle.

## Interpretation

The ground-state wavefunction is largest near the center of the box and zero at the walls, so the particle is much more likely to be found closer to the middle than near the edge.