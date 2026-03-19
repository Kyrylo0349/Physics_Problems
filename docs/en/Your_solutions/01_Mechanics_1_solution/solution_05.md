# Task 05 – Relative Velocity

## Problem Statement

A river flows east at speed

$$
2 \text{ m/s}
$$

A boat can travel at speed

$$
5 \text{ m/s}
$$

relative to still water. The boat wants to move directly north across the river.

Determine:

- the direction in which the boat must head,
- the time required to cross a river of width $200$ m.

## Theory

Relative velocity combines the boat velocity relative to the water with the water velocity relative to the ground:

$$
\vec{v}_{\text{boat, ground}} = \vec{v}_{\text{boat, water}} + \vec{v}_{\text{water, ground}}
$$

To move directly north, the ground velocity must have zero east-west component. Therefore, the boat must aim slightly west of north so that its westward component cancels the eastward river flow.

## Step-by-Step Solution

Choose axes:

- positive $x$ toward the east,
- positive $y$ toward the north.

The river velocity is

$$
\vec{v}_r = \begin{pmatrix} 2 \\ 0 \end{pmatrix}
$$

Let the boat head at angle $\phi$ west of north. Then its velocity relative to water is

$$
\vec{v}_{bw} = \begin{pmatrix} -5 \sin \phi \\ 5 \cos \phi \end{pmatrix}
$$

To go directly north, the total horizontal component must be zero:

$$
-5 \sin \phi + 2 = 0
$$

Hence,

$$
5 \sin \phi = 2
$$

$$
\sin \phi = \frac{2}{5}
$$

Therefore,

$$
\phi = \arcsin \left( \frac{2}{5} \right) \approx 23.58^\circ
$$

So the boat must head

$$
23.58^\circ
$$

west of north.

### Crossing time

The northward component of the ground velocity is

$$
v_{\text{north}} = 5 \cos \phi
$$

Using

$$
\sin \phi = \frac{2}{5}
$$

one gets

$$
\cos \phi = \sqrt{1 - \left( \frac{2}{5} \right)^2}
= \sqrt{\frac{21}{25}}
= \frac{\sqrt{21}}{5}
$$

Thus,

$$
v_{\text{north}} = 5 \cdot \frac{\sqrt{21}}{5} = \sqrt{21} \text{ m/s}
$$

Now use

$$
t = \frac{\text{distance}}{\text{speed}}
$$

Hence,

$$
t = \frac{200}{\sqrt{21}} \approx 43.64 \text{ s}
$$

## Final Result

The boat must head

$$
23.58^\circ
$$

west of north.

The crossing time is

$$
t \approx 43.64 \text{ s}
$$

## Interpretation

The boat cannot point directly north, because the river would carry it eastward. By aiming west of north, the boat creates a westward component that exactly cancels the river current, so the resulting motion relative to the ground is straight north.