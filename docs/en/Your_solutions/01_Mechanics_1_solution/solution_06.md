# Task 06 – Variable Velocity

## Problem Statement

The velocity of an object is

$$
v(t) = t^2 + 2t - 5
$$

The object was at position

$$
x = 4
$$

when

$$
t = 0
$$

Determine the position and acceleration at time

$$
t = 3
$$

## Theory

Velocity is the derivative of position:

$$
v(t) = \frac{dx}{dt}
$$

Therefore, position is found by integrating velocity. Acceleration is the derivative of velocity:

$$
a(t) = \frac{dv}{dt}
$$

## Step-by-Step Solution

### 1. Position function

Start from

$$
\frac{dx}{dt} = t^2 + 2t - 5
$$

Integrate:

$$
x(t) = \int (t^2 + 2t - 5) \, dt
$$

$$
x(t) = \frac{t^3}{3} + t^2 - 5t + C
$$

Use the initial condition

$$
x(0) = 4
$$

This gives

$$
4 = C
$$

Hence,

$$
x(t) = \frac{t^3}{3} + t^2 - 5t + 4
$$

Evaluate at $t = 3$:

$$
x(3) = \frac{27}{3} + 9 - 15 + 4
$$

$$
x(3) = 9 + 9 - 15 + 4 = 7
$$

### 2. Acceleration

Differentiate the velocity:

$$
a(t) = \frac{d}{dt}(t^2 + 2t - 5)
$$

$$
a(t) = 2t + 2
$$

Evaluate at $t = 3$:

$$
a(3) = 2 \cdot 3 + 2 = 8
$$

## Final Result

The position function is

$$
x(t) = \frac{t^3}{3} + t^2 - 5t + 4
$$

At time $t = 3$,

$$
x(3) = 7
$$

and

$$
a(3) = 8
$$

## Interpretation

The velocity is not constant, so the position is a cubic function of time and the acceleration is linear in time. At $t=3$, the object is at position $x=7$ and its acceleration is positive, which means the velocity is increasing at that moment.