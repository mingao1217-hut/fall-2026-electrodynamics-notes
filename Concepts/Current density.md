# Current density

## One-sentence meaning

Current density is signed electric charge transported per unit area per unit time, with a direction.

## Prerequisites

[[Vector fields, divergence and curl]]; charge density $\rho$ (charge per volume).

## Core equations

$$\mathbf J=\rho\mathbf v\quad\text{(one common-velocity charge population)},\qquad
\mathbf J=\sum_s n_sq_s\mathbf v_s\quad\text{(multiple populations)},$$
$$I=\int_A\mathbf J\cdot\mathbf n\,dA,\qquad
\partial_t\rho+\nabla\cdot\mathbf J=0.$$
For a simple isotropic Ohmic medium, $\mathbf J=\sigma\mathbf E$.

## Where they come from

In time $dt$, carriers moving normally through area $dA$ sweep volume $v_n\,dt\,dA$. Multiplying by charge per volume and dividing by $dt\,dA$ yields $J_n=\rho v_n$. Charge conservation in a small box gives the continuity equation.

## Assumptions

Use a sum over species when positive and negative carriers move differently. $\mathbf J=\sigma\mathbf E$ is a constitutive approximation for linear, local, isotropic Ohmic response, not a definition valid for every current. The simple relation is normally stated in the material rest frame.

## Physical meaning

The area normal selects which part of the current crosses a surface. Conventional current follows positive charge motion; negatively charged carriers contribute opposite to their velocity. Net charge density can vanish while current is nonzero.

## When to use it

Convert a distributed flow to circuit current; supply the source in [[Maxwell equations]]; calculate local energy transfer with [[Work and J dot E]].

## Example

For uniform axial current density in a wire of area $A$, $I=JA$. A fixed positive lattice with drifting electrons can have nearly zero net $\rho$ but nonzero $\mathbf J$ because the two populations have different velocities.

## Common confusion

**Earlier question: what does $\mathbf J=\sigma\mathbf E$ mean?** A larger electric field drives a proportionally larger current density in that material model. $\sigma$ is conductivity, not charge density.

**Does the lecture's $q\mathbf v\to\mathbf J$ equate their units?** No. It is shorthand for summing $q\mathbf v$ per unit volume. For a finite region, $\sum q\mathbf v$ corresponds to $\int\mathbf J\,dV$.

## Related concepts

[[Lorentz force]]; [[Maxwell equations]]; [[Work and J dot E]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §§1.2, 1.6, 1.8. Ohm's-law interpretation comes from study discussion; no specific lecture equation for it is assigned here. [[Homework/HW1 Map#Problem 1a|HW1 1(a)]] and [[Homework/HW1 Map#Problem 1b|1(b)]].
