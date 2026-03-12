# Task 01 – Vector Algebra

## Problem Statement

Given two vectors in three-dimensional space,

$$
\vec{a} = [2, 1, -3]
$$

and

$$
\vec{b} = [4, -2, 1]
$$

determine:

1. the magnitude of each vector,
2. the dot product $\vec{a} \cdot \vec{b}$,
3. the cross product $\vec{a} \times \vec{b}$,
4. the angle between $\vec{a}$ and $\vec{b}$.

## Theory

For a vector

$$
\vec{v} = [v_x, v_y, v_z]
$$

its magnitude is

$$
|\vec{v}| = \sqrt{v_x^2 + v_y^2 + v_z^2}
$$

The dot product of two vectors is

$$
\vec{a} \cdot \vec{b} = a_x b_x + a_y b_y + a_z b_z
$$

The cross product in component form is

$$
\vec{a} \times \vec{b} = \begin{pmatrix}
a_y b_z - a_z b_y \\
a_z b_x - a_x b_z \\
a_x b_y - a_y b_x
\end{pmatrix}
$$

The angle $\theta$ between two vectors is

$$
\cos \theta = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}| |\vec{b}|}
$$

## Step-by-Step Solution

### 1. Magnitude of $\vec{a}$

For

$$
\vec{a} = [2, 1, -3]
$$

the magnitude is

$$
|\vec{a}| = \sqrt{2^2 + 1^2 + (-3)^2}
$$

$$
|\vec{a}| = \sqrt{4 + 1 + 9}
$$

$$
|\vec{a}| = \sqrt{14}
$$

### 2. Magnitude of $\vec{b}$

For

$$
\vec{b} = [4, -2, 1]
$$

the magnitude is

$$
|\vec{b}| = \sqrt{4^2 + (-2)^2 + 1^2}
$$

$$
|\vec{b}| = \sqrt{16 + 4 + 1}
$$

$$
|\vec{b}| = \sqrt{21}
$$

### 3. Dot product $\vec{a} \cdot \vec{b}$

Using the component formula,

$$
\vec{a} \cdot \vec{b} = (2)(4) + (1)(-2) + (-3)(1)
$$

$$
\vec{a} \cdot \vec{b} = 8 - 2 - 3
$$

$$
\vec{a} \cdot \vec{b} = 3
$$

### 4. Cross product $\vec{a} \times \vec{b}$

Using the component formula,

$$
\vec{a} \times \vec{b} = \begin{pmatrix}
(1)(1) - (-3)(-2) \\
(-3)(4) - (2)(1) \\
(2)(-2) - (1)(4)
\end{pmatrix}
$$

Evaluate each component separately:

$$
(1)(1) - (-3)(-2) = 1 - 6 = -5
$$

$$
(-3)(4) - (2)(1) = -12 - 2 = -14
$$

$$
(2)(-2) - (1)(4) = -4 - 4 = -8
$$

Therefore,

$$
\vec{a} \times \vec{b} = [-5, -14, -8]
$$

### 5. Angle between the vectors

From the dot product formula,

$$
\cos \theta = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}| |\vec{b}|}
$$

Substitute the known values:

$$
\cos \theta = \frac{3}{\sqrt{14}\sqrt{21}}
$$

Combine the radicals:

$$
\cos \theta = \frac{3}{\sqrt{294}}
$$

Hence,

$$
\theta = \arccos \left( \frac{3}{\sqrt{294}} \right)
$$

Numerically,

$$
\theta \approx 79.9^\circ
$$

## Final Result

$$
|\vec{a}| = \sqrt{14}
$$

$$
|\vec{b}| = \sqrt{21}
$$

$$
\vec{a} \cdot \vec{b} = 3
$$

$$
\vec{a} \times \vec{b} = [-5, -14, -8]
$$

$$
\theta = \arccos \left( \frac{3}{\sqrt{294}} \right) \approx 79.9^\circ
$$

## Interpretation

The positive dot product shows that the angle between the vectors is acute in the cosine sense, but only slightly so, because the value is small compared with the product of the magnitudes. This is consistent with the angle being close to $90^\circ$. The cross product produces a vector perpendicular to both $\vec{a}$ and $\vec{b}$, with direction determined by the right-hand rule.





# Task 01 – Mini Theory: Vector Algebra

## What this topic is about

Vector algebra studies quantities that have both magnitude and direction. In physics, vectors are used for displacement, velocity, force, acceleration, and many other directional quantities.

In three dimensions, a vector is written as

$$
\vec{v} = \begin{pmatrix} v_x \\ v_y \\ v_z \end{pmatrix}
$$

## Key ideas

The magnitude of a vector tells how long it is.

The dot product measures how much two vectors point in the same direction.

The cross product produces a new vector perpendicular to both original vectors.

The angle between two vectors shows their directional relationship.

## Why it matters in physics

Many physical problems require splitting vectors into components, combining them, or comparing their directions. Vector algebra is one of the basic tools of mechanics and electromagnetism.