# HW0 Map

Source: `Homework0.pdf`, PHYS-6561, Fall 2026, 5 pages. This is a problem-setup and learning-status map, not a solution set. Exact assignment references: [[Sources/Course Sources#Homework sources]].

## Assignment overview

| Problem | Topic | Lecture connection | Main prerequisites |
| --- | --- | --- | --- |
| 1(a) | Sine-mode orthogonality | Mathematical preparation; no dedicated typed lecture section verified | [[Orthogonal, orthonormal and complete]] |
| 1(b) | Spherical-harmonic orthogonality | Syllabus background; no full derivation verified in Lecture 1–2 | [[Spherical harmonics]]; [[Basic Legendre polynomials]] |
| 1(c) | Assess bases for an exponential | Mathematical preparation | Orthogonality, completeness, interval and weight |
| 2(a) | Tensor decomposition | Lecture 1 §1.7; HW supplies the spacetime-metric extension | [[Rank-2 tensors and outer products]] |
| 3(a–d) | Coordinate transformations and invariants | Lecture 1 §1.7 gives Cartesian-rotation background; HW extends it to coordinate bases | Components, chain rule, Jacobians, metric |

## Problem 1a

- **Relevant lecture sections:** mathematical prerequisite work; Lecture 1 §1.7 offers the vector-inner-product analogy, not this function integral.
- **Prerequisite concepts:** [[Orthogonal, orthonormal and complete]]; trigonometric identities and definite integrals.
- **Physical/mathematical system:** sine functions on a full interval $[0,2\pi]$.
- **Knowns:** functions $\sin(mx)$, $\sin(nx)$ and integration limits. The stated $\pi\delta_{mn}$ result is read with positive integer mode labels; including the zero sine mode would need separate treatment.
- **Unknowns:** the overlap integral for equal and unequal indices, and its interpretation.
- **Symmetry:** integer-frequency periodicity; swapping $m,n$ leaves the overlap unchanged.
- **Assumptions:** weight 1, positive integer $m,n$; specify these before manipulating the expression.
- **Governing equations:** $\langle f_m,f_n\rangle=\int_0^{2\pi} f_m^*f_n\,dx$; the requested target is $\langle\sin(mx),\sin(nx)\rangle=\pi\delta_{mn}$.
- **Understanding/status:**
  - [ ] Explain what the overlap tests.
  - [ ] Distinguish the equal-index and unequal-index cases.
  - [ ] Identify whether the stated functions are normalized.
  - [ ] Attempted; checked; remaining questions recorded after discussion.

## Problem 1b

- **Relevant lecture sections:** background named in the syllabus; no exact full spherical-harmonic derivation verified in typed Lecture 1–2.
- **Prerequisite concepts:** [[Spherical harmonics]], [[Basic Legendre polynomials]], [[Orthogonal, orthonormal and complete]]; complex conjugation.
- **Physical/mathematical system:** scalar angular modes on the full sphere.
- **Knowns:** $Y_{\ell m}$ and $Y_{\ell'm'}$; $d\Omega=\sin\theta\,d\theta\,d\phi$.
- **Unknowns:** why the overlap vanishes unless both index pairs match; normalization constant is explicitly not required by the assignment.
- **Symmetry:** azimuthal periodicity; full-sphere angular integration.
- **Assumptions:** integer $\ell\ge0$, $|m|\le\ell$; consistent associated-Legendre and harmonic conventions; full sphere, not a cut-sky domain.
- **Governing equations:** $Y_{\ell m}\propto P_\ell^m(\cos\theta)e^{im\phi}$ and the inner product on $S^2$. Requested target: overlap proportional to $\delta_{\ell\ell'}\delta_{mm'}$.
- **Understanding/status:**
  - [ ] Explain the roles of $\ell$, $m$, conjugation and $\sin\theta$.
  - [ ] Identify what the azimuthal integral tests.
  - [ ] Identify what polar-angle overlap remains, without assuming completeness proves orthogonality.
  - [ ] Attempted; checked; unresolved steps identified.

## Problem 1c

- **Relevant lecture sections:** mathematical preparation; no exact matching typed Lecture 1–2 section.
- **Prerequisite concepts:** [[Orthogonal, orthonormal and complete]]; [[Basic Legendre polynomials]]; approximation and convergence.
- **Physical/mathematical system:** approximate $e^{-ax}$ on $[0,2\pi]$. The source writes the interval variable as $q$; the intended reading here is $x\in[0,2\pi]$.
- **Knowns:** target family and interval; proposed sine-only, cosine-only, combined trigonometric, monomial, Legendre and other Jacobi polynomial families.
- **Unknowns:** whether each specified family spans the needed targets and whether it provides a useful finite approximation. The problem does not give a numerical $a$ or an error tolerance.
- **Symmetry:** inspect the target under the interval's relevant reflection or periodic extension; do not assume it has even/odd symmetry without defining an origin and extension.
- **Assumptions:** make the allowed frequencies, inclusion of the constant mode, approximation norm, real/complex parameter choice and interval mapping explicit. “Good basis” can mean completeness, convergence efficiency or numerical conditioning; these are different tests.
- **Governing equations:** expansion $f\approx\sum_{n=0}^N a_n\phi_n$; inner-product projection for orthogonal families. To use Legendre's standard interval, a coordinate mapping is needed. Jacobi weights are an identified prerequisite gap; no new Jacobi-polynomial lesson is added here.
- **Understanding/status:**
  - [ ] State what “good” means for this comparison.
  - [ ] Examine each of the six proposed families separately.
  - [ ] Distinguish orthogonality from completeness and finite-truncation accuracy.
  - [ ] Distinguish integer full-period modes from a differently scaled half-range basis.
  - [ ] Record which Jacobi background needs instruction before attempting that comparison.
  - [ ] Attempted; checked; unresolved comparisons recorded.

## Problem 2a

- **Relevant lecture sections:** [[Sources/Course Sources#Lecture 1|Lecture 1]] §1.7, eqs. (43)–(58), supplies tensors and contractions; HW0 PDF pp. 2–3 supplies the additional metric setup.
- **Prerequisite concepts:** [[Rank-2 tensors and outer products]], symmetric/antisymmetric matrices, trace, repeated-index contraction.
- **Physical/mathematical system:** arbitrary covariant tensor $T_{\mu\nu}$ in $n$ Cartesian spacetime dimensions, with $\eta_{\mu\nu}=\operatorname{diag}(-1,+1,\ldots)$.
- **Knowns:** $\eta_{\mu\nu}\eta^{\nu\sigma}=\delta_\mu{}^\sigma$, $\eta^{\mu\nu}\eta_{\mu\nu}=n$, and the assignment's proposed split into trace, symmetric traceless and antisymmetric pieces.
- **Unknowns:** verify the split, show the pieces have the specified properties, show mutual orthogonality and uniqueness.
- **Symmetry:** behavior under interchanging the two indices; trace versus traceless parts.
- **Assumptions:** raise indices with the stated metric. “Orthogonal” here uses tensor contraction, not an assumed positive-definite Euclidean norm.
- **Governing equations:** trace $T=\eta^{\mu\nu}T_{\mu\nu}$; symmetric/antisymmetric projections $(T_{\mu\nu}\pm T_{\nu\mu})/2$; metric contraction $A_{\mu\nu}B^{\mu\nu}$. The full proposed identity is supplied in HW0 eq. (21); its proof is not copied here.
- **Understanding/status:**
  - [ ] Keep the scalar trace distinct from the original tensor with the same letter.
  - [ ] Explain symmetric, antisymmetric and traceless.
  - [ ] Verify reconstruction and each defining property.
  - [ ] Check orthogonality using the correct metric contraction.
  - [ ] Explain uniqueness without assuming positivity of the metric.
  - [ ] Attempted; checked; remaining questions identified.

## Problem 3

- **Relevant lecture sections:** Lecture 1 §1.7 is the Cartesian tensor background. HW0 PDF pp. 3–4 supplies the more general coordinate transformation.
- **Prerequisite concepts:** [[Rank-2 tensors and outer products]]; chain rule, matrix inverse, spherical coordinates, coordinate basis versus unit basis. These last items are prerequisite gaps to teach as needed, not new full concept notes in this pass.
- **Physical/mathematical system:** one Euclidean spatial geometry described in Cartesian and spherical coordinates.
- **Knowns:** $x=r\sin\theta\cos\phi$, $y=r\sin\theta\sin\phi$, $z=r\cos\theta$; barred indices for Cartesian coordinates, unbarred for spherical. The assignment defines $J^\mu{}_{\bar\nu}=\partial x^\mu/\partial x^{\bar\nu}$.
- **Unknowns:** (a) both Jacobians and whether they are diagonal; (b) spherical components of a Cartesian unit $x$ vector and whether its identity changes; (c) invariance of the inner product; (d) whether vectors related through the inverse Jacobian represent the same geometric vector.
- **Symmetry:** coordinate independence of geometric vectors and scalar products; the spherical chart is position-dependent.
- **Assumptions:** work away from coordinate singularities; use a consistent azimuthal branch. The source's $\arctan(y/x)$ alone does not specify all quadrants. Coordinate-basis components from a Jacobian are not automatically components in the orthonormal spherical unit-vector basis.
- **Governing equations:** chain rule; $J J^{-1}=I$; $v^\mu=J^\mu{}_{\bar\nu}v^{\bar\nu}$; $\mathbf k\cdot\mathbf l=g_{\mu\nu}k^\mu l^\nu=k^\mu l_\mu$, with metric obtained from basis dot products. No transformed components or completed proof are supplied here.
- **Understanding/status:**
  - [ ] Identify input/output coordinates of each Jacobian before differentiating.
  - [ ] Explain why changing components need not change the vector.
  - [ ] Distinguish a coordinate basis from unit vectors.
  - [ ] Account for the metric in part (c).
  - [ ] Interpret part (d) geometrically, not just as matrix multiplication.
  - [ ] Parts (a), (b), (c), (d) attempted and checked individually.

## Assignment status

- [x] Source inspected and all problem setups mapped.
- [ ] User-confirmed submission status recorded.
- [ ] User-confirmed self-grading status recorded.
- [ ] Remaining questions updated after a guided attempt.

No unchecked box is a claim that the user has not already done the work; individual completion status was not verified in this pass. See [[00 Course Map]] for the conceptual route.
