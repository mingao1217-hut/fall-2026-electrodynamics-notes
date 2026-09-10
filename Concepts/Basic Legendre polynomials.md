# Basic Legendre polynomials

## One-sentence meaning

Legendre polynomials are mutually orthogonal polynomial shapes on $[-1,1]$ that also describe axisymmetric angular patterns through $x=\cos\theta$.

## Prerequisites

[[Orthogonal, orthonormal and complete]]; polynomials; differentiation and integration.

## Core equations

$$P_0(x)=1,\qquad P_1(x)=x,\qquad P_2(x)=\tfrac12(3x^2-1),$$
$$\frac{d}{dx}\left[(1-x^2)\frac{dP_\ell}{dx}\right]+\ell(\ell+1)P_\ell=0,$$
$$\int_{-1}^{1}P_\ell(x)P_k(x)\,dx=\frac{2}{2\ell+1}\delta_{\ell k}.$$
Rodrigues' formula supplies the standard normalization:
$$P_\ell(x)=\frac1{2^\ell\ell!}\frac{d^\ell}{dx^\ell}(x^2-1)^\ell.$$
The normalized version is $\sqrt{(2\ell+1)/2}\,P_\ell$.

## Where they come from

At the basic level, the differential equation selects regular angular modes; nonnegative integer $\ell$ gives these polynomial solutions. To see orthogonality, multiply the equations for two different degrees by the opposite polynomial, subtract and integrate. The boundary term vanishes at $\pm1$, leaving their unequal eigenvalues times the overlap equal to zero. No full separation-of-variables derivation is claimed as mastered.

## Assumptions

The displayed orthogonality uses weight 1 on $[-1,1]$. For another interval, map the coordinate and include the Jacobian in an integral. The full polynomial family is complete in $L^2([-1,1])$; a finite truncation is an approximation.

## Physical meaning

$P_0$ is a constant shape; $P_1$ changes sign from one end to the other; $P_2$ has a different, even pattern. Setting $x=\cos\theta$ turns them into axisymmetric shapes on a sphere.

## When to use it

Recognize the polynomial basis in HW0 1(c), understand the $m=0$ part of [[Spherical harmonics]], and compute basic mode overlaps.

## Example

$\int_{-1}^{1}P_0P_1\,dx=\int_{-1}^{1}x\,dx=0$, while $\int_{-1}^{1}P_1^2\,dx=2/3$, not 1. This separates orthogonality from normalization without solving a homework proof.

## Common confusion

**Earlier gap: what is $P_\ell$?** It is a named family of functions, not a new physical field.

**Can I cite Sturm–Liouville theory to prove orthogonality?** The equation gives a short direct route through subtraction and a boundary term. Whether merely citing a theorem meets a homework “show” request depends on the expected justification; this note preserves the idea without claiming a completed proof submission.

**Is $P_\ell^m$ the $m$th power of $P_\ell$?** No: it denotes an associated Legendre function; see [[Spherical harmonics]].

## Related concepts

[[Orthogonal, orthonormal and complete]]; [[Spherical harmonics]]; [[Green functions]] (future).

## Used in

[[Homework/HW0 Map#Problem 1c|HW0 1(c)]] explicitly names the basis; [[Homework/HW0 Map#Problem 1b|1(b)]] uses its associated-function extension. Basic definitions support study discussion; no exact typed lecture section for Legendre theory is verified. See [[Sources/Course Sources#Scope and provenance]].
