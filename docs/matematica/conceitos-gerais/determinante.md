# Determinante

O **determinante** é uma função que associa a cada matriz quadrada $A \in M_n(K)$ (com entradas em um corpo $K$) um único elemento $\det(A) \in K$. Para uma aplicação linear $T:V\to V$ em um espaço vetorial de dimensão finita $n$, o determinante de $T$ é o fator pelo qual $T$ expande (ou contrai) volumes orientados no espaço e indica se $T$ é invertível ($\det(T)\neq0$).

---

## 1. Definição Formal

Seja $K$ um corpo. A função **determinante** é a única aplicação

$$
\det : M_n(K) \to K
$$

Para toda matriz $A = [a_{ij}] \in M_n(K)$, define-se:

$$
\det(A) = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \cdot a_{1,\sigma(1)} \cdot a_{2,\sigma(2)} \cdots a_{n,\sigma(n)}
$$

onde:

* $S_n$ é o **grupo simétrico** de todas as permutações do conjunto $\{1,2,\dots,n\}$,
* $\operatorname{sgn}(\sigma) \in \{-1, +1\}$ é o **sinal da permutação**, igual a $+1$ se $\sigma$ é par (produto de número par de transposições) e $-1$ se $\sigma$ é ímpar.

E satisfaz as três propriedades axiomáticas abaixo:

## 2. Axiomas fundamentais:

1. **Multilinearidade nas linhas (ou colunas):**
   A função $\det$ é **linear em cada linha** da matriz separadamente, ou seja, para todo $1 \leq i \leq n$, se a $i$-ésima linha $L_i$ de uma matriz $A$ for escrita como
   $$
   L_i = \lambda L'_i + \mu L''_i,\quad \lambda, \mu \in K,
   $$
   então:
   $$
   \det
   \begin{bmatrix}
   L_1 \\ \vdots \\ \lambda L'_i + \mu L''_i \\ \vdots \\ L_n
   \end{bmatrix}
   =
   \lambda\cdot \det
   \begin{bmatrix}
   L_1 \\ \vdots \\ L'_i \\ \vdots \\ L_n
   \end{bmatrix}
   +
   \mu\cdot \det
   \begin{bmatrix}
   L_1 \\ \vdots \\ L''_i \\ \vdots \\ L_n
   \end{bmatrix}
   $$

2. **Alternância (troca de linhas troca o sinal):**
   Se duas linhas quaisquer de uma matriz $A$ forem iguais, então $\det(A) = 0$.
   Mais geralmente, trocar duas linhas de $A$ inverte o sinal do determinante.

3. **Normalização (determinante da identidade):**

   $$
   \det(I_n) = 1
   $$

   onde $I_n$ é a matriz identidade de ordem $n$.

---

## 3. Propriedades úteis

Se $A, B \in M_n(K)$, então:

* $\det(A^T) = \det(A)$
* $\det(AB) = \det(A)\cdot\det(B)$
* $\det(A^{-1}) = \det(A)^{-1}$, se $A$ é invertível
* $A$ é invertível ⟺ $\det(A) \ne 0$
* $\det(\lambda A) = \lambda^n \cdot \det(A)$ para $\lambda \in K$
* Se $A$ tem uma linha ou coluna igual a zero, então $\det(A) = 0$

---

## Exemplo (ordem 3):

Seja

$$
A =
\begin{bmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end{bmatrix}
$$

Então:

$$
\det(A) =
a(ei - fh) - b(di - fg) + c(dh - eg)
$$
