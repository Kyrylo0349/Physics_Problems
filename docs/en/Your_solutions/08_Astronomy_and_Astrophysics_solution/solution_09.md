# Task 09 – Size and Distance of the Sun from Aristarchus' Method

## Problem Statement

At exact half-Moon phase, the Earth–Moon–Sun system forms a right triangle with the right angle at the Moon.

Given:

$$
\theta = 89.85^\circ
$$

$$
\alpha = 0.53^\circ
$$

$$
d_{EM} = 3.84 \times 10^5 \text{ km}
$$

Calculate:

1. the Earth–Sun distance $d_{ES}$,
2. the Sun's true diameter $D_S$ using the small-angle approximation,
3. the ratio $\frac{D_M}{D_S}$,
4. how $d_{ES}$ changes if

$$
\theta = 89.75^\circ
$$

is used instead.

## Theory

At dichotomy, the right triangle has:

- Earth–Moon distance as one leg,
- Earth–Sun distance as the hypotenuse,
- angle at Earth equal to $\theta$.

Therefore,

$$
\cos \theta = \frac{d_{EM}}{d_{ES}}
$$

so

$$
d_{ES} = \frac{d_{EM}}{\cos \theta}
$$

For a small angular diameter $\alpha$ in radians,

$$
\alpha \approx \frac{D}{d}
$$

so

$$
D \approx \alpha d
$$

## Step-by-Step Solution

### 1. Earth–Sun distance for $\theta = 89.85^\circ$

Use

$$
d_{ES} = \frac{d_{EM}}{\cos \theta}
$$

Substitute:

$$
d_{ES} = \frac{3.84 \times 10^5}{\cos 89.85^\circ} \text{ km}
$$

This gives

$$
d_{ES} \approx 1.4668 \times 10^8 \text{ km}
$$

### 2. True diameter of the Sun

Convert the angular diameter to radians:

$$
\alpha = 0.53^\circ \cdot \frac{\pi}{180} \approx 0.00925 \text{ rad}
$$

Now apply

$$
D_S \approx \alpha d_{ES}
$$

$$
D_S \approx 0.00925 \cdot 1.4668 \times 10^8
$$

$$
D_S \approx 1.36 \times 10^6 \text{ km}
$$

### 3. Ratio of true diameters

Since the Sun and Moon have the same apparent angular diameter,

$$
\frac{D_M}{D_S} = \frac{d_{EM}}{d_{ES}}
$$

Thus,

$$
\frac{D_M}{D_S} \approx \frac{3.84 \times 10^5}{1.4668 \times 10^8}
$$

$$
\frac{D_M}{D_S} \approx 0.00262
$$

Equivalently,

$$
\frac{D_S}{D_M} \approx 382
$$

### 4. Repeat for $\theta = 89.75^\circ$

Now compute

$$
d_{ES}' = \frac{3.84 \times 10^5}{\cos 89.75^\circ}
$$

This gives

$$
d_{ES}' \approx 8.8007 \times 10^7 \text{ km}
$$

The change is

$$
\Delta d = d_{ES}' - d_{ES}
$$

$$
\Delta d \approx -5.87 \times 10^7 \text{ km}
$$

So the estimated Earth–Sun distance becomes much smaller.

## Final Result

For

$$
\theta = 89.85^\circ
$$

the Earth–Sun distance is

$$
d_{ES} \approx 1.47 \times 10^8 \text{ km}
$$

The Sun's true diameter is

$$
D_S \approx 1.36 \times 10^6 \text{ km}
$$

The diameter ratio is

$$
\frac{D_M}{D_S} \approx 0.00262
$$

If

$$
\theta = 89.75^\circ
$$

is used instead, the Earth–Sun distance becomes

$$
d_{ES}' \approx 8.80 \times 10^7 \text{ km}
$$

which is smaller by about

$$
5.87 \times 10^7 \text{ km}
$$

## Interpretation

This method is extremely sensitive because $\cos \theta$ changes very rapidly when $\theta$ is close to

$$
90^\circ
$$

A very small angular measurement error produces a very large change in the estimated Earth–Sun distance. This shows both the brilliance and the practical difficulty of Aristarchus' method.