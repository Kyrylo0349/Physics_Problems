# Task 07 – Elimination of Time and Interpretation of Acceleration

## Problem Statement

The path is given in parametric form by

$$
x(t) = 2t^2
$$

and

$$
y(t) = 3t^3
$$

Required:

- eliminate the parameter $t$,
- describe the trajectory,
- calculate $\vec{v}(t)$, $|\vec{v}(t)|$, $\vec{a}(t)$, and $|\vec{a}(t)|$,
- determine whether the acceleration is constant.

## Theory

A parametric curve describes position through a parameter, usually time. Eliminating the parameter produces a direct relation between $x$ and $y$.

Velocity and acceleration are found by differentiating the position vector:

$$
\vec{r}(t) = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix}
$$

$$
\vec{v}(t) = \frac{d\vec{r}}{dt}
$$

$$
\vec{a}(t) = \frac{d\vec{v}}{dt}
$$

The magnitudes are

$$
|\vec{v}(t)| = \sqrt{v_x^2 + v_y^2}
$$

and

$$
|\vec{a}(t)| = \sqrt{a_x^2 + a_y^2}
$$

## Step-by-Step Solution

### 1. Eliminate the parameter

From

$$
x = 2t^2
$$

one gets

$$
t^2 = \frac{x}{2}
$$

Now square the equation for $y$:

$$
y = 3t^3
$$

$$
y^2 = 9t^6
$$

Since

$$
t^6 = (t^2)^3 = \left( \frac{x}{2} \right)^3
$$

it follows that

$$
y^2 = 9 \left( \frac{x}{2} \right)^3 = \frac{9}{8} x^3
$$

Thus the Cartesian equation is

$$
y^2 = \frac{9}{8} x^3
$$

### 2. Trajectory

Because

$$
x = 2t^2 \geq 0
$$

the curve lies in the right half-plane. For positive $t$, one has positive $y$; for negative $t$, one has negative $y$. The trajectory is a semicubical parabola with a cusp at the origin.

### 3. Velocity vector and speed

The position vector is

$$
\vec{r}(t) = \begin{pmatrix} 2t^2 \\ 3t^3 \end{pmatrix}
$$

Differentiate:

$$
\vec{v}(t) = \begin{pmatrix} 4t \\ 9t^2 \end{pmatrix}
$$

Its magnitude is

$$
|\vec{v}(t)| = \sqrt{(4t)^2 + (9t^2)^2}
$$

$$
|\vec{v}(t)| = \sqrt{16t^2 + 81t^4}
$$

A convenient factorized form is

$$
|\vec{v}(t)| = |t| \sqrt{16 + 81t^2}
$$

### 4. Acceleration vector and magnitude

Differentiate again:

$$
\vec{a}(t) = \begin{pmatrix} 4 \\ 18t \end{pmatrix}
$$

Its magnitude is

$$
|\vec{a}(t)| = \sqrt{4^2 + (18t)^2}
$$

$$
|\vec{a}(t)| = \sqrt{16 + 324t^2}
$$

## Final Result

The trajectory equation is

$$
y^2 = \frac{9}{8} x^3
$$

The velocity vector is

$$
\vec{v}(t) = \begin{pmatrix} 4t \\ 9t^2 \end{pmatrix}
$$

The speed is

$$
|\vec{v}(t)| = \sqrt{16t^2 + 81t^4} = |t| \sqrt{16 + 81t^2}
$$

The acceleration vector is

$$
\vec{a}(t) = \begin{pmatrix} 4 \\ 18t \end{pmatrix}
$$

The acceleration magnitude is

$$
|\vec{a}(t)| = \sqrt{16 + 324t^2}
$$

The acceleration is not constant.

## Interpretation

The motion follows a curved path whose shape is not a parabola but a semicubical parabola. The $x$-component of acceleration is constant, while the $y$-component depends on time. Therefore the acceleration vector changes with time, and so does its magnitude.