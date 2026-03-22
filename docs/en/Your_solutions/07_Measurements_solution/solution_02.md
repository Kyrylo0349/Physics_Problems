# Task 02 – Propagation of Error II

## Problem Statement

The dimensions of a rectangular plate are measured as

$$
L = (15.3 \pm 0.1)\text{ cm}
$$

$$
W = (8.4 \pm 0.1)\text{ cm}
$$

Calculate the area and its uncertainty.

## Theory

The area is

$$
A = LW
$$

For a product, the relative uncertainty is approximated by

$$
\frac{\Delta A}{A} \approx \frac{\Delta L}{L} + \frac{\Delta W}{W}
$$

## Step-by-Step Solution

First calculate the area:

$$
A = 15.3 \cdot 8.4 = 128.52 \text{ cm}^2
$$

Now calculate the relative uncertainty:

$$
\frac{\Delta A}{A} \approx \frac{0.1}{15.3} + \frac{0.1}{8.4}
$$

$$
\frac{\Delta A}{A} \approx 0.00654 + 0.01190 = 0.01844
$$

So the absolute uncertainty is

$$
\Delta A \approx 128.52 \cdot 0.01844 \approx 2.37 \text{ cm}^2
$$

Rounded appropriately,

$$
\Delta A \approx 2.4 \text{ cm}^2
$$

## Final Result

$$
A = (128.5 \pm 2.4)\text{ cm}^2
$$

## Interpretation

The uncertainty in width contributes more strongly than the uncertainty in length because the same absolute uncertainty represents a larger relative error for the smaller measurement.