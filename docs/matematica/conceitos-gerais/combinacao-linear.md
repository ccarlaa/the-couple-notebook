# Combinação Linear

 Uma **combinação linear** de vetores é uma expressão do tipo

  $$
  \lambda_1 v_1 + \lambda_2 v_2 + \dots + \lambda_n v_n,
  $$

  onde os $\lambda_i$ são escalares e os $v_i$ são vetores.

---

## 1. Definição Formal

Seja $(V, K, +, \cdot)$ um espaço vetorial sobre um corpo $K$. Se $v_1, \dots, v_n \in V$ e $\lambda_1, \dots, \lambda_n \in K$, então o vetor

$$
v := \lambda_1 v_1 + \lambda_2 v_2 + \dots + \lambda_n v_n
$$

é chamado de **Combinação Linear** de $v_1,\dots,v_n$ com coeficientes $\lambda_1,\dots,\lambda_n$.

Denotamos o **conjunto de todas as combinações lineares** de $v_1,\dots,v_n$ por:

$$
\operatorname{span}\{v_1, \dots, v_n\}
:= \left\{ \sum_{i=1}^{n} \lambda_i v_i \;\middle|\; \lambda_i \in K \right\}.
$$

Também chamado de **Subespaço Gerado**.

---

## 2. Dependência Linear

O conjunto de vetores $\{v_1, \dots, v_n\} \subseteq V$ é dito **linearmente dependente** se:

$$
\exists\, \lambda_1, \dots, \lambda_n \in \mathbb{K} \;,\; \big(\lambda_1, \dots, \lambda_n\big) \ne \mathbf{0} \;:\; 
\sum_{i=1}^n \lambda_i v_i = \mathbf{0}_V
$$
Ou seja, existe uma **combinação linear não trivial** que resulta no vetor nulo.

Se **não** existir tal combinação não trivial, dizemos que o conjunto é **linearmente independente**:

$$
\{v_1, \dots, v_n\} \text{ é linearmente independente}
\quad \Longleftrightarrow \quad
\sum_{i=1}^n \lambda_i v_i = 0_V \Rightarrow \lambda_1 = \dots = \lambda_n = 0.
$$

---

## Exemplos

### Exemplo 1: Dependência

No espaço vetorial $\mathbb{R}^3$,

$$
v_1 = (1,0,0),\quad
v_2 = (0,1,0),\quad
v_3 = (1,1,0).
$$

Temos:

$$
v_3 = v_1 + v_2 \;\Rightarrow\;
\{v_1,v_2,v_3\} \text{ é linearmente dependente}.
$$

### Exemplo 2: Independência

Em $\mathbb{R}^2$,

$$
v_1 = (1,0),\quad
v_2 = (0,1)
$$

é um conjunto **linearmente independente**, pois:

$$
\lambda_1 v_1 + \lambda_2 v_2 = 0
\;\Rightarrow\;
\lambda_1 = \lambda_2 = 0.
$$

---

Se quiser, posso seguir com a definição de base, posto, ou independência infinita — tudo formalmente.
