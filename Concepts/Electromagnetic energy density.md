# Electromagnetic energy density

## One-sentence meaning

Electromagnetic energy density is the amount of energy stored in the fields per unit volume.

## Prerequisites

[[Gaussian units and the 1 over c factors]]; squared vector magnitude; density versus total amount.

## Core equations

$$u=\frac{E^2+B^2}{8\pi},\qquad U_{\rm field}=\int_Vu\,dV,$$
$$u_E=\frac{E^2}{8\pi},\qquad u_B=\frac{B^2}{8\pi}.$$
Here $E^2=\mathbf E\cdot\mathbf E$ and $B^2=\mathbf B\cdot\mathbf B$.

## Where they come from

In the [[Poynting theorem]] derivation, $\mathbf E\cdot\partial_t\mathbf E=\tfrac12\partial_tE^2$ and the analogous magnetic term combine into $\partial_t[(E^2+B^2)/(8\pi)]$. This identifies the standard microscopic field energy density.

## Assumptions

Microscopic/vacuum expression in Gaussian units. Do not use it unchanged for a macroscopic material energy budget. Lecture 2 §1.10 introduces a different expression involving $D,H$ and warns about separating field and matter contributions; that extension is outside this initial note.

## Physical meaning

$u$ tells how much energy is present locally. $\partial_tu$ tells how quickly that local store changes. Neither says by itself how much energy is passing through.

## When to use it

Compute field energy, separate electric and magnetic contributions, or start a magnetic-energy calculation such as [[Homework/HW1 Map#Problem 1a|HW1 1(a)]].

## Example

A uniform electric field $E_0$ filling a region of volume $V$, with $B=0$, stores $E_0^2V/(8\pi)$ in that region. Doubling $E_0$ quadruples the energy density.

## Common confusion

**Earlier question: density versus flux?** $u$ has units energy/volume; [[Poynting vector|$\mathbf S$]] has units energy/(area time). Constant $u$ does not imply zero flux. **Does “field energy” mean only waves?** Static electric and magnetic fields store energy too.

## Related concepts

[[Poynting theorem]]; [[Poynting vector]]; [[Work and J dot E]]; [[Maxwell stress tensor]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §1.6, eqs. (39)–(40); [[Homework/HW1 Map#Problem 1a|HW1 1(a)]] and [[Homework/HW1 Map#Problem 1b|1(b)]].
