# Task 14 – Hadamard Gate and the “Schrödinger’s Cat” State

## Problem Statement

The qubit basis states are

$$
|0\rangle =
\begin{pmatrix}
1 \\
0
\end{pmatrix},
\qquad
|1\rangle =
\begin{pmatrix}
0 \\
1
\end{pmatrix}
$$

The Hadamard gate is

$$
H = \frac{1}{\sqrt{2}}
\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}
$$

Show that applying $H$ to

$$
|0\rangle
$$

gives

$$
|\psi\rangle = \frac{1}{\sqrt{2}}|0\rangle + \frac{1}{\sqrt{2}}|1\rangle
$$

Then explain why this is a superposition and why it is sometimes illustratively called a “Schrödinger's cat” state.

## Theory

A quantum state is a superposition when it is written as a linear combination of basis states. Matrix multiplication gives the action of a gate on a qubit.

## Step-by-Step Solution

Apply the Hadamard gate to

$$
|0\rangle
$$

$$
H|0\rangle =
\frac{1}{\sqrt{2}}
\begin{pmatrix}
1 & 1 \\
1 & -1
\end{pmatrix}
\begin{pmatrix}
1 \\
0
\end{pmatrix}
$$

Now perform the multiplication:

$$
H|0\rangle =
\frac{1}{\sqrt{2}}
\begin{pmatrix}
1 \cdot 1 + 1 \cdot 0 \\
1 \cdot 1 + (-1) \cdot 0
\end{pmatrix}
$$

$$
H|0\rangle =
\frac{1}{\sqrt{2}}
\begin{pmatrix}
1 \\
1
\end{pmatrix}
$$

Now write this in the basis-state form:

$$
\frac{1}{\sqrt{2}}
\begin{pmatrix}
1 \\
1
\end{pmatrix}
=
\frac{1}{\sqrt{2}}
\begin{pmatrix}
1 \\
0
\end{pmatrix}
+
\frac{1}{\sqrt{2}}
\begin{pmatrix}
0 \\
1
\end{pmatrix}
$$

Therefore,

$$
|\psi\rangle = \frac{1}{\sqrt{2}}|0\rangle + \frac{1}{\sqrt{2}}|1\rangle
$$

## Final Result

After the Hadamard gate acts on

$$
|0\rangle
$$

the final state is

$$
|\psi\rangle = \frac{1}{\sqrt{2}}|0\rangle + \frac{1}{\sqrt{2}}|1\rangle
$$

## Interpretation

This state is a superposition because it contains both basis states

$$
|0\rangle
$$

and

$$
|1\rangle
$$

at the same time in the mathematical description.

It is sometimes illustratively compared with a “Schrödinger's cat” state because the system is not in only one classical alternative before measurement. Instead, it is in a coherent combination of two possible outcomes. The comparison is pedagogical: a single-qubit superposition is a very simple quantum example of the broader idea that quantum systems can exist in combinations of classically distinct states.