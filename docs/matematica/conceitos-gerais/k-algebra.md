**Resumo (explicação simples)**
Uma **$K$–álgebra** é simultaneamente um **espaço vetorial** sobre um corpo $K$ e um **anel**, em que a multiplicação interna é **bilinear** em relação à multiplicação escalar. Em particular, todo produto de vetores com escalares pode “passar” entre as operações.

---

## Definição Formal

Seja $K$ um corpo. Uma **$K$–álgebra** é uma quádrupla

$$
\bigl(E,\; +,\;\cdot,\;\otimes\bigr)
$$

onde

* $\displaystyle + : E\times E\to E$ é a adição em $E$,
* $\displaystyle \cdot : E\times E\to E$ é a multiplicação interna em $E$,
* $\displaystyle \otimes : K\times E\to E$ é a multiplicação escalar,
  de modo que valem os seguintes axiomas:

1. **Grupo abeliano aditivo**

   $$
   \begin{aligned}
     &\forall\,x,y,z\in E,\quad (x + y) + z \;=\; x +(y + z),\\
     &\exists\,0_E\in E\;\bigl(\forall x\in E,\;x + 0_E = 0_E + x = x\bigr),\\
     &\forall x\in E,\;\exists(-x)\in E\;\bigl(x +(-x)=0_E\bigr),\\
     &\forall x,y\in E,\quad x + y = y + x.
   \end{aligned}
   $$

2. **Espaço vetorial sobre $K$**
   Para todo $\lambda,\mu\in K$ e $x,y\in E$:

   $$
   \begin{aligned}
     &(\lambda + \mu)\otimes x \;=\; (\lambda\otimes x)\; +\;(\mu\otimes x),\\
     &\lambda\otimes(x + y)\;=\;(\lambda\otimes x)\; +\;(\lambda\otimes y),\\
     &(\lambda\mu)\otimes x \;=\; \lambda\otimes(\mu\otimes x),\\
     &1_K\otimes x \;=\; x.
   \end{aligned}
   $$

3. **Semigrupo multiplicativo**

   $$
   \forall\,x,y,z\in E,\quad (x\cdot y)\cdot z \;=\; x\cdot(y\cdot z).
   $$

4. **Anel (distributividade)**

   $$
   \begin{aligned}
     &x\cdot(y + z) \;=\; (x\cdot y)\; +\;(x\cdot z),\\
     &(x + y)\cdot z \;=\; (x\cdot z)\; +\;(y\cdot z).
   \end{aligned}
   $$

5. **Bilinearidade da multiplicação interna**

   $$
   \forall\,\lambda\in K,\;x,y\in E,\quad
   (\lambda\otimes x)\cdot y = \lambda\otimes(x\cdot y)
   = x\cdot(\lambda\otimes y).
   $$

> **Observações adicionais**
>
> * Se existir $1_E\in E$ tal que $1_E\cdot x = x\cdot1_E = x$ para todo $x$, dizemos que a álgebra é **unitária**.
> * Se $\cdot$ for comutativa ($x\cdot y = y\cdot x$), temos uma **álgebra comutativa**.

---

## Exemplos

1. **Álgebra de matrizes**
   $\;M_n(K)$ com

   $$
      + = \text{soma de matrizes},\quad
     \cdot = \text{produto usual},\quad
     \lambda\otimes A = \lambda A.
   $$

2. **Álgebra de polinômios**
   $\;K[x]$ com

   $$
      +,\;\cdot\text{ como em }K[x],\quad
     \lambda\otimes f(x) = \sum_i (\lambda\,a_i)x^i.
   $$

3. **Álgebra de endomorfismos**
   Se $V$ é espaço vetorial sobre $K$, então
   $\mathrm{End}_K(V)$ (funções lineares $V\to V$) é uma $K$–álgebra com
   $ +$ e $\cdot$ (composição) usuais, e $\lambda\otimes T$ definido por $(\lambda\otimes T)(v)=\lambda\,T(v)$.
