# Vector fields, divergence and curl

## One-sentence meaning

A vector field assigns an arrow to each point; divergence measures local net outward flow, while curl measures local circulation.

## Prerequisites

Components of a vector; partial derivatives; dot and cross products. These are entry skills, not additional assumed EM knowledge.

## First-pass intuition

### How to read this note

**Physical question:** Given arrows throughout a region, how can we tell whether they describe local net outward flow, local circulation, both, or neither?

We will start with an arrow and a slope. Then we will build two different measurements: a tiny box tests outward flow; a tiny loop tests circulation. These are the ideas behind the divergence and curl symbols in [[Maxwell equations]] and the energy balance in [[Poynting theorem]]. You do not need those EM equations to begin.

The water and paddle-wheel pictures below are **intuition**, easiest to interpret when the arrows represent a fluid velocity. The derivative and integral equations are **formal statements**. An electric field is not literally water, but the same mathematical operations still apply.

Read one subsection at a time. Try each pause question before opening its answer. These checkpoints are for reconstruction, not claims that you have already mastered the steps.

### 1. One arrow: separate its location from its components

A vector has a magnitude and direction. In a flat drawing, we can describe it with two numbers: how much it points right and how much it points up. Negative numbers mean left or down.

We use bold $\mathbf F$ for the vector. Its components are $F_x,F_y,F_z$. The subscript tells us **which direction the component points**, not where the arrow is located. The symbols $\hat{\mathbf x},\hat{\mathbf y},\hat{\mathbf z}$ are unit vectors: arrows of length one along the coordinate axes. A hat here means “unit direction.”

For example, $\mathbf F=2\hat{\mathbf x}-\hat{\mathbf y}$ has components $(2,-1,0)$. It points right and down. We have not yet said whether another location has the same vector.

A **vector field** supplies that missing information: it assigns a vector to each location. In $\mathbf F(x,y,z)$, the arguments in parentheses label the location where we evaluate the field.

**Worked micro-example.** Let $\mathbf F(x,y,z)=(x,y,0)$, using dimensionless coordinates and components for this teaching example. The rule says to use the point's $x$ coordinate as the rightward component and its $y$ coordinate as the upward component.

| Location | Substitution | Field arrow |
| --- | --- | --- |
| $(1,0,0)$ | $(x,y,0)=(1,0,0)$ | Right |
| $(0,1,0)$ | $(x,y,0)=(0,1,0)$ | Up |
| $(-1,0,0)$ | $(x,y,0)=(-1,0,0)$ | Left |
| $(0,-1,0)$ | $(x,y,0)=(0,-1,0)$ | Down |

Together the arrows spread away from the origin. That is a description of how arrows vary with **position**. It does not say that the field changes with **time**.

> **Pause:** At $(2,1,0)$, what arrow does this rule assign? If the arrow at one point is nonzero, does that tell you whether neighboring arrows differ?

<details>
<summary>Check your reasoning</summary>

The assigned arrow is $(2,1,0)$. A nonzero arrow does not establish spatial variation: the uniform field $(2,1,0)$ at every point has the same value at this point but different neighbors from the field $(x,y,0)$.

</details>

### 2. Comparing neighbors: what a partial derivative asks

For a function of one variable, a derivative is a local slope: change in the function divided by a small change in the input. A field has several component functions and several possible directions in which to move. We must specify both.

The symbol $\partial_xF_y$ is short for $\partial F_y/\partial x$. Read it as:

> “Move a little in the $x$ direction, holding the other coordinates fixed. How quickly does the **$y$ component** change?”

The direction of motion and the direction of the component being compared need not be the same.

For the field $\mathbf F=(-y,x,0)$, the component functions are $F_x=-y$, $F_y=x$, $F_z=0$. Therefore:

- $\partial_xF_y=1$: moving right by a small amount increases the upward component by that amount.
- $\partial_yF_x=-1$: moving up makes the rightward component more negative, so it points more strongly left.
- $\partial_xF_x=0$: moving right does not change $-y$ when $y$ is held fixed.

All of these compare different locations at one instant. None is a time derivative.

The symbol $\nabla$, pronounced “del” or “nabla,” packages spatial derivatives. In Cartesian coordinates it stands for $(\partial_x,\partial_y,\partial_z)$. It is a differential operator: something to apply to a field, not an ordinary arrow with numerical components. The dot or cross written after it specifies which combination of derivatives to take.

