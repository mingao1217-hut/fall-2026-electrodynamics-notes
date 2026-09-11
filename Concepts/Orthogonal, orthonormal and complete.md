# Orthogonal, orthonormal and complete

## One-sentence meaning

Orthogonal modes have zero mutual overlap, orthonormal modes also have unit norm, and a complete set can represent every member of the specified function space in the specified sense.

## Prerequisites

Dot products; integrals; complex conjugation for complex functions.

## First-pass intuition

### 1. Start with an arrow and ask how to reconstruct it

**The problem:** We want to describe something complicated by adding simpler pieces. The pieces might be spatial directions, or later functions describing an angular pattern. Three separate questions arise: do the pieces overlap, how are they scaled, and are enough pieces available?

Start with ordinary arrows in a plane. Bold $\mathbf v$ denotes a vector; $(v_x,v_y)$ lists its horizontal and vertical components. Let $\mathbf e_x=(1,0)$ and $\mathbf e_y=(0,1)$ be unit arrows along the axes. “Unit” means length one. Then

$$\mathbf v=(3,2)=3\mathbf e_x+2\mathbf e_y.$$

The numbers 3 and 2 are **coefficients**: how much of each building block we add. A linear combination means multiplying vectors by numbers and adding the results. The **span** of a set is everything we can make this way. A **basis**, in this finite-dimensional setting, is a set of independent building blocks that spans the space. Independent means none can be constructed from the others.

Before using “complete,” ask: what is the target space? Here it is the plane, meaning every pair of real components. In three dimensions we would also need to account for vertical motion out of the plane.

**Intuition:** Think of adjustable contributions to a total. **Formal distinction:** whether all targets can be reconstructed is a statement about the set and its specified target space, not about one successful example.

### 2. Orthogonal: measure overlap before worrying about length

For real vectors $\mathbf a=(a_x,a_y)$ and $\mathbf b=(b_x,b_y)$, their **dot product** is the number

$$\mathbf a\cdot\mathbf b=a_xb_x+a_yb_y.$$

Multiply matching components, then add. Geometrically, the same quantity is the length of $\mathbf a$ times the length of $\mathbf b$ times the cosine of the angle between them. For nonzero vectors, a zero dot product therefore means they are perpendicular. This is called **orthogonal**.

**Worked micro-example.** Take $\mathbf a=(2,0)$ and $\mathbf b=(0,3)$:

$$\mathbf a\cdot\mathbf b=2(0)+0(3)=0.$$

They are orthogonal even though their lengths are 2 and 3. They reconstruct our earlier vector as

$$ (3,2)=\frac32\mathbf a+\frac23\mathbf b.$$

Multiplying $\mathbf a$ by another nonzero number changes its length but not its perpendicular relationship to $\mathbf b$. So zero mutual overlap does not fix the length of either object.

This reconstructs the first step behind the earlier question **“orthogonal versus orthonormal?”** The overlap calculation compared **two different vectors**. It has not yet checked the length of **either vector itself**.

### 3. Orthonormal: check each object against itself

A vector's **norm**, written $\|\mathbf a\|$, is its length. Its squared norm is its dot product with itself:

$$\|\mathbf a\|^2=\mathbf a\cdot\mathbf a.$$

For $\mathbf a=(2,0)$, this gives $\|\mathbf a\|^2=4$ and $\|\mathbf a\|=2$. To **normalize** a nonzero vector, divide by its norm:

$$\mathbf u=\frac{\mathbf a}{\|\mathbf a\|}=(1,0).$$

Dividing by the norm changes the scale so that $\mathbf u\cdot\mathbf u=1$. It does not change the direction. Dividing by the *squared* norm would generally give the wrong length. The zero vector cannot be normalized.

A set is **orthonormal** when different members have zero overlap and each member has norm one. For our example, normalizing $\mathbf a$ and $\mathbf b$ gives $\mathbf e_x$ and $\mathbf e_y$.

