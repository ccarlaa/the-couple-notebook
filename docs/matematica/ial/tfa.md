# Teorema Fundamental da Álgebra

O **Teorema Fundamental da Álgebra** afirma que todo polinômio não-constante de grau $n$ com coeficientes complexos tem exatamente $n$ raízes complexas não necessáriamente distintas. Em outras palavras, o campo $\mathbb{C}$ é **algebricamente fechado**: todo polinômio sobre $\mathbb{C}$ se fatoriza completamente em fatores lineares.


---

## 1. Enunciado Formal

Seja $p(z)$ um polinômio de grau $n \geq 1$ com coeficientes complexos:

$$
p(z) = a_n z^n + a_{n-1} z^{n-1} + \cdots + a_1 z + a_0,\quad \text{com } a_n \neq 0.
$$

Então, existem números complexos $\lambda_1, \lambda_2, \dots, \lambda_n$ (não necessariamente distintos) tais que:

$$
p(z) = a_n (z - \lambda_1)(z - \lambda_2) \cdots (z - \lambda_n) \quad \text{e} \quad \forall k \in \mathbb{N}^+, k\le n, \quad p(\lambda_k) = 0
$$

### Em notação Simbólica

Seja $f(x) = \sum_{i=0}^n a_i x^i$ uma **função polinomial**:

$$
\forall n\in\mathbb{N},\,n\ge 1,\;\forall f(z) \in\mathbb{C}[z],\; a_n\neq0,\;\exists (\lambda_1,\dots,\lambda_n)\in\mathbb{C}^n:
$$

$$
\quad \forall k \in \mathbb{N}^+,\; k\le n,\; f(\lambda_k) = 0 \quad
\wedge \quad
f(z) = \sum_{k=0}^n a_k\,z^k \;=\; a_n\;\prod_{i=1}^n (z-\lambda_i).
$$

## Propriedades

Ou seja, o TFA afirma sobre:

1. **Existência de raiz**
   $$
   \exists\,\alpha\in\mathbb{C}\quad\text{tal que}\quad f(\alpha)=0.
   $$

2. **Fatoração completa**
   Mais ainda, podemos escrever

   $$
   f(x) \;=\; a_n\prod_{k=1}^{n}(x - \alpha_k),
   $$

   onde $\alpha_1,\dots,\alpha_n\in\mathbb{C}$ são todas as raízes de $f$ (com suas multiplicidades).


