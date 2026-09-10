# Fall 2026 Electrodynamics — Course Map

This vault develops concepts from fundamentals upward. Start with the physical question, check the prerequisites, then work through one section at a time. A written note means the idea has been discussed; it does **not** certify mastery.

## Physical map

The first lectures connect three questions: how charges and currents determine fields, how fields exchange energy with matter, and how fields exert forces and transport momentum. HW0 refreshes the mathematical language needed to describe those relations. HW1 applies magnetic energy and stress to concrete systems.

## Dependencies and learning order

Each row gives a next step and the ideas it depends on. These are learning dependencies, not a claim that every topic was derived in lecture.

| Stage | Topic | Understand first | Main result or purpose |
| --- | --- | --- | --- |
| Mathematical entry | [[Vector fields, divergence and curl]] | Components, partial derivatives, dot/cross products | Distinguish outward flow from circulation |
| Mathematical entry | [[Orthogonal, orthonormal and complete]] | Dot products, integrals, conjugation | Distinguish overlap, unit norm and spanning |
| Polynomial modes | [[Basic Legendre polynomials]] | Orthogonality and polynomials | Basis on $[-1,1]$; shapes in $\cos\theta$ |
| Angular modes | [[Spherical harmonics]] | Legendre functions, orthogonality, spherical angles | Modes on the sphere; HW0 1(b) |
| Two directional slots | [[Rank-2 tensors and outer products]] | Vector components, orthonormal bases | Transform and contract tensors |
| Unit conventions | [[Gaussian units and the 1 over c factors]] | Spatial derivatives, dimensions | Follow Nils' Gaussian convention |
| Sources | [[Current density]] | Charge density, vector fields, flux | Charge transport and $I=\int\mathbf J\cdot d\mathbf A$ |
| Field laws | [[Maxwell equations]] | Divergence, curl, units, current density | Source constraints and evolution |
| Forces | [[Lorentz force]] | Cross products, Gaussian units | Force on moving charges |
| Energy exchange | [[Work and J dot E]] | Lorentz force, current density, work | Power per volume delivered to matter |
| Energy storage | [[Electromagnetic energy density]] | Units, squared field magnitudes | $u=(E^2+B^2)/(8\pi)$ |
| Energy transport | [[Poynting vector]] | Cross products, surface flux, units | $\mathbf S=c\mathbf E\times\mathbf B/(4\pi)$ |
| Energy balance | [[Poynting theorem]] | Maxwell, work, storage, transport | $\partial_tu+\nabla\cdot\mathbf S=-\mathbf J\cdot\mathbf E$ |
| Momentum balance | [[Maxwell stress tensor]] | Maxwell, Lorentz force, tensors, divergence | Surface traction and field momentum |

Energy storage and flux can be understood physically before their derivation from Maxwell's equations. The cross-links between those notes and Poynting's theorem reflect that two-pass learning path.

## Lecture coverage

- [[Sources/Course Sources#Lecture 1|Lecture 1]] §§1.1–1.4: units, Maxwell equations, and a brief introduction to matter. §§1.5–1.6: force, work, energy balance. §1.7: Cartesian tensors. §1.8 begins momentum conservation and stops after eq. (61).
- [[Sources/Course Sources#Lecture 2|Lecture 2]] §1.8: momentum density and Maxwell stress, eqs. (62)–(79). Later sections on angular momentum, macroscopic conservation, potentials and gauges are present in the source, but presence in a PDF is not evidence we have studied them fully. No new standalone concept notes for them in this initial set.
- [[Green functions]]: **future link only**. Possible preparation includes Maxwell equations, differential equations, boundary conditions, and orthogonal-function expansions. Do not populate this topic until we study its setup.

## Homework maps

- [[Homework/HW0 Map]] — functions, tensor decomposition, coordinate transformations.
- [[Homework/HW1 Map]] — magnetic energy, inductance, dielectric-sphere force. The supplied PDF says Fall 2025; the map records the provided assignment without relabeling its source.

HW2–HW6 and solution PDFs are available in the project but excluded from this initial scope. No exam-problem links are invented.

## Learning checkpoints to revisit

- [ ] Explain the difference between divergence and curl using a tiny box and a tiny loop.
- [ ] Explain why equal total inflow/outflow gives zero integrated divergence, not necessarily zero pointwise divergence.
- [ ] Track the units of $u$, $\mathbf S$, $\partial_tu$, $\nabla\cdot\mathbf S$ and $\mathbf J\cdot\mathbf E$.
- [ ] Explain steady field energy while matter gains energy.
- [ ] Explain the two directional slots of stress without invoking propagation or spiraling fields.
- [ ] Distinguish orthogonality, normalization, completeness and uniqueness of coefficients.
- [ ] Recognize $P_\ell$, $P_\ell^m$ and $Y_{\ell m}$.

These are questions to check in a guided session, not a record of failed or completed work.

## Source discipline

[[Sources/Course Sources]] records source locations, version ambiguity and narrowly identified corrections. [[AGENTS]] records the maintenance rules. Course PDFs remain the authority for coverage and conventions; no transcripts or copied solution sets are stored here.
