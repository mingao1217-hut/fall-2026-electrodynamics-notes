# Orthogonal, orthonormal and complete

## One-sentence meaning

Orthogonal modes have zero mutual overlap, orthonormal modes also have unit norm, and a complete set can represent every member of the specified function space in the specified sense.

## Prerequisites

Dot products; integrals; complex conjugation for complex functions.

## Core equations

$$\langle f,g\rangle=\int_D f^*(x)g(x)w(x)\,dx,$$
$$\langle f_m,f_n\rangle=N_n\delta_{mn}\quad\text{(orthogonal)},\qquad N_n=1\quad\text{(orthonormal)}.$$
For an orthogonal expansion, $a_n=\langle f_n,f\rangle/N_n$ and $f\sim\sum_na_nf_n$. Completeness means the expansion can converge to every target in the chosen space, for example in the $L^2$ norm.

## Where they come from

This is the vector dot-product idea extended to functions: multiply matching values and sum by integration. Orthogonality kills cross terms when projecting onto one mode, leaving its coefficient times its norm. Completeness is a further property of the full set, not a consequence of this projection step.

## Assumptions

Specify domain, weight, allowed indices and convergence notion. For an ordinary positive inner product, $w>0$ almost everywhere. HW0 2 uses a different, indefinite metric contraction: the usual positive-norm geometric intuition needs care there.

## Physical meaning

Orthogonality separates coefficients; normalization sets the scale of a mode; completeness determines whether any needed direction is missing. Unique coefficients within an orthogonal set do not prove that every target can be represented.

## When to use it

Choose or assess modes for expansions and check what an orthogonality integral actually proves in HW0.

## Example

The two vectors $\hat{\mathbf x},\hat{\mathbf y}$ are orthonormal in $\mathbb R^3$ but incomplete there, since they cannot represent $\hat{\mathbf z}$. They are complete in the $xy$ plane. Multiplying them by 2 preserves orthogonality but removes unit normalization.

## Common confusion

**Earlier question: orthogonal versus orthonormal?** Zero overlap between different members is not unit norm.

**Does orthogonality prove completeness or uniqueness of every expansion?** It gives unique coefficients for an expansion that exists (with the appropriate convergence). Completeness is separate.

**Are sine-only or cosine-only sets always incomplete?** No universal answer: the interval, frequency family and function space matter. Half-range bases on a suitable interval differ from restricting an integer-frequency full-period Fourier family. HW0 1(c) must be assessed with its stated interval, rather than an unexplained slogan about parity.

## Related concepts

[[Basic Legendre polynomials]]; [[Spherical harmonics]]; [[Rank-2 tensors and outer products]]; [[Green functions]] (future).

## Used in

[[Homework/HW0 Map#Problem 1a|HW0 1(a)]], [[Homework/HW0 Map#Problem 1b|1(b)]], [[Homework/HW0 Map#Problem 1c|1(c)]]. [[Sources/Course Sources#Lecture 1|Lecture 1]] §1.7, eqs. (46)–(49), for orthonormal vector bases; no dedicated function-space lecture section verified in the supplied typed lectures.
