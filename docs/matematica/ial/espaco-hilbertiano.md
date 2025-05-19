# Espaço de Hilbert

## 1. Definição Formal

Seja $\mathcal{H}$ um espaço vetorial sobre o corpo $\mathbb{K}$ (onde $\mathbb{K} = \mathbb{R}$ ou $\mathbb{C}$), equipado com um produto interno $\langle \cdot, \cdot \rangle: \mathcal{H} \times \mathcal{H} \to \mathbb{K}$. O espaço $\mathcal{H}$ é chamado de **espaço de Hilbert** se for completo em relação à norma induzida pelo produto interno, definida por:

$$
\|x\| = \sqrt{\langle x, x \rangle}, \quad \forall x \in \mathcal{H}.
$$

A completude significa que toda sequência de Cauchy em $\mathcal{H}$ converge para um elemento em $\mathcal{H}$ com respeito à norma $\| \cdot \|$, ou seja, para cada 2 elementos existe um outro entre eles na qual a distância para qualquer dos 2 elementos é menor que a distância entre eles.

## 2. Norma Induzida e Desigualdade de Cauchy-Schwarz

A norma induzida pelo produto interno é dada por:

$$
\|x\| = \sqrt{\langle x, x \rangle}.
$$

Essa norma satisfaz a **desigualdade de Cauchy-Schwarz**:

$$
|\langle x, y \rangle| \leq \|x\| \cdot \|y\|, \quad \forall x, y \in \mathcal{H}.
$$

## 3. Exemplos de Espaços de Hilbert

* **Espaço $\mathbb{R}^n$**: Com o produto interno usual $\langle x, y \rangle = \sum_{i=1}^n x_i y_i$, é um espaço de Hilbert de dimensão finita.

* **Espaço $\ell^2$**: Conjunto de todas as sequências $(x_n)$ de números complexos tais que $\sum_{n=1}^\infty |x_n|^2 < \infty$, com produto interno $\langle x, y \rangle = \sum_{n=1}^\infty x_n \overline{y_n}$.

* **Espaço $L^2(\Omega)$**: Conjunto de todas as funções mensuráveis $f: \Omega \to \mathbb{C}$ tais que $\int_\Omega |f(x)|^2 dx < \infty$, com produto interno $\langle f, g \rangle = \int_\Omega f(x) \overline{g(x)} dx$.
