# Rank-2 tensors and outer products

## One-sentence meaning

A rank-2 Cartesian tensor describes a relation with two directional slots, such as an input direction and an output vector component.

## Prerequisites

Vector components; dot products; [[Orthogonal, orthonormal and complete]] for orthonormal Cartesian bases.

## Core equations

$$(\mathbf a\otimes\mathbf b)_{ij}=a_ib_j,\qquad
(\mathbf a\otimes\mathbf b)\cdot\mathbf n=\mathbf a(\mathbf b\cdot\mathbf n),$$
$$T'_{ij}=R_{ik}R_{jm}T_{km},\qquad T'=RTR^{\mathsf T},\qquad R^{\mathsf T}R=I.$$
$$ (T\cdot\mathbf n)_i=\sum_jT_{ij}n_j,\qquad
T=T_{ij}\,\mathbf e_i\otimes\mathbf e_j.$$
Repeated indices are summed; a free index labels the component left over.

## Where they come from

Each vector in an outer product transforms once under rotation, so the product transforms with two rotation matrices. Linear combinations of basis outer products produce general rank-2 Cartesian tensors.

## Assumptions

These component rules use an orthonormal Cartesian basis and ordinary rotations. HW0's spacetime metric and spherical coordinate bases need separate index/metric care; a Cartesian dot-product formula cannot simply be copied to a non-unit coordinate basis.

## Physical meaning

For stress, the first slot is the force or momentum component and the second selects the surface-normal direction. Contracting with a normal produces a traction vector. A matrix represents the tensor in a basis; its transformation rule gives it geometric meaning.

## When to use it

Describe directional responses and momentum transfer across surfaces; read [[Maxwell stress tensor]]; organize the tensor decomposition in [[Homework/HW0 Map#Problem 2a|HW0 2(a)]].

## Example

Take $\mathbf a=\hat{\mathbf x}$ and $\mathbf b=\hat{\mathbf y}$. The tensor has only $T_{xy}=1$. It maps $\hat{\mathbf y}$ to $\hat{\mathbf x}$ and maps $\hat{\mathbf x}$ to zero. Reversing the outer product changes the result.

## Common confusion

**Earlier thought: is the Maxwell stress tensor needed because $E$ and $B$ spiral or propagate?** No. Momentum has a component direction, and transport has an independent surface-normal direction. Those two directional slots require rank 2, including for static fields.

**Does rank 2 mean matrix rank 2?** No: tensor rank here counts indices. An outer product is a rank-2 tensor even though its matrix has linear-algebra rank 1 when both vectors are nonzero.

**Does divergence leave two indices?** No. $(\nabla\cdot T)_i=\partial_jT_{ij}$ contracts the spatial derivative with one slot and leaves a vector.

## Related concepts

[[Maxwell stress tensor]]; [[Vector fields, divergence and curl]]; [[Orthogonal, orthonormal and complete]].

## Used in

[[Sources/Course Sources#Lecture 1|Lecture 1]] §1.7, eqs. (43)–(58). [[Homework/HW0 Map#Problem 2a|HW0 2(a)]] and [[Homework/HW0 Map#Problem 3|3]]; [[Homework/HW1 Map#Problem 3|HW1 3]].
