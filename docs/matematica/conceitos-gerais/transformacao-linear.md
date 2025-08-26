# Transformação Linear

**Resumo**

Uma **transformação linear** (ou **aplicação linear**) é uma função entre dois espaços vetoriais que preserva soma de vetores e multiplicação por escalares. Em termos geométricos, ela “respeita” a estrutura de combinações lineares.

---

## Definição Formal

Sejam

$$
(V, \mathbb{K}, +, \cdot)
\quad\text{e}\quad
(W, \mathbb{K}, +, \cdot)
$$

espaços vetoriais sobre o mesmo corpo $\mathbb{K}$. Uma aplicação

$$
T\colon V \longrightarrow W
$$

é chamada **transformação linear** se, e somente se, para todos $u,v\in V$ e todo $\lambda\in \mathbb{K}$ valem os dois axiomas:

1. **Aditividade**

   $$
   T(u + v) \;=\; T(u) + T(v).
   $$

2. **Homogeneidade (ou compatibilidade escalar)**

   $$
   T(\lambda \cdot v) \;=\; \lambda \cdot T(v).
   $$


---

## Definições Associadas

* **Núcleo** ($\ker T$)

  $$
    \ker T 
    := \{\,v\in V \mid T(v) = 0\}.
  $$
* **Imagem** ($\operatorname{Im} T$)

  $$
    \operatorname{Im} T
    := \{\,T(v)\in W \mid v\in V\}.
  $$
* **Propriedades**

  * $T$ é **injetora** ⟺ $\ker T = \{0\}$.
  * $T$ é **sobrejetora** ⟺ $\operatorname{Im}T = W$.
  * **Teorema da dimensão** (caso $\dim V < \infty$):
    $\displaystyle \dim V = \dim(\ker T) + \dim(\operatorname{Im}T).$

---

## Exemplos

1. **Mapa identidade**
   $\displaystyle \mathrm{id}\colon V\to V,\;\mathrm{id}(v)=v$.

2. **Mapa nulo**
   $\displaystyle T\colon V\to W,\;T(v)=0$ para todo $v\in V$.

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