> **Pause:** Does $\partial_xF_y$ mean “the field points along $x$”? What is it for $\mathbf F=(x,y,0)$?

<details>
<summary>Check your reasoning</summary>

No. It asks how the $y$ component changes as position changes along $x$. For $(x,y,0)$, $F_y=y$ does not depend on $x$, so $\partial_xF_y=0$.

</details>

### 3. A tiny box: build divergence from outward flow

**Intuition.** Imagine arrows describing water velocity. Water can enter and leave a small box. The relevant question is not “is water moving?” but “is more flowing out than in?”

A surface has a **normal**, meaning a perpendicular direction. We use $\mathbf n$ for a unit normal. On a closed box we choose it to point outward: right on the right face, left on the left face, and similarly on the other faces.

The dot product $\mathbf F\cdot\mathbf n$ selects the field component perpendicular to the face. It is positive for outward arrows, negative for inward arrows, and zero for arrows parallel to the face. Multiplying by the face area measures the flux through that face if the field is uniform over it. For a varying field, we sum small surface patches using an integral.

**Formal bridge, one pair of faces.** Let a tiny box have widths $\Delta x,\Delta y,\Delta z$, where $\Delta$ means a small finite change. Its right and left faces have area $\Delta y\Delta z$. To leading order, their combined outward flux is

$$[F_x(x+\Delta x)-F_x(x)]\,\Delta y\Delta z.$$

Here $y,z$ are held fixed and suppressed in the notation. The right face contributes positively; the left face carries a minus sign from its outward normal. Divide by the box volume $\Delta x\Delta y\Delta z$:

$$\frac{F_x(x+\Delta x)-F_x(x)}{\Delta x}\ \longrightarrow\ \partial_xF_x.$$

The arrow means “approaches as the box shrinks.” The other face pairs give $\partial_yF_y$ and $\partial_zF_z$. Adding all three gives **divergence**, a scalar:

$$\nabla\cdot\mathbf F=\partial_xF_x+\partial_yF_y+\partial_zF_z.$$

Term by term, each derivative measures the imbalance associated with one pair of opposite faces. Their sum measures the local net outward flux per unit volume. It can be positive, negative, or zero.

**Worked micro-example.** Return to $\mathbf F=(x,y,0)$:

$$\partial_xF_x=\partial_xx=1,\qquad
\partial_yF_y=\partial_yy=1,\qquad
\partial_zF_z=\partial_z0=0.$$

So the divergence is $1+1+0=2$. For a direct check, take a unit cube with $0\le x,y,z\le1$. The right face has outward flux 1 and the left face 0. The top $y$ face has outward flux 1 and the bottom one 0. The $z$ faces have zero flux. Total outward flux is 2; volume is 1. Their ratio agrees with divergence 2.

Compare a uniform field $(1,0,0)$. The right face has outward flux $+1$, the left face $-1$. The field is nonzero, but the net outward flux is zero.

These are geometric field examples, not proposed steady incompressible-water solutions. For a velocity field, divergence measures local volume expansion. For an actual transported quantity, the appropriate flux may also include its density.

> **Pause:** If twice as much leaves a small box as enters it, what sign do you expect for its average divergence? Does zero divergence mean nothing crosses its faces?

<details>
<summary>Check your reasoning</summary>

The average divergence is positive because the net flux is outward. Zero divergence does not prohibit transport: equal inward and outward flux can cancel.

</details>

### 4. A tiny loop: build curl from circulation

**Intuition.** A box tests arrows crossing its faces. To test circulation, trace a small closed loop and ask how much the arrows line up with the direction you walk. Arrows along your walk contribute positively; arrows against it negatively; perpendicular arrows contribute zero.

The small directed displacement along the path is $d\boldsymbol\ell$. The quantity $\mathbf F\cdot d\boldsymbol\ell$ selects the tangential component and multiplies it by the small distance walked. Adding this around the loop is **circulation**. The closed-integral symbol $\oint$ means to integrate all the way around the closed path.

**Formal bridge in the $xy$ plane.** Trace a tiny rectangle counterclockwise as seen from the positive $z$ side. Its bottom edge is traversed rightward and its top edge leftward. To leading order, their combined contribution is

$$[F_x(y)-F_x(y+\Delta y)]\Delta x
\approx-\partial_yF_x\,\Delta x\Delta y.$$

The right edge is traversed upward and the left edge downward, giving

