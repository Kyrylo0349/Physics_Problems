# Task 03 – Path Intersection

## Problem Statement

Alice moves along the path

$$
A(t) = \begin{pmatrix} 2 + t \\ 8 - 3t \end{pmatrix}
$$

Bob moves along the path

$$
B(t) = \begin{pmatrix} 2t - 1 \\ 2t + 2 \end{pmatrix}
$$

Determine whether their paths intersect. If they do, determine when and where they collide. If they do not collide, determine the minimum distance between them and when it occurs.

## Theory

Two moving points collide if they occupy the same position at the same time.

Two geometric paths intersect if there exist parameters, not necessarily equal, for which the positions coincide.

For simultaneous motion, the distance between the points is

$$
d(t) = |A(t) - B(t)|
$$

The minimum distance is found by minimizing $d(t)$, or more conveniently $d^2(t)$.

## Step-by-Step Solution

### 1. Check whether the geometric paths intersect

Let Alice and Bob have parameters $t_A$ and $t_B$.

Then

$$
\begin{pmatrix} 2 + t_A \\ 8 - 3t_A \end{pmatrix}
=
\begin{pmatrix} 2t_B - 1 \\ 2t_B + 2 \end{pmatrix}
$$

This gives the system

$$
2 + t_A = 2t_B - 1
$$

$$
8 - 3t_A = 2t_B + 2
$$

From the first equation,

$$
t_A = 2t_B - 3
$$

Substitute into the second:

$$
8 - 3(2t_B - 3) = 2t_B + 2
$$

$$
8 - 6t_B + 9 = 2t_B + 2
$$

$$
17 - 6t_B = 2t_B + 2
$$

$$
15 = 8t_B
$$

$$
t_B = \frac{13}{8}
$$

Then

$$
t_A = 2 \cdot \frac{13}{8} - 3 = \frac{1}{4}
$$

So the paths do intersect geometrically. The intersection point is

$$
A\left( \frac{1}{4} \right) = \begin{pmatrix} 2 + \frac{1}{4} \\ 8 - \frac{3}{4} \end{pmatrix}
= \begin{pmatrix} \frac{9}{4} \\ \frac{29}{4} \end{pmatrix}
$$

### 2. Check whether they collide

A collision requires

$$
A(t) = B(t)
$$

for the same $t$.

Equating coordinates with a common time parameter gives

$$
2 + t = 2t - 1
$$

which implies

$$
t = 3
$$

From the $y$-coordinates,

$$
8 - 3t = 2t + 2
$$

which implies

$$
6 = 5t
$$

$$
t = \frac{6}{5}
$$

These times are different. Therefore, Alice and Bob do not collide.

### 3. Distance between them at the same time

The relative position is

$$
A(t) - B(t) = \begin{pmatrix} 2 + t - (2t - 1) \\ 8 - 3t - (2t + 2) \end{pmatrix}
= \begin{pmatrix} 3 - t \\ 6 - 5t \end{pmatrix}
$$

Hence,

$$
d^2(t) = (3 - t)^2 + (6 - 5t)^2
$$

Expand:

$$
d^2(t) = 9 - 6t + t^2 + 36 - 60t + 25t^2
$$

$$
d^2(t) = 26t^2 - 66t + 45
$$

Differentiate:

$$
\frac{d}{dt} d^2(t) = 52t - 66
$$

Set equal to zero:

$$
52t - 66 = 0
$$

$$
t = \frac{33}{26}
$$

This gives the time of minimum distance.

Now substitute into $d^2(t)$:

$$
d_{\min}^2 = 26 \left( \frac{33}{26} \right)^2 - 66 \left( \frac{33}{26} \right) + 45
$$

which simplifies to

$$
d_{\min}^2 = \frac{81}{26}
$$

Therefore,

$$
d_{\min} = \sqrt{\frac{81}{26}} = \frac{9}{\sqrt{26}} \approx 1.77
$$

## Final Result

The geometric paths intersect at

$$
\begin{pmatrix} \frac{9}{4} \\ \frac{29}{4} \end{pmatrix}
$$

Alice reaches this point at

$$
t_A = \frac{1}{4}
$$

and Bob reaches it at

$$
t_B = \frac{13}{8}
$$

Therefore, they do not collide.

The minimum distance during simultaneous motion occurs at

$$
t = \frac{33}{26}
$$

and is

$$
d_{\min} = \frac{9}{\sqrt{26}} \approx 1.77
$$

## Interpretation

The two moving points pass through the same geometric location, but at different times. Their paths intersect, yet there is no collision. The minimum-distance calculation shows the closest approach during their actual simultaneous motion.