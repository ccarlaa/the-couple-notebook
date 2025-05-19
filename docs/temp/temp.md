**Resumo (explicação simples)**

* **Conjuntos** são coleções bem definidas de objetos (chamados *elementos*). Ex.: o conjunto dos números inteiros, o conjunto das cores primárias.
* **Lógica** é o estudo de proposições (sentenças que podem ser verdadeiras ou falsas) e das regras que permitem formar argumentos válidos. Ex.: “Se chove, então a rua fica molhada”; “Não (P e Q) é equivalente a (¬P) ou (¬Q)”.

---

## 1. Teoria de Conjuntos (ZF)

**Linguagem**:

* Símbolo único de predicado binário:

  $$
    L_{\in} = \{\;\in\;\}.
  $$

**Termos**:

$$
  t ::= x \quad(x\text{ variável}).
$$

**Fórmulas** (indutivamente):

* $t_1 \in t_2$ e $t_1 = t_2$ são fórmulas atômicas;
* Se $\varphi,\psi$ são fórmulas, então
  $\neg\varphi,\;(\varphi\land\psi),\;(\varphi\lor\psi),\;(\varphi\to\psi)$ são fórmulas;
* Se $\varphi$ é fórmula e $x$ variável, então $\forall x\,\varphi$ e $\exists x\,\varphi$ são fórmulas.

**Axiomas de Zermelo–Fraenkel**

1. **Extensionalidade**

   $$
     \forall A\;\forall B\;\bigl(\forall x\,(x\in A\leftrightarrow x\in B)\;\to\;A=B\bigr).
   $$
2. **Esquema de Compreensão Restrita**
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
9. **Escolha (AC)** *(opcional)*

   $$
     \forall A\bigl(\varnothing\notin A\to\exists f:A\to\bigcup A\;\land\;\forall X\in A\,(f(X)\in X)\bigr).
   $$

---

## 2. Lógica de Primeira Ordem

**Linguagem**

$$
  L = \bigl(\mathcal V,\;\mathcal F,\;\mathcal P,\;=\bigr)
$$

* $\mathcal V$: conjunto infinito de variáveis $x,y,z,\dots$.
* $\mathcal F$: símbolos de função de vários aridades.
* $\mathcal P$: símbolos de predicado de vários aridades.
* “$=$” é símbolo de igualdade (predicado binário especial).

**Termos**

$$
  t ::= x\mid f(t_1,\dots,t_n)\quad(f\in\mathcal F,\;n\ge1).
$$

**Fórmulas**

* $P(t_1,\dots,t_n)$ e $t_1 = t_2$ são atômicas;
* Fecham-se sob $\neg,\land,\lor,\to$;
* Fecham-se sob quantificadores $\forall x,\;\exists x$.

**Estrutura (Interpretação)**

$$
  \mathcal M = \bigl(D,\;I\bigr),
$$

onde

* $D$ é o domínio não vazio;
* $I$ mapeia cada $n$-símbolo de função $f\mapsto f^{\mathcal M}:D^n\to D$ e cada $n$-símbolo de predicado $P\mapsto P^{\mathcal M}\subseteq D^n$.

**Satisfação**
Para atribuição $v:\mathcal V\to D$, define-se recursivamente quando
$\mathcal M\vDash\varphi[v]$ (“$\varphi$ é verdadeira em $\mathcal M$ sob $v$”), conforme a semântica usual.

---

## Exemplos

1. **Conjuntos**

   $$
     A = \{1,2,3\},\quad B=\{2,3,4\}.
   $$

   $$
     A\cap B = \{\,x\mid x\in A\land x\in B\} = \{2,3\},
     \quad
     A\cup B = \{1,2,3,4\}.
   $$

2. **Fórmulas Lógicas**

   * $\forall x\,(P(x)\to Q(x))$: “Para todo $x$, se $P(x)$ então $Q(x)$”.
   * $\exists y\,P(y)\land\neg Q(y)$: “Existe $y$ tal que $P(y)$ e não $Q(y)$”.

3. **Exemplo em Teoria de Conjuntos**
   Axioma do Par aplicado a $\{a\}$ e $\{b\}$:

   $$
     \exists C\;\forall x\;(x\in C\leftrightarrow x=\{a\}\lor x=\{b\}),
   $$

   ou seja, $C = \bigl\{\{a\},\{b\}\bigr\}$.
