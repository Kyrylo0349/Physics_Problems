# Task 08 – Definite Integral of $\sin x$

## Problem Statement

Calculate the area under the curve

$$
f(x) = \sin x
$$

from

$$
x = 0
$$

to

$$
x = \pi
$$

## Theory

The area under a curve on an interval can be found using a definite integral:

$$
\text{Area} = \int_a^b f(x)\,dx
$$

For the sine function,

$$
\int \sin x \, dx = -\cos x + C
$$

On the interval

$$
[0, \pi]
$$

the function $\sin x$ is non-negative, so the definite integral is equal to the geometric area.

## Step-by-Step Solution

Set up the integral:

$$
\int_0^{\pi} \sin x \, dx
$$

Use the antiderivative of $\sin x$:

$$
\int_0^{\pi} \sin x \, dx = \left[ -\cos x \right]_0^{\pi}
$$

Evaluate at the upper and lower limits:

$$
\left[ -\cos x \right]_0^{\pi} = -\cos \pi - \left( -\cos 0 \right)
$$

Use the values

$$
\cos \pi = -1
$$

and

$$
\cos 0 = 1
$$

Then

$$
-\cos \pi - \left( -\cos 0 \right) = -(-1) - (-1)
$$

$$
= 1 + 1
$$

$$
= 2
$$

## Final Result

$$
\int_0^{\pi} \sin x \, dx = 2
$$

Therefore, the area under the curve is

$$
2
$$

square units.

## Interpretation

The graph of $\sin x$ forms one positive arch between $0$ and $\pi$. The definite integral measures the total signed area, and because the curve remains above the $x$-axis on this interval, the result is the actual geometric area.