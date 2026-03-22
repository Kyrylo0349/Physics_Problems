# Task 04 – Geostationary Orbit

## Problem Statement

A geostationary satellite remains above the same point on Earth.

Determine:

- its orbital period,
- its altitude above the Earth's surface.

## Theory

A geostationary satellite must rotate with the same angular speed as the Earth. Therefore its orbital period must equal the Earth's rotation period.

For a circular orbit,

$$
T = 2\pi \sqrt{\frac{r^3}{GM_E}}
$$

Solving for $r$ gives

$$
r = \left( \frac{GM_E T^2}{4\pi^2} \right)^{1/3}
$$

The altitude is then

$$
h = r - R_E
$$

## Step-by-Step Solution

### 1. Orbital period

For a truly geostationary orbit, the period is one sidereal day, approximately

$$
T \approx 23 \text{ h } 56 \text{ min} \approx 86164 \text{ s}
$$

### 2. Orbital radius

Use

$$
r = \left( \frac{GM_E T^2}{4\pi^2} \right)^{1/3}
$$

with

$$
G = 6.67 \times 10^{-11}
$$

$$
M_E = 5.97 \times 10^{24} \text{ kg}
$$

Substituting gives

$$
r \approx 4.216 \times 10^7 \text{ m}
$$

$$
r \approx 42159 \text{ km}
$$

### 3. Altitude above the Earth's surface

Take

$$
R_E = 6378 \text{ km}
$$

Then

$$
h = 42159 - 6378
$$

$$
h \approx 35781 \text{ km}
$$

## Final Result

The required orbital period is approximately

$$
T \approx 23 \text{ h } 56 \text{ min}
$$

The altitude of a geostationary orbit is approximately

$$
h \approx 3.58 \times 10^4 \text{ km}
$$

## Interpretation

A geostationary satellite must orbit very far from the Earth so that its orbital period matches the Earth's rotation period.