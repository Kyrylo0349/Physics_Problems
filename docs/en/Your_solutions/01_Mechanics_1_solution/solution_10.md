# Task 10 – Kinematics of a Space Curve

## Problem Statement

The point $M$ moves according to

$$
\vec{r}(t) = \begin{pmatrix}
a \cos(\omega t) \\
b \sin(\omega t) \\
bt
\end{pmatrix}
$$

where $a$, $b$, and $\omega$ are positive constants.

Required:

- find the equation of the trajectory,
- compute the path length from $t=0$ to $t=t_0$,
- provide a Python plot and discuss special cases.

## Theory

A space curve can be described parametrically by its coordinate functions. The geometric trajectory is found by eliminating the parameter.

The path length between $t=0$ and $t=t_0$ is

$$
s = \int_0^{t_0} |\vec{v}(t)| \, dt
$$

where

$$
\vec{v}(t) = \frac{d\vec{r}}{dt}
$$

If the speed is constant, the arc length reduces to

$$
s = |\vec{v}| t_0
$$

## Step-by-Step Solution

### 1. Equation of the trajectory

The coordinates are

$$
x(t) = a \cos(\omega t)
$$

$$
y(t) = b \sin(\omega t)
$$

$$
z(t) = bt
$$

From the first two equations,

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = \cos^2(\omega t) + \sin^2(\omega t) = 1
$$

Thus, the point moves on the elliptical cylinder

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

At the same time,

$$
z = bt
$$

so the motion rises linearly with time. Therefore, the full trajectory is an elliptical helix.

A useful $z$-dependent form is obtained from

$$
t = \frac{z}{b}
$$

which gives

$$
x = a \cos \left( \frac{\omega z}{b} \right)
$$

$$
y = b \sin \left( \frac{\omega z}{b} \right)
$$

### 2. Velocity and speed

Differentiate the position vector:

$$
\vec{v}(t) = \begin{pmatrix}
-a\omega \sin(\omega t) \\
b\omega \cos(\omega t) \\
b
\end{pmatrix}
$$

The speed is

$$
|\vec{v}(t)| = \sqrt{a^2 \omega^2 \sin^2(\omega t) + b^2 \omega^2 \cos^2(\omega t) + b^2}
$$

### 3. Path length

The arc length from $0$ to $t_0$ is

$$
s(t_0) = \int_0^{t_0} \sqrt{a^2 \omega^2 \sin^2(\omega t) + b^2 \omega^2 \cos^2(\omega t) + b^2} \, dt
$$

In general, this integral is not elementary. It is the correct exact expression for the path length.

If

$$
a = b
$$

then the speed becomes constant:

$$
|\vec{v}(t)| = \sqrt{a^2 \omega^2 + b^2}
$$

and the arc length simplifies to

$$
s(t_0) = t_0 \sqrt{a^2 \omega^2 + b^2}
$$

Since in this special case $a=b$, one may also write

$$
s(t_0) = t_0 \, a \sqrt{1 + \omega^2}
$$

## Final Result

The trajectory lies on the elliptical cylinder

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
$$

with vertical coordinate

$$
z = bt
$$

so the motion is an elliptical helix.

The velocity vector is

$$
\vec{v}(t) = \begin{pmatrix}
-a\omega \sin(\omega t) \\
b\omega \cos(\omega t) \\
b
\end{pmatrix}
$$

The path length from $0$ to $t_0$ is

$$
s(t_0) = \int_0^{t_0} \sqrt{a^2 \omega^2 \sin^2(\omega t) + b^2 \omega^2 \cos^2(\omega t) + b^2} \, dt
$$

In the special case

$$
a = b
$$

this becomes

$$
s(t_0) = t_0 \sqrt{a^2 \omega^2 + b^2}
$$

## Interpretation

The projection of the motion onto the $xy$-plane is an ellipse, while the $z$-coordinate increases linearly. This creates a rising helical path. If $a=b$, the horizontal projection becomes a circle and the motion becomes a circular helix. If the vertical rise were removed, the motion would reduce to planar elliptical motion.