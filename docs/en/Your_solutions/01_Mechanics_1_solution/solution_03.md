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

Determine whether their paths intersect. If yes, determine when and where they collide. If not, determine the minimum distance between them and when it occurs.

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
\begin{aligned}
\begin{pmatrix} 2 + t_A \\ 8 - 3t_A \end{pmatrix}
&=
\begin{pmatrix} 2t_B - 1 \\ 2t_B + 2 \end{pmatrix}
\end{aligned}
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

Substitute into the second equation:

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
t_B = \frac{15}{8}
$$

Then

$$
t_A = 2 \cdot \frac{15}{8} - 3 = \frac{30}{8} - \frac{24}{8} = \frac{6}{8} = \frac{3}{4}
$$

So the geometric paths do intersect.

The intersection point is

$$
A\left( \frac{3}{4} \right) = \begin{pmatrix} 2 + \frac{3}{4} \\ 8 - 3 \cdot \frac{3}{4} \end{pmatrix} = \begin{pmatrix} \frac{11}{4} \\ \frac{23}{4} \end{pmatrix}
$$

Checking with Bob:

$$
B\left( \frac{15}{8} \right) = \begin{pmatrix} 2 \cdot \frac{15}{8} - 1 \\ 2 \cdot \frac{15}{8} + 2 \end{pmatrix} = \begin{pmatrix} \frac{11}{4} \\ \frac{23}{4} \end{pmatrix}
$$

Therefore, the paths intersect at

$$
\begin{pmatrix} \frac{11}{4} \\ \frac{23}{4} \end{pmatrix}
$$

### 2. Check whether they collide

A collision requires

$$
A(t) = B(t)
$$

for the same time $t$.

Equating the coordinates with one common parameter gives

$$
2 + t = 2t - 1
$$

Hence,

$$
t = 3
$$

From the second coordinate,

$$
8 - 3t = 2t + 2
$$

$$
6 = 5t
$$

$$
t = \frac{6}{5}
$$

The times are different, so Alice and Bob do not collide.

### 3. Minimum distance during simultaneous motion

The relative position vector is

$$
A(t) - B(t) = \begin{pmatrix} 2 + t - (2t - 1) \\ 8 - 3t - (2t + 2) \end{pmatrix} = \begin{pmatrix} 3 - t \\ 6 - 5t \end{pmatrix}
$$

Therefore,

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

Set the derivative equal to zero:

$$
52t - 66 = 0
$$

$$
t = \frac{33}{26}
$$

Now evaluate the minimum value:

$$
d_{\min}^2 = 26 \left( \frac{33}{26} \right)^2 - 66 \left( \frac{33}{26} \right) + 45
$$

$$
d_{\min}^2 = \frac{81}{26}
$$

Hence,

$$
d_{\min} = \sqrt{\frac{81}{26}} = \frac{9}{\sqrt{26}} \approx 1.77
$$

## Final Result

The geometric paths intersect at

$$
\begin{pmatrix} \frac{11}{4} \\ \frac{23}{4} \end{pmatrix}
$$

Alice reaches this point at

$$
t_A = \frac{3}{4}
$$

Bob reaches it at

$$
t_B = \frac{15}{8}
$$

Therefore, they do not collide.

The minimum distance during simultaneous motion occurs at

$$
t = \frac{33}{26}
$$

and equals

$$
d_{\min} = \frac{9}{\sqrt{26}} \approx 1.77
$$

## Interpretation

The two trajectories cross as geometric curves, but the moving points do not arrive at the intersection point at the same time. Therefore, there is no collision. The closest approach occurs later, at a time obtained by minimizing the squared distance between the positions.