The **Kronecker delta**, $\delta_{mn}$, abbreviates two cases: it equals 1 when the labels $m,n$ match and 0 when they differ. Subscripts $m,n$ here label members of a set. If $\mathbf e_m$ are orthonormal, we can write both conditions in one equation:

$$\mathbf e_m\cdot\mathbf e_n=\delta_{mn}.$$

Read its equal-label case as “unit squared length” and its unequal-label case as “zero overlap.”

> **Self-check:** If we double every member of an orthonormal set, what happens to orthogonality and to each squared norm?

<details>
<summary>Check your reasoning</summary>

The overlap of two different members remains zero. Each squared norm becomes 4, so the set is still orthogonal but no longer orthonormal. The available directions and their span have not changed.

</details>

### 4. A function can also be a building block

A function gives one value for each input. Imagine first recording its values at just three points. Those three numbers form a list, much like vector components. To compare two such lists, we multiply values at matching points and add.

For continuous functions, an integral takes the place of that sum. We call this generalized dot product an **inner product**, written $\langle f,g\rangle$. The brackets mean “compute the overlap using the specified rule”; they do not mean multiply the names $f$ and $g$.

Before writing the general rule, identify its ingredients:

| Notation | Meaning |
| --- | --- |
| $D$ | The domain over which we compare functions, such as an interval |
| $x$, $dx$ | The input coordinate and a small interval element in the integral |
| $f(x),g(x)$ | The values of the two functions at the same input |
| $f^*(x)$ | Complex conjugate: replace $i$ by $-i$; for real functions it equals $f(x)$ |
| $w(x)$ | A positive weight specifying how locations contribute; often simply 1 |

The rule is

$$\langle f,g\rangle=\int_D f^*(x)g(x)w(x)\,dx.$$

Term by term: compare values at the same location through $f^*g$, weight that comparison by $w$, then add it over the whole domain through the integral. We conjugate the first function so that its overlap with itself contains $f^*f=|f|^2$, the nonnegative squared magnitude. For example $(1-i)(1+i)=2$, whereas $(1+i)^2=2i$ would not serve as a positive squared length.

This is the bridge from arrows to functions. The word **mode** in this context means a chosen function used as one of the building blocks. It need not describe a vibration unless the physical problem gives it that meaning.

**Worked micro-example.** Use real, dimensionless functions $f(x)=1$ and $g(x)=x$ on $[-1,1]$, with weight 1:

$$\langle f,g\rangle=\int_{-1}^{1}x\,dx
=\left[\frac{x^2}{2}\right]_{-1}^{1}=\frac12-\frac12=0.$$

Their overlap is zero. Yet neither function is absent from half the interval: the positive and negative contributions cancel. For functions, **orthogonal does not mean their graphs never cross or never occupy the same region**. It means this particular inner product vanishes.

Check the squared norms separately:

$$\|f\|^2=\int_{-1}^{1}1\,dx=2,\qquad
\|g\|^2=\int_{-1}^{1}x^2\,dx=\frac23.$$

Thus the normalized versions are $1/\sqrt2$ and $\sqrt{3/2}\,x$. This is the same divide-by-length operation as for arrows, using the function norm instead of ordinary spatial length.

**Why the domain matters.** The same functions on $[0,1]$ have overlap $\int_0^1x\,dx=1/2$, which is nonzero. “These functions are orthogonal” is incomplete information unless the domain and inner product are understood. The examples here prepare the language of [[Basic Legendre polynomials]]; they are not a proof of the homework's spherical-harmonic result.

### 5. Why orthogonality lets us extract a coefficient

Return to the idea of reconstructing a target by adding building blocks. Call the target function $h$ and the available functions $f_n$. A subscript $n$ is a label, not a power. Suppose for now the target is exactly a **finite** sum:

$$h=\sum_n a_nf_n.$$

The symbol $\sum_n$ means add the listed terms; $a_n$ tells us how much of $f_n$ is present. Let $N_n=\langle f_n,f_n\rangle$ be its squared norm. For nonzero mutually orthogonal functions,

