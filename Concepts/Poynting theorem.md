# Poynting theorem

## One-sentence meaning

Poynting's theorem balances local field-energy storage, electromagnetic energy flow, and energy transferred to matter.

## Prerequisites

[[Maxwell equations]]; [[Work and J dot E]]; [[Vector fields, divergence and curl]]; [[Electromagnetic energy density]]; [[Poynting vector]].

## Core equations

$$\boxed{\partial_tu+\nabla\cdot\mathbf S=-\mathbf J\cdot\mathbf E}.$$
$$\frac{d}{dt}\int_Vu\,dV=-\oint_{\partial V}\mathbf S\cdot\mathbf n\,dA-\int_V\mathbf J\cdot\mathbf E\,dV.$$
All terms in the local equation have units energy/(volume time).

## Where they come from

1. Solve Ampère–Maxwell for $\mathbf J$: $\mathbf J=(c/4\pi)\nabla\times\mathbf B-(1/4\pi)\partial_t\mathbf E$.
2. Dot with $\mathbf E$ and use the divergence identity in [[Poynting vector]].
3. Insert Faraday's law for $\nabla\times\mathbf E$.
4. Combine the two squared-field time derivatives into $\partial_tu$.

This is the short derivational path of Lecture 1 §1.6. The divergence theorem gives the fixed-volume form.

## Assumptions

Microscopic fields in Gaussian units, fixed control volume, outward normals. This is a field-energy balance. To write a total field-plus-matter balance, include any matter energy transported across the boundary or other work channels.

## Physical meaning

Read it as “rate of increase of field energy here + net outward field-energy flow here = negative rate of energy given to matter here.” It is an instantaneous balance, not a statement that the left-hand side stays constant in time.

## When to use it

Decide whether energy supplied to matter comes from a declining field store, incoming flux, or both. Integrate when a total power through boundaries is easier to evaluate than local derivatives.

## Example

Suppose $\partial_tu=0$ but $\mathbf J\cdot\mathbf E=p_0>0$ in a region. Then $\nabla\cdot\mathbf S=-p_0$: net inflow replenishes the energy transferred to matter. Conversely, if $J=0$ and net outward flux is positive, field energy decreases.

## Common confusion

**Earlier water analogy:** The user suggested a jar inside the sink to represent matter's separate energy store. The sink's water store models field energy; water routed into the jar models field-to-matter transfer. The sink can keep the same water level if incoming flow replenishes what enters the jar. This helps only if both stores and boundary flows are tracked explicitly.

**“Density change plus flux change per volume should stay constant”?** The sum equals $-\mathbf J\cdot\mathbf E$ at each time; it need not be constant. Divergence, not curl, measures net outward flow.

**Equal left inflow and right outflow means divergence is unchanged?** With no other boundary flux, the integral of divergence is zero. Pointwise zero needs an additional local condition, such as uniform $\mathbf S$.

**Source wording:** Lecture 1's prose after eq. (41) calls the surface integral inward flux. With outward $\mathbf n$, the integral itself is outward; its negative is inward. See [[Sources/Course Sources#Clarifications retained with the source]].

## Related concepts

[[Electromagnetic energy density]]; [[Poynting vector]]; [[Work and J dot E]]; [[Maxwell stress tensor]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §§1.5–1.6, eqs. (32)–(42). Energy-conservation context for [[Homework/HW1 Map#Problem 1a|HW1 1(a)]]; no direct derivation problem in supplied HW0/HW1.