$$[F_y(x+\Delta x)-F_y(x)]\Delta y
\approx\partial_xF_y\,\Delta x\Delta y.$$

Add them and divide by the rectangle's area. As it shrinks, circulation per unit area becomes

$$ (\nabla\times\mathbf F)_z=\partial_xF_y-\partial_yF_x.$$

Term by term: the first derivative compares the upward field on the right and left; the second compares the rightward field on the top and bottom. Its minus sign comes from the opposing directions of traversal. This is why the expression uses cross-direction derivatives rather than the same-direction derivatives of divergence.

**Why a vector, and why $z$?** Circulation can be measured in differently oriented planes. Curl packages those oriented measurements into a vector. Curl's $z$ component measures circulation in the $xy$ plane. Curl's $x$ component measures circulation in the $yz$ plane, and its $y$ component measures circulation in the $zx$ plane.

The right-hand rule fixes the sign: curl your fingers along the positive traversal direction; your thumb gives the positive normal. A positive $z$ curl does **not** mean the field arrows or fluid move upward out of the page. It identifies the axis perpendicular to the circulation plane.

For a field entirely in the $xy$ plane with no $z$ dependence, the other curl components vanish. A paddle wheel turning within the page has an axle perpendicular to the page, which helps explain this direction. For a velocity field, curl is related to local rotation; the paddle-wheel image is a guide, not the definition for every kind of field.

> **Pause:** Can arrows confined to the page have curl pointing out of the page? Which two directions are being distinguished?

<details>
<summary>Check your reasoning</summary>

Yes. The arrows show the field's direction. Curl shows the axis of local circulation. Those are different directions describing different properties.

</details>

### 5. Work through the two fields that looked confusing

All coordinates and components in this subsection are dimensionless teaching examples.

**Field A: $\mathbf F=(-y,x,0)$.** At the right of the origin it points up; at the top it points left; at the left it points down; at the bottom it points right. These arrows circulate counterclockwise.

First ask about net outward flow:

$$\nabla\cdot\mathbf F=\partial_x(-y)+\partial_yx+\partial_z0=0+0+0=0.$$

Then ask about circulation in the $xy$ plane:

$$ (\nabla\times\mathbf F)_z=\partial_xx-\partial_y(-y)=1-(-1)=2.$$

The two positive contributions reinforce each other. The complete curl vector is $(0,0,2)$. No $z$-directed field component was needed.

**Field B: $\mathbf F=(x,y,0)$.** The arrows spread outward. We already found divergence 2. Its $z$ curl is

$$ (\nabla\times\mathbf F)_z=\partial_xy-\partial_yx=0-0=0.$$

The field varies in space, yet its local circulation is zero. Spatial variation alone is not enough to establish nonzero curl; the pattern of variation matters.

| Field | Divergence | Curl | What the comparison teaches |
| --- | --- | --- | --- |
| $(-y,x,0)$ | $0$ | $(0,0,2)$ | Circulation can occur without net outward flow |
| $(x,y,0)$ | $2$ | $(0,0,0)$ | Net outward flow can occur without circulation |
| $(1,0,0)$ | $0$ | $(0,0,0)$ | Nonzero field need not have either |

**A useful intermediate question:** “If the field is zero at the origin, how can its curl or divergence be nonzero there?” Both examples have a zero arrow at the origin. Derivatives compare neighboring arrows, so a zero value at one point does not require zero derivatives there. This is the same reason the function $f(x)=x$ has value zero but slope 1 at $x=0$.

### 6. Reconstruct the density-versus-flux question

The earlier question was whether the flux term becomes “per volume” because of curl. It helps to separate three steps rather than remember only the correction.

First, **what is already being measured?** In [[Poynting vector]], $\mathbf S$ measures electromagnetic energy crossing an area per unit time. Its units are energy/(area time). It is already a flux density; it is not stored energy per volume.

Second, **what do opposite faces tell us?** Their difference measures net outward energy flow. Dividing by the little box volume and shrinking the box produces $\nabla\cdot\mathbf S$, just as in the box construction above.

Third, **how do the units work?** A spatial derivative contributes one inverse length:

$$\frac{\text{energy}}{\text{area}\times\text{time}}
\times\frac1{\text{length}}
=\frac{\text{energy}}{\text{volume}\times\text{time}}.$$

This can be added to the time derivative of stored energy density in [[Poynting theorem]]. The derivative itself is not an instruction to divide by a whole volume. The volume interpretation emerges from the face-flux difference divided by box volume.

