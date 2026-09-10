# Poynting vector

## One-sentence meaning

The Poynting vector gives the local electromagnetic energy flux, including its direction.

## Prerequisites

[[Vector fields, divergence and curl]]; [[Gaussian units and the 1 over c factors]]; cross products.

## Core equations

$$\mathbf S=\frac{c}{4\pi}\mathbf E\times\mathbf B,\qquad
P_{\rm outward}=\oint_{\partial V}\mathbf S\cdot\mathbf n\,dA.$$
$[S]=$ energy/(area time); $[\nabla\cdot\mathbf S]=$ energy/(volume time).

## Where they come from

The vector identity $\nabla\cdot(\mathbf E\times\mathbf B)=\mathbf B\cdot(\nabla\times\mathbf E)-\mathbf E\cdot(\nabla\times\mathbf B)$ converts part of the electric work expression into a spatial divergence. Its coefficient identifies $\mathbf S$ in [[Poynting theorem]].

## Assumptions

Microscopic/vacuum Gaussian formula. Use outward unit normal $\mathbf n$ for a closed volume. The macroscopic expression in the lecture involves $\mathbf E\times\mathbf H$, not automatically $\mathbf E\times\mathbf B$.

## Physical meaning

$\mathbf S\cdot\mathbf n$ measures energy per area per time crossing a chosen surface. Positive means outward with the chosen outward normal. $\nabla\cdot\mathbf S$ measures local net export, not the magnitude of energy transport.

## When to use it

Find energy crossing a surface or explain how energy reaches matter while local field energy remains steady.

## Example

If $\mathbf E=E_0\hat{\mathbf x}$ and $\mathbf B=B_0\hat{\mathbf y}$, then $\mathbf S=(cE_0B_0/4\pi)\hat{\mathbf z}$. A uniform $\mathbf S$ carries equal flux in and out of a box and has zero divergence. This is a local flux example; no wave solution is assumed.

## Common confusion

**Does nonzero $S$ imply decreasing energy inside?** Only net outward flux affects the balance. Equal inflow and outflow can give zero net loss. **Is its divergence a curl?** No: the curl equations help derive $S$, but its divergence enters the energy balance.

## Related concepts

[[Poynting theorem]]; [[Electromagnetic energy density]]; [[Work and J dot E]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §1.6, eqs. (36)–(42). Foundational energy-flux context for [[Homework/HW1 Map|HW1]]; no direct Poynting-flux problem in supplied HW0/HW1.