$$\langle f_m,f_n\rangle=N_n\delta_{mn}.$$

This says two things: if the labels differ, the overlap is zero; if they match, it is the squared norm of that function. The $N_n$ is not the norm itself. If all $N_n=1$, the set is orthonormal.

Now compare the target with one selected member, $f_m$:

$$\langle f_m,h\rangle
=\sum_n a_n\langle f_m,f_n\rangle
=a_mN_m.$$

The first equality distributes the inner product across the sum. In the second, every term with $n\ne m$ is zero. Only the matching term survives. Therefore

$$a_m=\frac{\langle f_m,h\rangle}{N_m}.$$

The numerator measures overlap with the chosen shape; the denominator corrects for that shape's scale. For an orthonormal set the denominator is 1. The compact reference below calls the target $f$ rather than $h$; it is the same rule.

**Worked micro-example.** On $[-1,1]$ with weight 1, reconstruct $h(x)=3+2x$ using $f_0=1$ and $f_1=x$:

$$\langle f_0,h\rangle=\int_{-1}^{1}(3+2x)\,dx=6,
\qquad a_0=6/2=3,$$
$$\langle f_1,h\rangle=\int_{-1}^{1}(3x+2x^2)\,dx=\frac43,
\qquad a_1=\frac{4/3}{2/3}=2.$$

We recover the original coefficients. If we forgot the squared-norm denominators, the raw overlaps 6 and $4/3$ would be mistaken for the coefficients.

**Boundary of this argument:** We assumed the finite expansion exists. The projection calculation does not prove that these building blocks can represent every possible target. If the target lies outside their span, the same coefficients give its orthogonal projection onto that span, with a leftover difference called the residual. Infinite expansions require an appropriate convergence condition as well.

### 6. Complete: are any directions or shapes missing?

**Intuition:** A set may contain beautifully separated and normalized building blocks while still missing something necessary.

Consider $(1,0,0)$ and $(0,1,0)$. They are orthonormal in ordinary three-dimensional space, written $\mathbb R^3$. Every linear combination has the form $(a,b,0)$, so none can equal $(0,0,1)$. The set is incomplete in $\mathbb R^3$, but complete in the $xy$ plane.

A function example makes the same distinction. The two functions $1,x$ can represent every function of the form $a+bx$. They cannot represent $x^2$ on the whole interval $[-1,1]$. To see this without advanced theory, suppose $a+bx=x^2$ for every $x$. At $x=0$ we need $a=0$; at $x=1$ we then need $b=1$; but at $x=-1$ that choice gives $-1$ instead of $+1$. The proposed equality fails.

This set is complete in the two-dimensional space of linear polynomials. It is not complete in a space that also includes arbitrary quadratic or more general functions. Normalizing $1$ and $x$ cannot fix that missing shape.

**Formal statement for function spaces:** Completeness means the span can approximate every member of the specified space arbitrarily well in the specified norm. For infinitely many building blocks, we allow progressively longer finite sums rather than demanding every target equal a short sum.

The notation $L^2$ in the reference means square-integrable functions: their integrated squared magnitude is finite. With our weight, the squared error between a target $h$ and an approximation $h_N$ is

$$\|h-h_N\|^2=\int_D|h(x)-h_N(x)|^2w(x)\,dx.$$

Here $h_N$ denotes an approximation using finitely many modes; its subscript is a truncation label, distinct from the squared norms $N_n$ used earlier. The absolute-value bars give the magnitude of the difference; squaring prevents positive and negative errors from cancelling. Convergence in this norm means this integrated squared error tends to zero as the approximation is refined. It does not automatically promise equality at every individual point. In $L^2$, functions differing only on a set of zero measure are treated as the same element.

You do not need a completeness proof yet. The immediate skill is to separate **“I can extract coefficients”** from **“I have enough modes to reconstruct every allowed target.”**

> **Self-check:** If a set is orthonormal, does that settle whether it is complete? If a target lies outside a finite orthogonal span, can its projection coefficients still be unique?

<details>
<summary>Check your reasoning</summary>

