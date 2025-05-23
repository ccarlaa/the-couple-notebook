Certainly! Here's your sentence rewritten purely in formal mathematical notation:

$$
\exists \lambda_1, \dots, \lambda_n \in \mathbb{K},\; \text{nem todos nulos},\; \text{tais que} \; \sum_{i=1}^{n} \lambda_i v_i = \mathbf{0}_V
$$

Or, more compactly and fully symbolized:

$$
\exists\, \lambda_1, \dots, \lambda_n \in \mathbb{K} \;\text{com}\; \big(\lambda_1, \dots, \lambda_n\big) \ne \mathbf{0} \;\text{tal que}\; \sum_{i=1}^n \lambda_i v_i = \mathbf{0}_V
$$

Where:

* $\mathbb{K}$ is the underlying field (e.g., $\mathbb{R}$, $\mathbb{C}$, etc.),
* $\mathbf{0}_V$ is the zero vector in the vector space $V$,
* $v_1, \dots, v_n \in V$ are given vectors.

Let me know if you also want the negation or the equivalent condition for linear **independence**.

The **Kronecker delta**, denoted $\delta_{ij}$, is a function of two variables (typically integers $i$ and $j$) that equals 1 when the indices are equal and 0 otherwise. Formally:

$$
\delta_{ij} =
\begin{cases}
1 & \text{if } i = j, \\
0 & \text{if } i \ne j.
\end{cases}
$$

---

### Properties

1. **Identity in summations**:

   $$
   \sum_j \delta_{ij} a_j = a_i
   $$

   It acts like a filter that "selects" the term where $j = i$.

2. **Matrix interpretation**:
   In linear algebra, $\delta_{ij}$ is the element of the **identity matrix** $I$, where:

   $$
   I_{ij} = \delta_{ij}
   $$

3. **Orthogonality indicator**:
   In inner product spaces, if $\langle \phi_i, \phi_j \rangle = \delta_{ij}$, then the set $\{\phi_k\}$ is an **orthonormal set**.

---

### Example

If you have a basis $\{e_1, e_2, e_3\}$ with inner product $\langle e_i, e_j \rangle = \delta_{ij}$, then:

* $\langle e_1, e_1 \rangle = 1$,
* $\langle e_1, e_2 \rangle = 0$,
* $\langle e_2, e_3 \rangle = 0$,
  and so on.

---

### Not to confuse with:

* **Dirac delta** $\delta(x)$: a generalized function or distribution used in continuous settings.
* **Heaviside function**: a step function, not related to the Kronecker delta.

Let me know if you want its generalization to tensors or its use in proofs.
