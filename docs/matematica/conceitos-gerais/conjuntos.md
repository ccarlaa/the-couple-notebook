# Conjuntos

## **Definição**

Seja $U$ um “universo” de discurso (conjunto de referência). Um **conjunto** $A$ é determinado por uma propriedade (predicado) $P$ que seus elementos satisfazem:

$$
A \;=\; \{\,x \in U \mid P(x)\,\}.
$$

Ou, de forma abreviada, quando o universo estiver implícito,

$$
A \;=\; \{\,x \mid P(x)\,\}.
$$

---
## **Propriedades**

1. **Extensionalidade**

   $$
     \forall A\;\forall B\;\bigl(\forall x\,(x\in A\leftrightarrow x\in B)\;\to\;A=B\bigr).
   $$
2. **Esquema de Compreensão Restrita**:

   Para cada fórmula $\varphi(x)$ sem quantificar sobre o conjunto resultante,

   $$
     \forall A\;\exists B\;\forall x\;\bigl(x\in B\leftrightarrow x\in A\land\varphi(x)\bigr).
   $$
3. **Par Ordenado**

   $$
     \forall A\,\forall B\;\exists C\;\forall x\;\bigl(x\in C\leftrightarrow x=A\lor x=B\bigr).
   $$
4. **União**

   $$
     \forall A\;\exists B\;\forall x\;\bigl(x\in B\leftrightarrow\exists C\,(x\in C\land C\in A)\bigr).
   $$
5. **Conjunto das Partes**

   $$
     \forall A\;\exists B\;\forall x\;\bigl(x\in B\leftrightarrow x\subseteq A\bigr).
   $$
6. **Infinito**

   $$
     \exists I\;\bigl(\varnothing\in I\;\land\;\forall x\,(x\in I\to x\cup\{x\}\in I)\bigr).
   $$
7. **Substituição (Esquema)**
   Se $\varphi(x,y)$ define função, então

   $$
     \forall A\;\exists B\;\forall y\;\bigl(y\in B\leftrightarrow\exists x\,(x\in A\land\varphi(x,y))\bigr).
   $$
8. **Regularidade (Fundamentação)**

   $$
     \forall A\bigl(A\neq\varnothing\to\exists x\,(x\in A\land x\cap A=\varnothing)\bigr).
   $$
9. **Conjunto vazio**

Define-se o conjunto vazio como aquele que não contém elemento algum:

$$
\varnothing \;=\;\{\,x\mid x \neq x\,\}.
$$

Em particular, vale

$$
\forall x\;\bigl(x \notin \varnothing\bigr).
$$

---

**3. Operações básicas**

* **União**
  $\displaystyle X\;\cup\;Y \;=\;\{\,z\mid z\in X \;\lor\; z\in Y\,\}.$

* **Interseção**
  $\displaystyle X\;\cap\;Y \;=\;\{\,z\mid z\in X \;\land\; z\in Y\,\}.$

* **Subconjunto**
  $\displaystyle X\subseteq Y \;\iff\;\forall z\,(z\in X\implies z\in Y).$

* **Diferença**
  $\displaystyle X\setminus Y \;=\;\{\,z\mid z\in X \;\land\; z\notin Y\,\}.$

---



