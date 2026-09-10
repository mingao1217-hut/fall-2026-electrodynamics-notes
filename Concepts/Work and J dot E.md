# Work and J dot E

## One-sentence meaning

$\mathbf J\cdot\mathbf E$ is the rate per unit volume at which the electromagnetic field transfers energy to matter.

## Prerequisites

[[Lorentz force]]; [[Current density]]; work as force dotted with displacement.

## Core equations

$$\frac{dW}{dt}=\mathbf F\cdot\mathbf v=q\mathbf E\cdot\mathbf v,$$
$$p_{\rm matter}=\mathbf J\cdot\mathbf E,\qquad
P_{\rm field\to matter}=\int_V\mathbf J\cdot\mathbf E\,dV.$$
For a scalar Ohmic conductivity, $\mathbf J\cdot\mathbf E=\sigma E^2$.

## Where they come from

Divide $dW=\mathbf F\cdot d\mathbf x$ by $dt$. Insert the Lorentz force; the magnetic term vanishes because its cross product is perpendicular to velocity. Sum the electric power over charges per volume.

## Assumptions

This is electromagnetic work on matter; other energy transfers may also occur. Identifying the integral with the change of all matter energy inside a fixed volume additionally requires accounting for matter flowing across its boundary. $\sigma E^2\ge0$ assumes a passive scalar conductivity $\sigma\ge0$.

## Physical meaning

Positive $\mathbf J\cdot\mathbf E$ means matter gains energy from the field. Negative means matter transfers energy to the field. This is an exchange term, so field energy alone need not be conserved.

## When to use it

Identify the exchange term in [[Poynting theorem]] or compute heating in a simple conductor.

## Example

For a uniform Ohmic conductor of volume $V$, uniform $E$ and scalar $\sigma$, the electrical power delivered to matter is $\sigma E^2V$.

## Common confusion

**Does matter gaining energy require local field energy density to fall?** No. Incoming electromagnetic energy can replenish it. A steady $u$ with positive $\mathbf J\cdot\mathbf E$ requires negative $\nabla\cdot\mathbf S$.

**Is all electromagnetic work immediately heat?** No. Depending on the system it can become ordered kinetic energy or other matter energy.

## Related concepts

[[Poynting theorem]]; [[Electromagnetic energy density]]; [[Poynting vector]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §§1.5–1.6, eqs. (33)–(38). Background for the energy viewpoint in [[Homework/HW1 Map#Problem 1a|HW1 1(a)]], not an independent homework question.
