# Spherical harmonics

## One-sentence meaning

Spherical harmonics are orthogonal angular patterns on a sphere, indexed by a degree $\ell$ and an azimuthal index $m$.

## Prerequisites

[[Orthogonal, orthonormal and complete]]; [[Basic Legendre polynomials]]; polar angle $\theta$, azimuth $\phi$, complex exponentials.

## Core equations

$$Y_{\ell m}(\theta,\phi)\propto P_\ell^m(\cos\theta)e^{im\phi},\qquad
\ell=0,1,\ldots,\quad -\ell\le m\le\ell,$$
$$d\Omega=\sin\theta\,d\theta\,d\phi,\qquad
\int_{S^2}Y_{\ell m}^*Y_{\ell'm'}\,d\Omega=\delta_{\ell\ell'}\delta_{mm'}$$
for the conventional unit normalization. For $m\ge0$, one common convention is
$$P_\ell^m(x)=(-1)^m(1-x^2)^{m/2}\frac{d^mP_\ell(x)}{dx^m}.$$
Normalization and phase conventions must be used consistently. HW0 1(b) only asks for proportionality to the two deltas.

## Where they come from

The azimuthal modes $e^{im\phi}$ are periodic around the axis. The associated Legendre factor supplies the polar-angle shape regular on the sphere. Separating angular dependence explains why two indices appear; a full angular eigenvalue derivation is deferred. Orthogonality can be understood by first separating the $\phi$ integral and then the polar integral.

## Assumptions

Scalar functions on the full unit sphere, with the spherical measure $d\Omega$. The complete infinite set spans $L^2(S^2)$; a truncated set or a masked-sky inner product does not retain all of the full-sphere properties. No claim of pointwise convergence for arbitrary functions is needed.

## Physical meaning

$\ell$ labels angular structure; $m$ labels variation around the chosen axis. For $m=0$, there is no azimuthal variation and the polar shape is $P_\ell(\cos\theta)$. These are functions of direction, not radial distance.

## When to use it

Organize angular dependence and understand the orthogonality requested in HW0 1(b). CMB angular maps provide a familiar application, without extending this note into CMB analysis or multipole radiation.

## Example

$Y_{00}=1/\sqrt{4\pi}$ is constant over the sphere. $Y_{10}=\sqrt{3/(4\pi)}\cos\theta$ has opposite signs in the two hemispheres. These illustrate constant and dipolar angular patterns.

## Common confusion

**Earlier gap: what does $P_\ell^m$ mean?** It is an associated Legendre function, not a power. **Does the star mean another harmonic?** It means complex conjugation in the inner product. **Why two Kronecker deltas?** Both mode labels must match for a nonzero overlap. **Does orthogonality alone establish completeness?** No; that is a separate property of the full family.

## Related concepts

[[Basic Legendre polynomials]]; [[Orthogonal, orthonormal and complete]]; [[Green functions]] (future).

## Used in

[[Homework/HW0 Map#Problem 1b|HW0 1(b)]]. Listed as useful background in [[Sources/Course Sources#Syllabus|the syllabus]]. No detailed spherical-harmonic derivation in the supplied typed Lecture 1–2 sections; keep this at introductory discussion depth.
