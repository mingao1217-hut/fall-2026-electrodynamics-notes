# Maxwell stress tensor

## One-sentence meaning

The Maxwell stress tensor converts a surface orientation into electromagnetic traction and organizes field-mediated momentum balance.

## Prerequisites

[[Rank-2 tensors and outer products]]; [[Lorentz force]]; [[Maxwell equations]]; [[Vector fields, divergence and curl]].

## Core equations

$$T_{ij}=\frac1{4\pi}\left(E_iE_j+B_iB_j-\frac12\delta_{ij}(E^2+B^2)\right),$$
$$\mathbf g=\frac{\mathbf E\times\mathbf B}{4\pi c}=\frac{\mathbf S}{c^2},\qquad
f_i=\partial_jT_{ij}-\partial_tg_i,$$
$$\mathbf F_{\rm EM}=\oint_{\partial V}T\cdot\mathbf n\,dA-\frac{d}{dt}\int_V\mathbf g\,dV.$$
For static fields, the field-momentum derivative vanishes: $\mathbf F_{\rm EM}=\oint T\cdot\mathbf n\,dA$.

## Where they come from

Start from $\mathbf f=\rho\mathbf E+\mathbf J\times\mathbf B/c$. Eliminate $\rho,\mathbf J$ using Maxwell's equations. The product rule extracts $\partial_t(\mathbf E\times\mathbf B)/(4\pi c)$. The remaining terms are spatial derivatives; for example,
$$[\mathbf E(\nabla\cdot\mathbf E)-\mathbf E\times(\nabla\times\mathbf E)]_i
=\partial_j\left(E_iE_j-\tfrac12\delta_{ij}E^2\right).$$
Adding the magnetic counterpart gives $\partial_jT_{ij}$.

## Assumptions

This is the lecture's microscopic/vacuum Gaussian stress convention. For a force on a material object, choose an enclosing surface in vacuum where possible. Do not insert fields inside a dielectric into this vacuum formula without addressing matter stresses. A time-dependent problem must retain the field-momentum term.

## Physical meaning

$T_{ij}n_j$ is traction: force per area associated with the surface in the balance. Index $i$ selects the force/momentum component and $j$ selects the normal component. With the displayed sign convention, the outward electromagnetic momentum-flux tensor in a continuity equation is $-T$: $\partial_tg_i+\partial_j(-T_{ij})=-f_i$. This prevents a sign ambiguity in the phrase “momentum flux.”

## When to use it

Calculate force using fields on a surface, especially when a direct sum over microscopic charges is difficult. HW1 3 explicitly requires this approach.

## Example

For $\mathbf E=E_0\hat{\mathbf x}$ and $B=0$,
$$T=\frac{E_0^2}{8\pi}\operatorname{diag}(1,-1,-1).$$
An $x$-normal face has positive $x$ traction; a $y$-normal face has negative $y$ traction. For a closed box in a spatially uniform field, opposite-face contributions cancel. This does not mean each face has zero traction.

## Common confusion

**Earlier propagation/spiral explanation:** The tensor is rank 2 because momentum direction and surface-normal direction are independent, even in electrostatics.

**Do static fields imply zero electromagnetic force?** No. Lecture 2 eq. (79) appends “$=0$”; static fields alone justify dropping the field-momentum derivative, not setting the electromagnetic force to zero. Supports or other forces may balance a nonzero electromagnetic force.

**Which index is differentiated?** Here $(\nabla\cdot T)_i=\partial_jT_{ij}$. The lecture later interchanges index order in places; Maxwell stress is symmetric, $T_{ij}=T_{ji}$, so that swap leaves it unchanged. Do not assume this for arbitrary tensors.

## Related concepts

[[Poynting theorem]] (scalar energy balance versus vector momentum balance); [[Rank-2 tensors and outer products]]; [[Electromagnetic energy density]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §1.8, eqs. (59)–(61); [[Sources/Course Sources#Lecture 2|Lecture 2]] §1.8, eqs. (62)–(79), PDF pp. 1–2. [[Homework/HW1 Map#Problem 3|HW1 3]].