Orthonormality settles overlaps and lengths, not completeness. The projection coefficients onto a nonzero orthogonal set are still uniquely determined, but their sum leaves a residual for a target outside the span. Unique coefficients do not guarantee exact reconstruction.

</details>

### 7. Reassemble the earlier questions and the downstream use

The earlier questions about orthogonality, normalization, completeness and uniqueness become easier when kept in this order:

1. **“Do different members overlap?”** Compute their inner product. Zero gives orthogonality.
2. **“But is each member length one?”** Compute its self-inner-product. A value of 1 gives unit norm; together with the first condition, this gives orthonormality.
3. **“Then can I reconstruct anything?”** Specify the target space and test completeness. Neither of the first two checks answers this.
4. **“What exactly is unique?”** For a nonzero orthogonal set, coefficients of an existing norm-convergent expansion are fixed by projection. That is not a proof that every target has such an expansion.

For the earlier sine-only/cosine-only question in [[Homework/HW0 Map#Problem 1c|HW0 1(c)]], this suggests what to establish before judging a family: its interval, allowed frequencies, constant mode, inner product and meaning of approximation. The names “sine” or “cosine” alone do not settle completeness. A differently scaled half-range family is not automatically the same family as integer-frequency modes over a full period. This note identifies the questions rather than resolving the assignment's six comparisons.

For [[Rank-2 tensors and outer products]], the immediate connection is an orthonormal Cartesian basis. If $\mathbf a=\sum_m a_m\mathbf e_m$ and $\mathbf b=\sum_n b_n\mathbf e_n$, then

$$\mathbf a\cdot\mathbf b
=\sum_{m,n}a_mb_n(\mathbf e_m\cdot\mathbf e_n)
=\sum_m a_mb_m.$$

The delta rule removed all unequal-index pairs. This explains why ordinary Cartesian dot products are sums of matching component products. In a non-orthonormal basis, the basis overlaps must be retained. HW0's indefinite spacetime metric is a separate extension; the positive-length intuition used here must not be transferred to it unchanged.

For [[Basic Legendre polynomials]] and [[Spherical harmonics]], the same inner-product logic applies to function shapes with the correct interval or angular measure. A spherical integral has an area measure rather than the simple $dx$ used in this example. We will use those notes to specify that measure and the mode labels.

The following compact sections preserve the original reference and source locations. The teaching examples above are explanatory bridges, not claims of additional lecture coverage or completed homework proofs.

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

## Before moving on, I should be able to…

- Explain orthogonality using two different members and normalization using one member's self-inner-product.
- Normalize a nonzero vector or function by dividing by its norm, not its squared norm.
- State the domain and inner product before claiming functions are orthogonal; explain why complex conjugation appears.
- Recover a coefficient using overlap divided by squared norm, and explain why other orthogonal terms disappear.
- Give an orthonormal-but-incomplete example and distinguish unique projection coefficients from exact reconstruction.
- Explain how an orthonormal basis reduces a vector dot product to matching-component products, ready for [[Rank-2 tensors and outer products]].

These are readiness targets for the linked notes, not a claim that a completeness proof or the HW0 problems have been finished.

## Later review

| Property | Test or question | What it does not establish |
| --- | --- | --- |
| Orthogonal | Different members have zero inner product | Unit norm or completeness |
| Orthonormal | Orthogonal, with each self-inner-product equal to 1 | Completeness |
| Complete | Can the span approximate every target in the specified space and norm? | Orthogonality or good accuracy with a small truncation |
| Unique coefficients | Projection fixes each coefficient for a nonzero orthogonal set | That the residual vanishes |

For functions, fix the domain, measure/weight and allowed family first. Use $N_n=\langle f_n,f_n\rangle$ and $a_n=\langle f_n,h\rangle/N_n$. Normalize by $\sqrt{N_n}$. Remember $1$ and $x$ on $[-1,1]$: zero mutual overlap, squared norms $2$ and $2/3$, sufficient for linear polynomials but insufficient for $x^2$.
