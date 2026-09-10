# Lorentz force

## One-sentence meaning

The Lorentz force gives the electric and magnetic force on a moving charge.

## Prerequisites

[[Gaussian units and the 1 over c factors]]; vector dot and cross products.

## Core equations

$$\mathbf F=q\left(\mathbf E+\frac{\mathbf v}{c}\times\mathbf B\right),\qquad
\mathbf f=\rho\mathbf E+\frac1c\mathbf J\times\mathbf B.$$
Here $\mathbf f$ is force per unit volume.

## Where they come from

The particle force law is a starting physical law in Lecture 1. Summing electric forces over charges per volume produces $\rho\mathbf E$; summing charge times velocity produces $\mathbf J$, giving the magnetic force density.

## Assumptions

Classical charge dynamics in Gaussian units. When applying the particle law, use the physical applied field; singular point-charge self-force requires treatment beyond this note. The continuum expression uses total charge and current.

## Physical meaning

Electric force can be parallel to velocity and transfer energy. Magnetic force is perpendicular to the instantaneous velocity, changing direction without directly doing work.

## When to use it

Find forces on charges or currents, then connect force to energy through a dot product with velocity or to momentum through time evolution.

## Example

For $q>0$, $\mathbf v=v\hat{\mathbf x}$ and $\mathbf B=B\hat{\mathbf z}$ with $\mathbf E=0$, $\mathbf F=-(qvB/c)\hat{\mathbf y}$. The force is perpendicular to the motion.

## Common confusion

**Why $\mathbf v/c$?** See [[Gaussian units and the 1 over c factors]]. **Does the magnetic field do work because it changes motion?** A change in direction alone does not change kinetic energy: $(\mathbf v\times\mathbf B)\cdot\mathbf v=0$.

## Related concepts

[[Current density]]; [[Work and J dot E]]; [[Maxwell stress tensor]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §§1.5, 1.8, eqs. (32)–(33), (59)–(61). Force-law background for [[Homework/HW1 Map#Problem 3|HW1 3]], where the assignment requires stress instead of a direct force sum.
