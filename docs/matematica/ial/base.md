# Base

## 1. Definição 

Seja $(V, K, +, \cdot)$ um espaço vetorial sobre um corpo $K$, um conjunto de vetores $B \subseteq V$ é dito uma **base** de $V$ se satisfaz as duas condições seguintes:

1. **Geração** (ou *spanning*):

$B$ gera $V$:
   $$
   \operatorname{span}(B) = V,
   \quad \text{isto é,} \quad
   \forall v \in V,\; \exists\; b_1,\dots,b_n \in B,\; \lambda_1,\dots,\lambda_n \in K
   \;\text{ tais que }\;
   v = \sum_{i=1}^{n} \lambda_i b_i.
   $$
2. **Independência linear**:

   $$
   \forall\; b_1,\dots,b_n \in B,\;
   \left(\sum_{i=1}^{n} \lambda_i b_i = 0 \Rightarrow \lambda_1 = \dots = \lambda_n = 0\right).
   $$

Portanto, uma base é um conjunto **linearmente independente** que **gera** todo o espaço vetorial.

## 2. Notação

Se $B = \{v_1,\dots,v_n\}$ é uma base de $V$, escrevemos:

$$
V = \operatorname{span}\{v_1,\dots,v_n\}
\quad \text{e} \quad
\text{os } v_i \text{ são linearmente independentes}.
$$

## 3. Consequências

* Todo vetor $v \in V$ admite **uma única** combinação linear dos elementos da base:

  $$
  v = \sum_{i=1}^{n} \lambda_i v_i
  \quad \text{com } \lambda_i \in K \text{ únicos}.
  $$

* Se $V$ admite uma base finita com $n$ elementos, diz-se que $V$ é **de dimensão finita**, e define-se:

  $$
  \dim_K V := n.
  $$

* Todas as bases de um espaço vetorial de dimensão finita têm o mesmo número de elementos.

## Base Ortogonal

Seja $V$ um **espaço vetorial com produto interno** $\langle \cdot,\cdot \rangle$ sobre um corpo $\mathbb{K} \in \{\mathbb{R},\mathbb{C}\}$.

Um subconjunto $\mathcal{B} = \{v_1, v_2, \dots, v_n\} \subseteq V$ é uma **base ortogonal** de $V$ se:

1. $\mathcal{B}$ é **linearmente independente** e **gera** $V$, ou seja:
   $$
   V = \operatorname{span}(\mathcal{B});
   $$

2. Os vetores da base são **ortogonais dois a dois**:

   $$
   \forall i \ne j,\quad \langle v_i, v_j \rangle = 0.
   $$

Se, além disso,

$$
\forall i,\quad \|v_i\| = \sqrt{\langle v_i, v_i \rangle} = 1,
$$

então $\mathcal{B}$ é uma **base ortonormal**.

---

### Observações

* Em qualquer espaço euclidiano (como $\mathbb{R}^n$ com produto interno usual), **existe uma base ortonormal** (por exemplo, via processo de Gram-Schmidt).
* Em uma base ortogonal $\mathcal{B} = \{v_1, \dots, v_n\}$, todo vetor $v \in V$ pode ser escrito como:

  $$
  v = \sum_{i=1}^n \frac{\langle v, v_i \rangle}{\langle v_i, v_i \rangle} \, v_i.
  $$

  No caso ortonormal, essa fórmula se simplifica para:

  $$
  v = \sum_{i=1}^n \langle v, v_i \rangle \, v_i.
  $$

---

### Exemplo Clássico

No espaço $\mathbb{R}^3$ com produto interno usual

$$
\langle u, v \rangle = u_1v_1 + u_2v_2 + u_3v_3,
$$

a base canônica

$$
\mathcal{B} = \{e_1 = (1,0,0),\; e_2 = (0,1,0),\; e_3 = (0,0,1)\}
$$

é uma **base ortonormal**, pois:

* $\langle e_i, e_j \rangle = 0$ se $i \ne j$,
* $\|e_i\| = 1$ para todo $i$.

---