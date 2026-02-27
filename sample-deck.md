---
deck: Linear Algebra · 18.06
tags: [math, linear-algebra, sample]
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
Equivalent conditions (any one implies all):

- $\det(A) \neq 0$
- $\operatorname{rank}(A) = n$
- $Ax = 0$ has only the trivial solution
- The columns of $A$ are linearly independent

---

### Card
Q: Define an **orthogonal matrix**.

A:
A square matrix $Q$ such that $Q^T Q = Q Q^T = I$, i.e. $Q^{-1} = Q^T$.

Its columns form an *orthonormal* basis for $\mathbb{R}^n$.

---

### Card
Q: State the **Cauchy–Schwarz inequality**.

A:
For vectors $\mathbf{u}, \mathbf{v} \in \mathbb{R}^n$,
$$|\mathbf{u} \cdot \mathbf{v}| \leq \|\mathbf{u}\| \cdot \|\mathbf{v}\|,$$
with equality iff $\mathbf{u}$ and $\mathbf{v}$ are parallel.

---

### Card
Q: What is the **spectral theorem** (for real symmetric matrices)?

A:
Every real symmetric matrix $A = A^T$ can be diagonalized as
$$A = Q \Lambda Q^T,$$
where $Q$ is orthogonal and $\Lambda = \operatorname{diag}(\lambda_1, \ldots, \lambda_n)$ contains the real eigenvalues.

---

### Card
Q: What does it mean for a matrix to be **positive definite**?

A:
A symmetric matrix $A$ is **positive definite** if
$$\mathbf{x}^T A \mathbf{x} > 0 \quad \forall\, \mathbf{x} \neq \mathbf{0}.$$

Equivalent tests: all eigenvalues $> 0$, or all leading principal minors $> 0$ (Sylvester's criterion).
