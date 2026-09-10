# Vector fields, divergence and curl

## One-sentence meaning

A vector field assigns an arrow to each point; divergence measures local net outward flow, while curl measures local circulation.

## Prerequisites

Components of a vector; partial derivatives; dot and cross products. These are entry skills, not additional assumed EM knowledge.

## Core equations

$$\mathbf F=F_x\hat{\mathbf x}+F_y\hat{\mathbf y}+F_z\hat{\mathbf z},\qquad
\nabla\cdot\mathbf F=\partial_xF_x+\partial_yF_y+\partial_zF_z.$$
$$\nabla\times\mathbf F=(\partial_yF_z-\partial_zF_y,\ \partial_zF_x-\partial_xF_z,\ \partial_xF_y-\partial_yF_x).$$
$$\int_V\nabla\cdot\mathbf F\,dV=\oint_{\partial V}\mathbf F\cdot\mathbf n\,dA,\qquad
\int_A(\nabla\times\mathbf F)\cdot\mathbf n\,dA=\oint_{\partial A}\mathbf F\cdot d\boldsymbol\ell.$$
The first integral identity is the divergence theorem; the second is the circulation form of Stokes' theorem.

## Where they come from

For a tiny box, subtract inward flux from outward flux on opposite faces and divide by volume: the limit gives divergence. For a tiny oriented loop, add the tangential contributions around its edges and divide by area: the limit gives the normal component of curl.

## Assumptions

Use Cartesian derivative formulas in Cartesian coordinates. Fields must be sufficiently smooth locally; integral statements need suitable boundaries. Singular sources require an integral or distributional treatment.

## Physical meaning

Divergence is a scalar: positive means local net outward flux. Curl is an axial vector: its direction is the right-hand-rule axis of circulation, not the direction of the field arrow. A tiny paddle wheel is a useful intuition for a velocity field. A spatial derivative contributes units of inverse length; it does not literally mean dividing by volume.

## When to use it

Use divergence for charge constraints and energy balance. Use curl for Maxwell's induction laws and to diagnose local circulation.

## Example

For $\mathbf F=(-y,x,0)$, $\nabla\cdot\mathbf F=0$ and $\nabla\times\mathbf F=(0,0,2)$. For $\mathbf F=(x,y,0)$, divergence is $2$ and curl is zero. The first circulates; the second spreads outward. For a uniform field both derivatives vanish although the field is nonzero.

## Common confusion

**Earlier question: does the flux-per-volume term come from curl?** No: energy balance uses $\nabla\cdot\mathbf S$. Since $\mathbf S$ already has units energy/(area time), one spatial derivative gives energy/(volume time).

**Earlier question: should 2D curl point along $x$?** For an $xy$-plane field independent of $z$, its curl can only point along $z$: $(\nabla\times\mathbf F)_z=\partial_xF_y-\partial_yF_x$.

**Equal inflow and outflow means divergence is “unchanged”?** It means the volume-integrated divergence is zero if these are the only boundary fluxes. It does not determine pointwise divergence without more information.

## Related concepts

[[Maxwell equations]]; [[Poynting theorem]]; [[Poynting vector]]; [[Maxwell stress tensor]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §§1.2, 1.6, eqs. (19)–(20), (36), (41)–(42); [[Sources/Course Sources#Lecture 2|Lecture 2]] §1.8. [[Homework/HW1 Map#Problem 1a|HW1 1(a)]] and [[Homework/HW1 Map#Problem 3|HW1 3]].
