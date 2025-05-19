# Sequência de Cauthy

## 1. Definição 

Seja $E$ um espaço vetorial sobre o corpo $\Bbb K$ (onde $\Bbb K = \mathbb{R}$ ou $\mathbb{C}$) munido de uma norma $\|\cdot\|$. Definimos a métrica associada por

$$
d \colon E \times E \;\longrightarrow\; \mathbb{R},\qquad
d(x,y) \;=\;\|\,x - y\|\,. 
$$

Uma sequência $\{x_n\}_{n\in\mathbb{N}}\subset E$ é dita **sequência de Cauchy** se, e somente se, satisfaz a condição:

$$
\forall \varepsilon > 0,\;\;\exists N\in\mathbb{N}:\;\;
\forall\,m,n\gt N,\quad
d(x_n,x_m) \;<\;\varepsilon\,.
$$

Em termos de norma, escrevemos equivalentemente:

$$
\forall \varepsilon > 0,\;\;\exists N\in\mathbb{N}:\;\;
\forall\,m,n\ge N,\quad
\bigl\|\,x_n - x_m \bigr\| \;<\; \varepsilon\,.
$$

---

## 2. Comentários adicionais

1. **Dependência da distância**
   A definição acima emprega a métrica $d$ induzida pela norma. Em espaços vetoriais com outra métrica $d$, basta substituir $d(x_n,x_m)$ na mesma forma.

2. **Intuição**
   A ideia central é que os termos da sequência “se aproximam cada vez mais uns dos outros” à medida que $n,m\to\infty$.

3. **Completude**
   Um espaço vetorial normado $(E,\|\cdot\|)$ é **completo** se toda sequência de Cauchy em $E$ converge para algum limite em $E$. Quando $E$ é completo, chamamos $(E,\|\cdot\|)$ de **espaço de Banach**.

<figure markdown="span">
  ![Sequência de Cauchy](../assets/Cauchy_sequence_illustration.png){ width="500" align="center" }
  <figcaption>Imagem 1: Gráfico de uma sequência de Cauchy.</figcaption>
</figure>