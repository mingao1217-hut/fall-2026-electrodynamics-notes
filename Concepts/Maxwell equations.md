# Maxwell equations

## One-sentence meaning

Maxwell's equations relate the local spatial and temporal structure of electromagnetic fields to charge and current.

## Prerequisites

[[Vector fields, divergence and curl]]; [[Gaussian units and the 1 over c factors]]; [[Current density]].

## Core equations

$$\nabla\cdot\mathbf E=4\pi\rho,\qquad\nabla\cdot\mathbf B=0,$$
$$\nabla\times\mathbf E=-\frac1c\frac{\partial\mathbf B}{\partial t},\qquad
\nabla\times\mathbf B=\frac{4\pi}{c}\mathbf J+\frac1c\frac{\partial\mathbf E}{\partial t}.$$
For macroscopic fields, the corresponding source equations are $\nabla\cdot\mathbf D=4\pi\rho_{\rm free}$ and $\nabla\times\mathbf H=(4\pi/c)\mathbf J_{\rm free}+(1/c)\partial_t\mathbf D$; the other two equations retain $\mathbf E,\mathbf B$.

## Where they come from

At this stage these are the physical starting laws, not consequences of a more fundamental theory studied here. The divergence theorem and Stokes' theorem connect them to enclosed charge, magnetic flux, circulation of $E$, and circulation of $B$. Taking the divergence of the Ampère–Maxwell equation and using Gauss' law gives $\partial_t\rho+\nabla\cdot\mathbf J=0$.

## Assumptions

The first set uses microscopic fields and total charge/current in Gaussian units. “Vacuum” in the lecture's heading does not require $\rho=\mathbf J=0$ everywhere. A source-free region is an additional restriction. Macroscopic matter requires distinguishing total and free sources.

## Physical meaning

The divergence equations constrain fields on a time slice. The curl equations connect their evolution to spatial variation and current. Nonzero curl does not require arrows to trace visibly circular field lines everywhere.

## When to use it

Choose the relevant source and symmetry first. For stationary currents, $\partial_t\mathbf E=0$ yields $\nabla\times\mathbf B=4\pi\mathbf J/c$. For electrostatics, $\nabla\times\mathbf E=0$.

## Example

For a spherically symmetric isolated point charge, Gauss' law gives $4\pi r^2E_r=4\pi q$, hence $E_r=q/r^2$ outside the origin. Divergence is zero away from the charge, although the field is nonzero.

## Common confusion

**Does zero divergence mean no field or no flow?** No: it means no local net source of that flux. **Do Gaussian vacuum equations use SI $\epsilon_0$?** No: use the course's normalization consistently.

## Related concepts

[[Lorentz force]]; [[Poynting theorem]]; [[Maxwell stress tensor]]; [[Green functions]] (future).

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §§1.1–1.4, especially eqs. (19)–(24). [[Homework/HW1 Map#Problem 1a|HW1 1(a)]]; [[Homework/HW1 Map#Problem 3|HW1 3]].
