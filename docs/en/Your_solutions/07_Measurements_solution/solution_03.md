# Task 03 – Propagation of Error III

## Problem Statement

Resistance is calculated from Ohm's law:

$$
R = \frac{V}{I}
$$

with measured values

$$
V = (10.0 \pm 0.2)\text{ V}
$$

$$
I = (2.00 \pm 0.05)\text{ A}
$$

Find the resistance and its uncertainty.

## Theory

For a quotient,

$$
\frac{\Delta R}{R} \approx \frac{\Delta V}{V} + \frac{\Delta I}{I}
$$

## Step-by-Step Solution

First calculate the resistance:

$$
R = \frac{10.0}{2.00} = 5.00\,\Omega
$$

Now calculate the relative uncertainty:

$$
\frac{\Delta R}{R} \approx \frac{0.2}{10.0} + \frac{0.05}{2.00}
$$

$$
\frac{\Delta R}{R} \approx 0.020 + 0.025 = 0.045
$$

So the absolute uncertainty is

$$
\Delta R \approx 5.00 \cdot 0.045 = 0.225\,\Omega
$$

Rounded appropriately,

$$
\Delta R \approx 0.23\,\Omega
$$

## Final Result

$$
R = (5.00 \pm 0.23)\,\Omega
$$

## Interpretation

Because resistance depends on a division, the relative uncertainties of voltage and current add. Here the current measurement contributes slightly more to the final uncertainty.