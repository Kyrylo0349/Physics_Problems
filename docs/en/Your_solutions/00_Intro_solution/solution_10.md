# Task 10 – Infinite Series and Final Position of an Ant

## Problem Statement

An ant starts at the origin and moves according to the pattern:

- $1$ meter east,
- $\frac{1}{2}$ meter north,
- $\frac{1}{3}$ meter west,
- $\frac{1}{4}$ meter south,
- $\frac{1}{5}$ meter east,

and so on indefinitely.

Determine the final position of the ant.

## Theory

The motion can be separated into horizontal and vertical components.

- Odd-numbered steps contribute to the horizontal position.
- Even-numbered steps contribute to the vertical position.
- The directions alternate, producing alternating infinite series.

Two standard series are useful:

$$
1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots = \frac{\pi}{4}
$$

and

$$
1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots = \ln 2
$$

## Step-by-Step Solution

### 1. Horizontal displacement

The horizontal motion is

$$
1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \cdots
$$

This is the Gregory-Leibniz series for

$$
\frac{\pi}{4}
$$

Therefore, the final horizontal coordinate is

$$
x = \frac{\pi}{4}
$$

### 2. Vertical displacement

The vertical motion is

$$
\frac{1}{2} - \frac{1}{4} + \frac{1}{6} - \frac{1}{8} + \cdots
$$

Factor out $\frac{1}{2}$:

$$
\frac{1}{2} - \frac{1}{4} + \frac{1}{6} - \frac{1}{8} + \cdots
=
\frac{1}{2}
\left(
1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots
\right)
$$

The series in parentheses is the alternating harmonic series:

$$
1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots = \ln 2
$$

Hence,

$$
y = \frac{1}{2} \ln 2
$$

### 3. Final position

Combining the horizontal and vertical coordinates gives

$$
\left( \frac{\pi}{4}, \frac{1}{2}\ln 2 \right)
$$

Numerically,

$$
\frac{\pi}{4} \approx 0.785
$$

and

$$
\frac{1}{2}\ln 2 \approx 0.347
$$

So the final position is approximately

$$
(0.785,\; 0.347)
$$

## Final Result

The ant approaches the final position

$$
\left( \frac{\pi}{4}, \frac{1}{2}\ln 2 \right)
$$

## Interpretation

Although the ant keeps moving forever, the step lengths decrease, and the total displacement converges to a finite point. This is a standard example of how an infinite process can produce a finite result when the corresponding series converges.