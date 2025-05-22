# Anel

Um **anel** é uma coleção de elementos onde se pode somar, subtrair e multiplicar, obedecendo regras que generalizam as operações usuais em ℤ. Ele serve de estrutura básica em muitas áreas da Álgebra, como números inteiros, matrizes e polinômios.

---

## 1. Definição
Um **anel** é uma tripla $(R, +, \cdot)$ tal que satisfaz os seguintes axiomas:

## 2. Axiomas
### **Axiomas do grupo aditivo**

   $$
   (R, +)\text{ é um grupo abeliano.}
   $$

   Ou seja, para todos $a,b,c \in R$:

   1. (Fechamento) $\;a + b \in R$.
   2. (Associatividade) $\;(a + b) + c = a + (b + c).$
   3. (Existência do neutro aditivo) $\;\exists\,0\in R$ tal que $a + 0 = a = 0 + a.$
   4. (Existência de inverso aditivo) $\;\forall a\in R,\;\exists(-a)\in R$ tal que $a + (-a) = 0 = (-a) + a.$
   5. (Comutatividade) $\;a + b = b + a.$

### **Axiomas do semigrupo multiplicativo**

   $$
   (R, \cdot)\text{ é um semigrupo associativo.}
   $$

   Isto é, para todos $a,b,c \in R$:

   1. (Fechamento) $\;a\cdot b \in R.$
   2. (Associatividade) $\;(a\cdot b)\cdot c = a\cdot (b\cdot c).$

### **Distributividade**
   Para todos $a,b,c \in R$ valem

   $$
   a\cdot (b + c) \;=\; a\cdot b \;+\; a\cdot c,
   \qquad
   (a + b)\cdot c \;=\; a\cdot c \;+\; b\cdot c.
   $$

---

---

## Exemplos

1. **Inteiros**
   $\bigl(\mathbb{Z},+,\times\bigr)$ é um anel comutativo unitário (unidade $1$).

2. **Matrizes quadradas**
   O conjunto $M_n(\mathbb{R})$ de todas as matrizes $n\times n$ com entradas reais, com soma e produto usuais, é um anel não comutativo, mas unitário (unidade $I_n$).

3. **Polinômios**
   $\mathbb{R}[x]$, o conjunto de polinômios em $x$ com coeficientes reais, forma um anel comutativo unitário.

4. **Funções**
   Se $X$ é um conjunto, as funções $f\colon X\to\mathbb{R}$ com soma e produto ponto a ponto formam um anel comutativo unitário (unidade: função constante $1$).
