# Task 07 – Motion of a Fly Between a Bicycle and a Wall

## Problem Statement

A bicycle is $10$ meters from a wall and moves toward it at a constant speed of $1 \text{ m/s}$. A fly starts from the bicycle's front wheel and flies toward the wall at $2 \text{ m/s}$. Each time it hits the wall, it instantly turns around and flies back toward the bicycle, repeating this motion until the bicycle reaches the wall. Determine the total distance traveled by the fly before it is crushed.

## Theory

Although the fly changes direction infinitely many times, the total time of motion is finite. The simplest method is therefore:

1. determine how long the bicycle takes to reach the wall,
2. multiply that time by the fly's constant speed.

This avoids summing an infinite geometric sequence of shorter and shorter trips.

## Step-by-Step Solution

### 1. Time for the bicycle to reach the wall

The bicycle starts $10$ meters from the wall and moves at

$$
v_{\text{bike}} = 1 \text{ m/s}
$$

The travel time is

$$
t = \frac{\text{distance}}{\text{speed}}
$$

Therefore,

$$
t = \frac{10}{1}
$$

$$
t = 10 \text{ s}
$$

### 2. Distance traveled by the fly

The fly moves for the same total time,

$$
t = 10 \text{ s}
$$

at constant speed

$$
v_{\text{fly}} = 2 \text{ m/s}
$$

Hence the total distance traveled is

$$
d_{\text{fly}} = v_{\text{fly}} t
$$

$$
d_{\text{fly}} = 2 \cdot 10
$$

$$
d_{\text{fly}} = 20 \text{ m}
$$

## Final Result

$$
d_{\text{fly}} = 20 \text{ m}
$$

## Interpretation

The infinitely many turns do not imply an infinite total distance. Each leg of the fly's motion becomes shorter, and all of them occur within the finite time interval of $10$ seconds. The total distance is therefore simply the fly's speed multiplied by that total time.







# Task 07 – Mini Theory: Logic, Motion, and Infinite Processes

## What this topic is about

This type of problem combines motion with logical reasoning. Even if an object changes direction infinitely many times, the total time of motion can still be finite.

The central relation is

$$
\text{distance} = \text{speed} \times \text{time}
$$

## Key ideas

An infinite number of events does not always mean an infinite total result.

If the total time is finite, the total distance can also be finite.

Some complicated motion problems can be simplified by focusing on total time instead of each separate step.

## Why it matters in physics

Physics often requires identifying the simplest viewpoint. Instead of tracking every detail, it is often better to find a global quantity such as total time, energy, or momentum.