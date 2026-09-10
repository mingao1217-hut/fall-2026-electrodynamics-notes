# Gaussian units and the 1 over c factors

## One-sentence meaning

Gaussian units assign electric and magnetic fields the same dimensions, placing explicit factors of $1/c$ in their dynamical coupling and magnetic force.

## Prerequisites

[[Vector fields, divergence and curl]]; dimensions of length, time, velocity and force.

## Core equations

In the lecture's parametrization,
$$k_1=1,\qquad k_2=1/c^2,\qquad k_3=1/c.$$
$$\nabla\times\mathbf E=-\frac1c\partial_t\mathbf B,\qquad
\nabla\times\mathbf B=\frac{4\pi}{c}\mathbf J+\frac1c\partial_t\mathbf E.$$
$$\mathbf F=q\left(\mathbf E+\frac{\mathbf v}{c}\times\mathbf B\right).$$
Heaviside–Lorentz uses $k_1=1/(4\pi)$ and $k_2=1/(4\pi c^2)$ with the same $k_3=1/c$. It is a different normalization of fields and charges.

## Where they come from

Lecture 1 starts with proportionality constants in Maxwell's equations. With $E$ and $B$ assigned equal dimensions, $c^{-1}\partial_t$ and $\nabla$ both have dimensions inverse length. The lecture fixes $k_3=1/c$ and $k_2/k_1=1/c^2$, so the source-free equations propagate at speed $c$. Choosing $k_1=1$ completes the Gaussian convention.

## Assumptions

Keep $c$ explicit for this course. Dimensional consistency checks the equations but does not alone establish the measured numerical wave speed. Do not combine field values from SI and Gaussian formulas without conversion.

## Physical meaning

The ratio $v/c$ is dimensionless. Since $E$ and $B$ have equal dimensions, it lets the two terms inside the Lorentz-force parentheses be added. The factors reflect unit conventions; they do not represent a separate physical suppression mechanism introduced by changing units.

## When to use it

Use this note when comparing Jackson with the lectures or checking missing factors in force, energy and inductance formulas.

## Example

If $\mathbf v\perp\mathbf B$, then $F_B/F_E=(v/c)(B/E)$ for the magnitudes of the separate magnetic and electric contributions. This becomes $v/c$ only when the field magnitudes are equal.

## Common confusion

**Earlier question: should I follow Nils' Gaussian convention?** Yes: Lecture 1 explicitly selects Gaussian units. Heaviside–Lorentz with $c=1$ is discussed as another choice, not the working convention.

**Is $1/c$ needed because a curl adds a time derivative?** No. Curl differentiates in space. The factor converts a time derivative to compatible dimensions.

## Related concepts

[[Maxwell equations]]; [[Lorentz force]]; [[Electromagnetic energy density]]; [[Poynting vector]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §1.1, eqs. (1)–(6), table 1; §1.2. [[Homework/HW1 Map|HW1]] throughout. No dedicated units problem in [[Homework/HW0 Map|HW0]].
