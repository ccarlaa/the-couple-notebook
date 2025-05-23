# Projeção

Uma **projeção** em Álgebra Linear é um operador linear que “projeta” vetores de um espaço $V$ sobre um subespaço $W\subseteq V$, deixando intacta a componente em $W$ e anulando a componente em um complemento.

---

## 1. Projeção Linear Geral

Seja $(V,K,+,\cdot)$ um espaço vetorial e $P\colon V\to V$ uma aplicação linear. Dizemos que $P$ é uma **projeção** se, e somente se,

$$
P^2 = P,
$$

isto é,

$$
\forall v\in V,\quad P\bigl(P(v)\bigr) = P(v).
$$

**Propriedades equivalentes**:

- $\operatorname{Im}(P)$ (imagem de $P$) e $\ker(P)$ (núcleo de $P$) satisfazem
  $$
    V = \operatorname{Im}(P)\;\oplus\;\ker(P).
  $$
- Para todo $v\in V$, escrevemos unicamente

  $$
    v = w + u,
    \quad
    w\in \operatorname{Im}(P),\;
    u\in \ker(P),
  $$

  e então

  $$
    P(v) = w.
  $$

### 1.1. Tipos de projeções lineares

* **Projeção sobre $W$ ao longo de $U$**:
  Se $V = W \oplus U$, define-se

  $$
    P_{W,U}\colon V\to V,
    \quad
    P_{W,U}(w+u) = w,
    \quad w\in W,\;u\in U.
  $$

  Então $P_{W,U}^2 = P_{W,U}$, $\operatorname{Im}(P_{W,U}) = W$, $\ker(P_{W,U}) = U$.

---

## 2. Projeção Ortogonal em Espaço com Produto Interno

Se $V$ é um espaço vetorial sobre $K$ dotado de um **produto interno** $\langle\cdot,\cdot\rangle$, e $W\subseteq V$ é um subespaço (finito gerado), a **projeção ortogonal** de $v\in V$ sobre $W$ é o vetor $P_W(v)\in W$ tal que

1. $v - P_W(v)$ pertence ao **ortogonal** $W^\perp$, i.e.
   $\langle v - P_W(v), w\rangle = 0$ para todo $w\in W$.

2. $P_W$ é a projeção linear cujo núcleo é $W^\perp$ e imagem é $W$.

### 2.1. Fórmula em base ortonormal

Se $\{e_1,\dots,e_k\}$ é uma base **ortonormal** de $W$, então para todo $v\in V$:

$$
P_W(v)
= \sum_{i=1}^{k} \langle v,\,e_i\rangle\,e_i.
$$

Nesse caso, $P_W$ satisfaz $P_W^2 = P_W$ e é **autoadjunto** ($P_W = P_W^*$).

---

## 3. Exemplos

1. **Projeção sobre o eixo $x$ em $\mathbb{R}^2$**:

   $$
     P(x,y) = (x,0).
   $$

   Aqui $W = \operatorname{span}\{(1,0)\}$, $U = \operatorname{span}\{(0,1)\}$.

2. **Projeção ortogonal em $\mathbb{R}^3$ no plano $xy$**:
   Com base ortonormal $\{e_1=(1,0,0),e_2=(0,1,0)\}$:

   $$
     P_{xy}(x,y,z) = \langle (x,y,z),e_1\rangle e_1 + \langle (x,y,z),e_2\rangle e_2 = (x,y,0).
   $$

3. **Matriz de projeção**
   Se $P$ é projeção sobre o subespaço gerado pelas colunas de $A\in M_{n\times k}(K)$ com colunas linearmente independentes, então

   $$
     P = A\,(A^TA)^{-1}A^T
     \quad (\text{em }K=\mathbb{R},\text{ produto interno usual}).
   $$
