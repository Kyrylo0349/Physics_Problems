# Task 09 – Optimization of a Rectangle Under a Curve

## Problem Statement

A rectangle lies under the curve

$$
y = 3 - x^2
$$

in the first quadrant. Determine the dimensions of the rectangle with maximum area.

## Theory

For a rectangle under a curve in the first quadrant, the standard interpretation is:

- one corner is at the origin,
- the opposite corner lies on the curve,
- the sides of the rectangle are parallel to the coordinate axes.

If the upper-right corner is

$$
(x, y)
$$

and it lies on the curve

$$
y = 3 - x^2
$$

then the area of the rectangle is

$$
A(x) = x y = x(3 - x^2)
$$

The maximum area is found by differentiating $A(x)$ and locating its critical points.

## Step-by-Step Solution

### 1. Express the area as a function of $x$

Since the rectangle is under the curve,

$$
y = 3 - x^2
$$

Therefore,

$$
A(x) = x(3 - x^2)
$$

Expand if needed:

$$
A(x) = 3x - x^3
$$

The first-quadrant condition requires

$$
x \geq 0
$$

and

$$
y \geq 0
$$

which implies

$$
3 - x^2 \geq 0
$$

Hence,

$$
0 \leq x \leq \sqrt{3}
$$

### 2. Differentiate the area function

Differentiate with respect to $x$:

$$
A'(x) = \frac{d}{dx}(3x - x^3)
$$

$$
A'(x) = 3 - 3x^2
$$

### 3. Find critical points

Set the derivative equal to zero:

$$
3 - 3x^2 = 0
$$

Divide by $3$:

$$
1 - x^2 = 0
$$

$$
x^2 = 1
$$

Since $x$ must be non-negative in the first quadrant,

$$
x = 1
$$

### 4. Determine the corresponding height

Substitute $x = 1$ into the curve:

$$
y = 3 - (1)^2
$$

$$
y = 3 - 1
$$

$$
y = 2
$$

### 5. Verify that this gives a maximum

Differentiate again:

$$
A''(x) = -6x
$$

At

$$
x = 1
$$

one has

$$
A''(1) = -6 < 0
$$

so the area is maximal there.

## Final Result

The rectangle with maximum area has dimensions

$$
\text{width} = 1
$$

and

$$
\text{height} = 2
$$

Its maximum area is

$$
A_{\max} = 1 \cdot 2 = 2
$$

## Interpretation

As the rectangle becomes wider, its height decreases because the top-right corner must remain on the parabola. The optimal rectangle is reached when the balance between width and height produces the largest possible product.