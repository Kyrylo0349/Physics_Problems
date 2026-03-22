# Task 07 – Mean and Standard Deviation

## Problem Statement

The test scores are:

$$
88,\ 92,\ 79,\ 85,\ 95,\ 81,\ 86,\ 90,\ 83,\ 77,\ 89
$$

Calculate:

- the mean,
- the standard deviation

using

$$
\bar{x} = \frac{1}{N}\sum_{i=1}^{N} x_i
$$

and

$$
\sigma = \sqrt{\frac{1}{N-1}\sum_{i=1}^{N}(x_i-\bar{x})^2}
$$

Then remove the highest and lowest scores and recalculate the mean and standard deviation.

## Theory

The mean gives the central value of the data.

The standard deviation measures the spread of the data around the mean.

## Step-by-Step Solution

### 1. Original dataset

There are

$$
N = 11
$$

scores.

Their sum is

$$
88 + 92 + 79 + 85 + 95 + 81 + 86 + 90 + 83 + 77 + 89 = 945
$$

So the mean is

$$
\bar{x} = \frac{945}{11} \approx 85.91
$$

Using the sample standard deviation formula,

$$
\sigma \approx 5.58
$$

### 2. Remove highest and lowest scores

Remove

$$
95
$$

and

$$
77
$$

The remaining scores are

$$
88,\ 92,\ 79,\ 85,\ 81,\ 86,\ 90,\ 83,\ 89
$$

There are now

$$
N = 9
$$

scores.

Their sum is

$$
773
$$

So the new mean is

$$
\bar{x}_{\text{new}} = \frac{773}{9} \approx 85.89
$$

The new sample standard deviation is

$$
\sigma_{\text{new}} \approx 4.31
$$

## Final Result

For all 11 scores:

$$
\bar{x} \approx 85.91
$$

$$
\sigma \approx 5.58
$$

After removing the highest and lowest scores:

$$
\bar{x}_{\text{new}} \approx 85.89
$$

$$
\sigma_{\text{new}} \approx 4.31
$$

## Interpretation

Removing the highest and lowest values hardly changes the mean, but it reduces the spread of the data, so the standard deviation becomes smaller.