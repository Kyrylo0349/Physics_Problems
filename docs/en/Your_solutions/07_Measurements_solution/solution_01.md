# Task 01 – Propagation of Error I

## Problem Statement

The radius of a sphere is measured as

$$
r = (6.20 \pm 0.05)\text{ cm}
$$

Calculate the volume of the sphere and its uncertainty.

## Theory

The volume of a sphere is

$$
V = \frac{4}{3}\pi r^3
$$

For a quantity of the form

$$
V \propto r^3
$$

the relative uncertainty is approximately

$$
\frac{\Delta V}{V} \approx 3 \frac{\Delta r}{r}
$$

## Step-by-Step Solution

First calculate the volume:

$$
V = \frac{4}{3}\pi (6.20)^3
$$

$$
V \approx 998.63 \text{ cm}^3
$$

Now calculate the relative uncertainty:

$$
\frac{\Delta V}{V} \approx 3 \frac{0.05}{6.20}
$$

$$
\frac{\Delta V}{V} \approx 0.02419
$$

So the absolute uncertainty is

$$
\Delta V \approx 998.63 \cdot 0.02419 \approx 24.16 \text{ cm}^3
$$

Rounded appropriately,

$$
\Delta V \approx 24 \text{ cm}^3
$$

## Final Result

$$
V = (999 \pm 24)\text{ cm}^3
$$

## Interpretation

Because the volume depends on the cube of the radius, even a small uncertainty in the radius produces a noticeably larger uncertainty in the volume.