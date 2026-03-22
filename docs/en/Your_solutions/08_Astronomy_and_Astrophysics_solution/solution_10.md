# Task 10 – Measuring the Height of the Atmosphere

## Problem Statement

A medieval observer measures the time between sunset and the first appearance of faint stars as

$$
t = 40 \text{ min}
$$

Assume:

$$
R_E = 6370 \text{ km}
$$

The Earth rotates

$$
360^\circ
$$

in

$$
24 \text{ h}
$$

and the atmosphere is modeled by

$$
\cos \phi = \frac{R_E}{R_E + h}
$$

Determine:

1. the solar depression angle $\phi$,
2. the atmospheric height $h$.

## Theory

The Earth rotates uniformly, so the Sun's apparent angular motion is

$$
15^\circ \text{ per hour}
$$

or

$$
1^\circ \text{ per 4 min}
$$

Thus the measured delay time directly gives the solar depression angle.

Once $\phi$ is known, the geometric atmosphere model gives

$$
R_E + h = \frac{R_E}{\cos \phi}
$$

so

$$
h = R_E \left( \frac{1}{\cos \phi} - 1 \right)
$$

## Step-by-Step Solution

### 1. Solar depression angle

The Earth rotates

$$
15^\circ
$$

per hour.

In

$$
40 \text{ min} = \frac{2}{3} \text{ h}
$$

the angular change is

$$
\phi = 15^\circ \cdot \frac{2}{3} = 10^\circ
$$

### 2. Atmospheric height

Use

$$
h = R_E \left( \frac{1}{\cos \phi} - 1 \right)
$$

Substitute

$$
R_E = 6370 \text{ km}
$$

and

$$
\phi = 10^\circ
$$

Then

$$
h = 6370 \left( \frac{1}{\cos 10^\circ} - 1 \right)
$$

Using

$$
\cos 10^\circ \approx 0.98481
$$

gives

$$
h \approx 98.3 \text{ km}
$$

## Final Result

The solar depression angle is

$$
\phi = 10^\circ
$$

The atmospheric height in this simple model is

$$
h \approx 98.3 \text{ km}
$$

## Interpretation

This result is an idealized geometric estimate. Real atmospheric visibility depends on scattering, extinction, refraction, and observer conditions, so the true visible atmosphere is not a sharp boundary. Still, the estimate is of the correct order of magnitude.