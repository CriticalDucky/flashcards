---
deck: Linear Algebra
tags: [math, linear-algebra, 18.06]
---

### Card
Q: State the **rank–nullity theorem**.

A:
For $A \in \mathbb{R}^{m \times n}$,
$$\operatorname{rank}(A) + \operatorname{nullity}(A) = n.$$

---

### Card
Q: When is a square matrix $A$ invertible?

A:
Any one of these conditions implies all others:

- $\det(A) \neq 0$
- $\operatorname{rank}(A) = n$
- $Ax = 0$ has only $x = 0$
- Columns of $A$ are linearly independent

---

### Card
Q: Define an **orthogonal matrix**.

A:
A square matrix $Q$ such that
$$Q^T Q = Q Q^T = I \implies Q^{-1} = Q^T.$$
Its columns form an *orthonormal* basis for $\mathbb{R}^n$.

---

### Card
Q: State the **Cauchy–Schwarz inequality**.

A:
$$|\mathbf{u} \cdot \mathbf{v}| \leq \|\mathbf{u}\|\,\|\mathbf{v}\|,$$
with equality iff $\mathbf{u} \parallel \mathbf{v}$.

---

### Card
Q: State the **spectral theorem** for real symmetric matrices.

A:
Every real symmetric $A = A^T$ decomposes as
$$A = Q \Lambda Q^T,$$
where $Q$ is orthogonal and $\Lambda = \operatorname{diag}(\lambda_1, \ldots, \lambda_n)$ contains the real eigenvalues.

---

### Card
Q: What is **positive definiteness**?

A:
$A$ is positive definite if
$$\mathbf{x}^T A \mathbf{x} > 0 \quad \forall\, \mathbf{x} \neq \mathbf{0}.$$

Equivalent tests: all eigenvalues $> 0$, or all leading principal minors $> 0$ (Sylvester's criterion).

---

### Card
Q: Define the **four fundamental subspaces** of $A \in \mathbb{R}^{m \times n}$.

A:

| Subspace | Lives in |
|---|---|
| Column space $C(A)$ | $\mathbb{R}^m$ |
| Null space $N(A)$ | $\mathbb{R}^n$ |
| Row space $C(A^T)$ | $\mathbb{R}^n$ |
| Left null space $N(A^T)$ | $\mathbb{R}^m$ |

$C(A) \perp N(A^T)$ and $C(A^T) \perp N(A)$.

---

### Card
Q: What is an **eigenvalue decomposition**?

A:
If $A$ has $n$ linearly independent eigenvectors,
$$A = S \Lambda S^{-1},$$
where columns of $S$ are eigenvectors and $\Lambda = \operatorname{diag}(\lambda_i)$.
