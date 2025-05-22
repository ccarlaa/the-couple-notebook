# Funções Polinomiais

Uma **função polinomial** é a <u>interpretação</u> de um polinômio formal como função: ela associa valores do corpo $K$ aos seus resultados pela **substituição de $x$**. Sendo as **raizes** de uma função polinomial os valores onde a função se anula.

---

## **Definições formais**

### 1. **Função polinomial sobre um corpo $K$**

Seja $f(x) = \sum_{i=0}^n a_i x^i \in K[x]$ um **polinômio formal**.
A **função polinomial associada** é o mapeamento:

$$
\tilde{f} \colon K \to K,\quad \tilde{f}(\alpha) := \sum_{i=0}^{n} a_i \alpha^i
$$

O conjunto de todas as funções polinomiais sobre $K$ é:

$$
\mathcal{P}_K := \left\{ \tilde{f} \colon K \to K \;\middle|\; \exists f(x)\in K[x]: \tilde{f}(\alpha) = f(\alpha)\;\forall \alpha\in K \right\}
$$

**Observação importante:**

* Pode acontecer que dois polinômios formais **diferentes** definam a **mesma função** (por exemplo, em corpos finitos).
* Por isso, $K[x]$ e $\mathcal{P}_K$ **não são** isomorfos em geral.
* Em corpos infinitos, o mapeamento $f \mapsto \tilde{f}$ é injetivo.

---

### 2. **Raiz de uma função polinomial**

Seja $f(x) \in K[x]$.
Dizemos que $\alpha \in K$ é uma **raiz** de $f$ se:

$$
f(\alpha) = \tilde{f}(\alpha) = 0
$$

Ou seja, substituindo $x = \alpha$, o valor do polinômio se anula.

O **conjunto das raízes** de $f$ em $K$ é:

$$
Z_K(f) := \left\{ \alpha \in K \;\middle|\; f(\alpha) = 0 \right\}
$$

---

### 3. **Multiplicidade da raiz**

Se $\alpha \in K$ é tal que:

$$
f(x) = (x - \alpha)^m \cdot g(x),\quad \text{com } g(\alpha) \ne 0
$$

então dizemos que $\alpha$ é uma **raiz de multiplicidade $m$** de $f$.

---

## Exemplos

1. Em $\mathbb{R}[x]$, o polinômio $f(x) = x^2 - 4$ define a função:

$$
\tilde{f}(\alpha) = \alpha^2 - 4
$$

com raízes $\alpha = \pm 2$, pois $\tilde{f}(\pm 2) = 0$.

2. Em $\mathbb{F}_2$, temos:

$$
f(x) = x^2 + x \Rightarrow \tilde{f}(0) = 0,\quad \tilde{f}(1) = 0
$$

então ambas as classes $0,1 \in \mathbb{F}_2$ são raízes.

3. Em $\mathbb{C}$, $f(x) = x^2 + 1$ tem raízes $i$ e $-i$, mas em $\mathbb{R}$ não tem nenhuma raiz.


