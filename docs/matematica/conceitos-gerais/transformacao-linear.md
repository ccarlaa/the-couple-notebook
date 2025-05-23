**Resumo (explicação simples)**
Uma **transformação linear** (ou **aplicação linear**, ou **morfismo de espaços vetoriais**) é uma função entre dois espaços vetoriais que preserva soma de vetores e multiplicação por escalares. Em termos geométricos, ela “respeita” a estrutura de combinações lineares.

---

## Definição Formal

Sejam

$$
(V, K, +_V, \bullet_V)
\quad\text{e}\quad
(W, K, +_W, \bullet_W)
$$

espaços vetoriais sobre o mesmo corpo $K$. Uma aplicação

$$
T\colon V \;\longrightarrow\; W
$$

é chamada **transformação linear** se, e somente se, para todos $u,v\in V$ e todo $\lambda\in K$ valem os dois axiomas:

1. **Aditividade**

   $$
   T(u +_V v) \;=\; T(u) +_W T(v).
   $$

2. **Homogeneidade (ou compatibilidade escalar)**

   $$
   T(\lambda \bullet_V v) \;=\; \lambda \bullet_W T(v).
   $$

Em notação compacta, pode-se escrever:

$$
\forall\,u,v\in V,\;\forall\,\lambda\in K,\quad
T(u + v) = T(u) + T(v),
\quad
T(\lambda v) = \lambda\,T(v).
$$

---

## Definições Associadas

* **Núcleo** ($\ker T$)

  $$
    \ker T 
    := \{\,v\in V \mid T(v) = 0_W\}.
  $$
* **Imagem** ($\operatorname{Im} T$)

  $$
    \operatorname{Im} T
    := \{\,T(v)\in W \mid v\in V\}.
  $$
* **Propriedades**

  * $T$ é **injetora** ⟺ $\ker T = \{0_V\}$.
  * $T$ é **sobrejetora** ⟺ $\operatorname{Im}T = W$.
  * **Teorema da dimensão** (caso $\dim V < \infty$):
    $\displaystyle \dim V = \dim(\ker T) + \dim(\operatorname{Im}T).$

---

## Exemplos

1. **Mapa identidade**
   $\displaystyle \mathrm{id}_V\colon V\to V,\;\mathrm{id}_V(v)=v$.

2. **Mapa nulo**
   $\displaystyle T\colon V\to W,\;T(v)=0_W$ para todo $v\in V$.

3. **Multiplicação por matriz**
   Se $A\in M_{m\times n}(K)$, então
   $$
     T_A\colon K^n \to K^m,\quad T_A(x)=A\,x
   $$
   é transformação linear.

4. **Derivação em polinômios**
   $$
     D\colon K[x]\to K[x],\quad D\Bigl(\sum_i a_i x^i\Bigr)
     = \sum_i i\,a_i x^{i-1}.
   $$
   Verifica $D(f+g)=D(f)+D(g)$ e $D(\lambda f)=\lambda D(f)$.

5. **Projeção ortogonal**
   Em um espaço euclidiano $V$, a aplicação que leva cada vetor ao seu componente sobre um subespaço $U\subset V$ é linear.
