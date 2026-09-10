# HW1 Map

Source: `Homework1.pdf`, one page, labeled **PHYS-6561 — Fall 2025**. This is the supplied assignment to map; whether its year label is stale is unresolved. No solutions from `Homework1_solns.pdf` were used. Source details: [[Sources/Course Sources#Homework sources]].

## Assignment overview

| Problem | Physical system | Lecture connection | Main tools |
| --- | --- | --- | --- |
| 1(a) | Stationary currents in empty space | Lecture 1 §1.6; Lecture 2 §2.1 and Coulomb-gauge subsection | Magnetic field energy, vector potential, integration by parts |
| 1(b) | Multiple current circuits | Same magnetic-energy framework; circuit reduction supplied by HW | Current density, energy as a quadratic form |
| 2 | Two coaxial circular loops | Lecture 1 §1.4 for permeability; builds on HW1 1(b) | Geometry, mutual inductance, elliptic integrals |
| 3 | Dielectric sphere with a vacuum cut | Lecture 1 §1.4; Lecture 2 §1.8 | Maxwell stress and dielectric boundary conditions |

Potentials, inductance, elliptic integrals and interface conditions appear here only as required problem tools. Their appearance does not mark them as mastered or authorize adding full new conceptual chapters.

## Problem 1a

- **Relevant lecture sections:** [[Sources/Course Sources#Lecture 1|Lecture 1]] §1.6 eq. (39), $u_B=B^2/(8\pi)$; §1.2, static Ampère law. [[Sources/Course Sources#Lecture 2|Lecture 2]] §2.1 eq. (95), $\mathbf B=\nabla\times\mathbf A$; §2.2 Coulomb-gauge setup. The explicit stationary-source integral is a needed bridge, not a verified derivation already mastered.
- **Prerequisite concepts:** [[Current density]], [[Electromagnetic energy density]], [[Maxwell equations]], [[Vector fields, divergence and curl]], [[Gaussian units and the 1 over c factors]].
- **Physical system:** current-carrying elements in empty space, with stationary currents.
- **Knowns:** $\mathbf J(\mathbf x)$; the all-space magnetic energy expression; the assignment's hint to replace one $\mathbf B$ by $\nabla\times\mathbf A$.
- **Unknown:** express magnetic energy solely as a double integral over source currents, as requested in the PDF.
- **Symmetry:** no spatial symmetry is imposed; symmetry under exchanging integration points will matter when interpreting source pairs.
- **Assumptions:** stationary currents; localized sources with sufficient decay for the boundary term at infinity to vanish; finite source distributions or explicit treatment of singular idealizations.
- **Governing equations:** $W=(1/8\pi)\int B^2\,dV$, $\mathbf B=\nabla\times\mathbf A$, $\nabla\times\mathbf B=4\pi\mathbf J/c$; a dot/curl divergence identity. The magnetostatic relation between $\mathbf A$ and $\mathbf J$ must be established or supplied with its assumptions during the guided attempt. No integrated solution chain is recorded here.
- **Understanding/status:**
  - [ ] Explain what $W$, $\mathbf A$ and $\mathbf J$ represent.
  - [ ] State which time derivatives vanish and why.
  - [ ] Identify the boundary term before deciding it vanishes.
  - [ ] Identify the missing potential-source relation and its unit convention.
  - [ ] Attempted; checked; remaining questions recorded.

## Problem 1b

- **Relevant lecture sections:** Lecture 1 §1.6 energy framework; HW1 1(a) is the immediate prerequisite. No dedicated inductance section was verified in typed Lecture 1–2.
- **Prerequisite concepts:** [[Current density]], [[Electromagnetic energy density]], current-to-circuit reduction, pair counting.
- **Physical system:** $n$ circuits carrying currents $I_1,\ldots,I_n$.
- **Knowns:** circuit geometry, chosen positive current directions, and the energy functional from part (a).
- **Unknowns:** integral expressions for self-inductance $L_i$ and mutual inductance $M_{ij}$, using the assignment's energy convention.
- **Symmetry:** interchange of circuits under reciprocal magnetostatic conditions; count each distinct circuit pair once.
- **Assumptions:** fixed circuit geometry and current profiles scaling linearly with their circuit currents; empty-space setting inherited from part (a). Finite conductor cross-section or a justified regularization is needed for self-energy; an infinitely thin filament has a singular self-term.
- **Governing equation:** the assignment defines the energy form
  $$W=\frac12\sum_iL_iI_i^2+\sum_i\sum_{j>i}M_{ij}I_iI_j.$$
  Keep the factors of $c$ in the derived coefficients consistent with this convention rather than importing SI inductance expressions.
- **Understanding/status:**
  - [ ] Explain self terms versus mutual terms.
  - [ ] Explain why the two sums use different counting conventions.
  - [ ] State how current orientation affects mutual terms.
  - [ ] Flag the ideal-filament self-energy issue before evaluating integrals.
  - [ ] Attempted; checked; unresolved steps recorded.

## Problem 2

- **Relevant lecture sections:** Lecture 1 §1.4, especially eq. (31), for $\mathbf B=\mu\mathbf H$; HW1 1(b) for mutual-inductance setup. No elliptic-integral reduction section was verified in the typed sources.
- **Prerequisite concepts:** [[Gaussian units and the 1 over c factors]], current loops, mutual inductance from 1(b), parametrization of circles. Elliptic integrals and near-coincident-loop asymptotics are explicit remaining tools, not presumed knowledge.
- **Physical system:** two circular coaxial loops of radii $a,b$, with centers separated by $d$, in a homogeneous medium with permeability $\mu$.
- **Knowns:** $a,b,d,\mu$; the target expression in HW1 eq. (23), written using complete elliptic integrals $K(k)$ and $E(k)$, with
  $$k^2=\frac{4ab}{(a+b)^2+d^2}.$$
- **Unknowns:** verify the stated mutual-inductance expression and characterize its limit for $d\ll a,b$ and $a\approx b$.
- **Symmetry:** common-axis rotations reduce the geometry to the difference of the two azimuthal angles; interchange of loop labels.
- **Assumptions:** interpret the specified scalar $\mu$ as a uniform linear isotropic permeability; consistent loop orientation; thin-loop model with distinct loops. The exactly coincident-filament configuration is singular and cannot be treated as a generic finite endpoint.
- **Governing equations:** mutual-energy/circuit integral from 1(b) with the medium factor, circle parametrization, and the assignment's elliptic modulus. Clarify whether a formula or software uses modulus $k$ or parameter $m=k^2$ before comparing results.
- **Understanding/status:**
  - [ ] Sketch the common axis, radii and separation.
  - [ ] Identify separation and tangent-vector factors in the circuit integral.
  - [ ] State the relevant definition of $K,E$ before attempting reduction.
  - [ ] Identify the limit of $k$ and which small geometric scales regulate it.
  - [ ] Attempted; checked; missing mathematical tools recorded.

## Problem 3

- **Relevant lecture sections:** Lecture 1 §1.4 for dielectric response; Lecture 2 §1.8 eqs. (73)–(79) for Maxwell stress. The assignment explicitly allows the sphere's interior field from Jackson §4.4. No additional textbook derivation is assumed.
- **Prerequisite concepts:** [[Maxwell stress tensor]], [[Rank-2 tensors and outer products]], [[Maxwell equations]], [[Gaussian units and the 1 over c factors]]; electrostatic boundary conditions at a dielectric–vacuum interface.
- **Physical system:** a dielectric sphere of radius $a$ and relative permittivity $\epsilon$ in a uniform external field $\mathbf E_0$, cut through its center perpendicular to the field; vacuum in the cut and outside.
- **Knowns:** $a$, $\epsilon$, $\mathbf E_0$; permitted uncut-sphere interior result
  $$\mathbf E_{\rm in}=\frac{3}{\epsilon+2}\mathbf E_0.$$
- **Unknown:** force of attraction between hemispheres, obtained using Maxwell stress as explicitly required.
- **Symmetry:** axial symmetry around $\mathbf E_0$, reflection across the cut plane; force direction follows the axis.
- **Assumptions:** electrostatic, linear isotropic dielectric with no imposed free charge on the cut. To use the supplied uncut-sphere field, interpret the cut as an infinitesimal vacuum gap before significant geometric rearrangement. A finite gap would require a changed field solution.
- **Governing equations:** vacuum stress $T_{ij}=(E_iE_j-\tfrac12\delta_{ij}E^2)/(4\pi)$, $\mathbf F=\oint T\cdot\mathbf n\,dA$; tangential $E$ continuity and normal $D$ jump condition from Maxwell's equations. The surface and field on each part of it must be identified before integration.
- **Understanding/status:**
  - [ ] Draw one chosen hemisphere and a closed integration surface.
  - [ ] Distinguish the field inside the dielectric from the field in the vacuum gap.
  - [ ] State the interface conditions and outward normals.
  - [ ] Justify every neglected surface contribution rather than integrating only a convenient face by assumption.
  - [ ] Explain why static fields can still give nonzero electromagnetic force.
  - [ ] Attempted; checked; remaining questions recorded.

## Assignment status

- [x] All supplied HW1 problems mapped without copying solutions.
- [ ] Confirm whether the source's Fall 2025 label is a stale header or an older assignment.
- [ ] User-confirmed submission and self-grading status recorded.
- [ ] Update individual problem understanding after a guided attempt.

Unchecked boxes denote unverified status, not a claim that the work is undone. Return to [[00 Course Map]] for the learning sequence.
