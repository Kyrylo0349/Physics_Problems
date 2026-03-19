# Task 04 – Vector Calculus

## Problem Statement

The position of an object is

$$
\vec{r}(t) = (3t^2)\hat{i} + (5t - 8t^2)\hat{j}
$$

Find the velocity and acceleration vectors as functions of time.

## Theory

Velocity is the time derivative of position:

$$
\vec{v}(t) = \frac{d\vec{r}}{dt}
$$

Acceleration is the time derivative of velocity:

$$
\vec{a}(t) = \frac{d\vec{v}}{dt} = \frac{d^2 \vec{r}}{dt^2}
$$

For a vector function, differentiation is performed component by component.

## Step-by-Step Solution

Write the position vector in component form:

$$
\vec{r}(t) = \begin{pmatrix} 3t^2 \\ 5t - 8t^2 \end{pmatrix}
$$

Differentiate each component to obtain the velocity:

$$
\vec{v}(t) = \begin{pmatrix} \frac{d}{dt}(3t^2) \\ \frac{d}{dt}(5t - 8t^2) \end{pmatrix}
= \begin{pmatrix} 6t \\ 5 - 16t \end{pmatrix}
$$

Differentiate again to obtain the acceleration:

$$
\vec{a}(t) = \begin{pmatrix} \frac{d}{dt}(6t) \\ \frac{d}{dt}(5 - 16t) \end{pmatrix}
= \begin{pmatrix} 6 \\ -16 \end{pmatrix}
$$

## Final Result

The velocity vector is

$$
\vec{v}(t) = \begin{pmatrix} 6t \\ 5 - 16t \end{pmatrix}
$$

The acceleration vector is

$$
\vec{a}(t) = \begin{pmatrix} 6 \\ -16 \end{pmatrix}
$$

## Interpretation

The velocity changes linearly with time, while the acceleration is constant. This means the motion is uniformly accelerated in the plane, but with different acceleration components in the $x$ and $y$ directions.