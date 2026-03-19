# Task 01 – Projectile Motion

## Problem Statement

A projectile is launched from the ground with initial speed

$$
v_0 = 100 \text{ m/s}
$$

at angle

$$
\theta = 37^\circ
$$

above the horizontal. Air resistance is neglected.

Required:

- derive the differential equations of motion in the horizontal and vertical directions,
- determine the time of flight,
- determine the maximum height,
- determine the range.

## Theory

Projectile motion is the motion of a body under the action of gravity alone. In the absence of air resistance, the horizontal and vertical motions are independent.

The acceleration vector is

$$
\vec{a} = \begin{pmatrix} 0 \\ -g \end{pmatrix}
$$

where

$$
g \approx 9.81 \text{ m/s}^2
$$

The initial velocity is decomposed into components:

$$
v_{0x} = v_0 \cos \theta
$$

$$
v_{0y} = v_0 \sin \theta
$$

## Step-by-Step Solution

### 1. Differential equations of motion

Let the projectile position be

$$
\vec{r}(t) = \begin{pmatrix} x(t) \\ y(t) \end{pmatrix}
$$

Since the only force is gravity,

$$
m \ddot{x}(t) = 0
$$

and

$$
m \ddot{y}(t) = -mg
$$

Therefore, the differential equations are

$$
\ddot{x}(t) = 0
$$

and

$$
\ddot{y}(t) = -g
$$

with initial conditions

$$
x(0) = 0, \qquad y(0) = 0
$$

$$
\dot{x}(0) = v_0 \cos \theta, \qquad \dot{y}(0) = v_0 \sin \theta
$$

Integrating gives

$$
x(t) = v_0 \cos \theta \, t
$$

and

$$
y(t) = v_0 \sin \theta \, t - \frac{1}{2} g t^2
$$

### 2. Time of flight

The projectile returns to the ground when

$$
y(t) = 0
$$

Thus,

$$
v_0 \sin \theta \, t - \frac{1}{2} g t^2 = 0
$$

Factor out $t$:

$$
t \left( v_0 \sin \theta - \frac{1}{2} g t \right) = 0
$$

The nonzero solution is

$$
T = \frac{2 v_0 \sin \theta}{g}
$$

Substitute the data:

$$
T = \frac{2 \cdot 100 \cdot \sin 37^\circ}{9.81}
$$

Using

$$
\sin 37^\circ \approx 0.6018
$$

gives

$$
T \approx 12.27 \text{ s}
$$

### 3. Maximum height

At the highest point, the vertical velocity is zero:

$$
v_y(t) = v_0 \sin \theta - gt
$$

Set

$$
v_y(t_H) = 0
$$

Then

$$
t_H = \frac{v_0 \sin \theta}{g}
$$

The maximum height is

$$
H = y(t_H)
$$

A standard equivalent formula is

$$
H = \frac{(v_0 \sin \theta)^2}{2g}
$$

Substitute the values:

$$
H = \frac{(100 \sin 37^\circ)^2}{2 \cdot 9.81}
$$

$$
H \approx 184.60 \text{ m}
$$

### 4. Range

The horizontal range is

$$
R = x(T)
$$

Hence,

$$
R = v_0 \cos \theta \cdot T
$$

Substitute the expression for $T$:

$$
R = v_0 \cos \theta \cdot \frac{2 v_0 \sin \theta}{g}
$$

Using

$$
2 \sin \theta \cos \theta = \sin 2\theta
$$

gives

$$
R = \frac{v_0^2 \sin 2\theta}{g}
$$

Now substitute the data:

$$
R = \frac{100^2 \sin 74^\circ}{9.81}
$$

Using

$$
\sin 74^\circ \approx 0.9613
$$

gives

$$
R \approx 979.88 \text{ m}
$$

## Final Result

The equations of motion are

$$
\ddot{x}(t) = 0, \qquad \ddot{y}(t) = -g
$$

with solutions

$$
x(t) = v_0 \cos \theta \, t
$$

and

$$
y(t) = v_0 \sin \theta \, t - \frac{1}{2} g t^2
$$

The time of flight is

$$
T \approx 12.27 \text{ s}
$$

The maximum height is

$$
H \approx 184.60 \text{ m}
$$

The range is

$$
R \approx 979.88 \text{ m}
$$

## Interpretation

Projectile motion separates naturally into uniform horizontal motion and uniformly accelerated vertical motion. The horizontal acceleration is zero, while the vertical acceleration is constant and directed downward. The trajectory is a parabola, and the key quantities of motion follow directly from the component form of the initial velocity.