Curl also contributes one inverse length, so dimensions alone cannot decide between divergence and curl. The **physical question** decides: energy balance counts net flow across a closed surface, which is the divergence construction.

**Another earlier step: “equal inflow and outflow means divergence is unchanged.”** Equal total inflow and outflow fixes the *net flux* to zero. It tells us the volume average of divergence is zero, not whether a local value changed over time and not necessarily whether it is zero at every point.

**Worked micro-example of the distinction.** Let $\mathbf F=(x^2,0,0)$ in the box $-1\le x\le1$, $0\le y,z\le1$. At the right face, outward flux is $+1$. At the left face it is $-1$, because the outward normal points left while the field points right. Other faces contribute zero. Total outward flux is therefore zero.

But locally $\nabla\cdot\mathbf F=\partial_xx^2=2x$: it is negative on the left and positive on the right. The contributions cancel when summed across the box. A boundary measurement of zero net flux does not force every local contribution to be zero.

> **Pause:** If energy flows through a box at the same rate in and out, can the Poynting vector be nonzero? What additional information would let you conclude its divergence is zero everywhere?

<details>
<summary>Check your reasoning</summary>

The Poynting vector can be nonzero. Equal total inflow and outflow establish zero integrated divergence. Spatially uniform $\mathbf S$ throughout the region would be a sufficient extra condition for pointwise zero divergence.

</details>

### 7. Read the integral statements before using them

The compact reference below keeps both integral theorems. Here is their notation before you encounter them there:

| Symbol | Meaning |
| --- | --- |
| $V$, $dV$ | A three-dimensional region and a small volume element |
| $\partial V$ | The boundary surface of that region; $\partial$ here denotes a boundary, not a derivative |
| $A$, $dA$ | An oriented surface and a small area element |
| $\partial A$ | The edge curve bounding that surface |
| $\mathbf n$ | A unit normal; outward for the closed surface of a volume |
| $d\boldsymbol\ell$ | A small tangent displacement in the chosen direction along a curve |
| $\int$, $\oint$ | Continuous sums; the circle marks a closed surface or closed path in these formulas |

**Divergence theorem, term by term:** the volume integral of $\nabla\cdot\mathbf F$ adds all local outward imbalances inside $V$. The surface integral of $\mathbf F\cdot\mathbf n$ adds the flux across the outside boundary. They agree because adjacent small boxes have shared-face contributions with opposite normals, so internal contributions cancel.

**Stokes' theorem, term by term:** the surface integral of $(\nabla\times\mathbf F)\cdot\mathbf n$ adds the local circulation normal to the surface. The curve integral of $\mathbf F\cdot d\boldsymbol\ell$ adds the tangential field around its edge. They agree because neighboring tiny loops traverse their shared edges in opposite directions. Choose the boundary traversal to match the normal by the right-hand rule.

Neither statement says a finite boundary measurement determines every derivative inside. Each relates a summed interior quantity to a boundary sum.

The full three-dimensional curl formula below lists the same construction for the $yz$, $zx$, and $xy$ planes, respectively. For example its first component, $\partial_yF_z-\partial_zF_y$, tests circulation in the $yz$ plane. Learn the plane/direction relationship before treating the expression as a memorized string of derivatives.

The following sections retain the original compact reference. The teaching examples above explain its mathematics; they are not additional lecture claims or homework solutions.

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

## Later review

| Question | Compact answer |
| --- | --- |
| What is a vector field? | An arrow assigned to each position; distinguish position from arrow components. |
| What does $\partial_xF_y$ ask? | How the $y$ component changes when moving in the $x$ direction. |
| What does divergence test? | Local net outward flux per volume; scalar result. |
| What does curl test? | Local circulation per oriented area; vector result normal to the circulation plane. |
| Why is 2D curl along $z$? | An $xy$-plane circulation has its axis along $z$, not along the field arrows. |
| Why is $\nabla\cdot\mathbf S$ a power per volume? | $\mathbf S$ is power per area; one spatial derivative adds inverse length. |
| What does equal total inflow/outflow establish? | Zero integrated divergence; pointwise zero requires more information. |

Reconstruct without looking: for $(-y,x,0)$ obtain divergence $0$ and curl $(0,0,2)$; for $(x,y,0)$ obtain divergence $2$ and curl zero. Explain the direction as well as the numbers. If that is difficult, revisit subsections 2–5 before [[Maxwell equations]].
