# $\sigma$-Álgebra

Um **$\sigma$-field** (ou **$\sigma$-álgebra**, mais comum em português) é um conceito fundamental na teoria da probabilidade e da teoria da medida. Em resumo, uma σ-álgebra $\mathcal{S}$ sobre um conjunto $X$ é uma coleção de subconjuntos de $X$ que contém $X$, é fechada por **complemento** e por uniões **contáveis**.

---

## **1. Definição Formal de $\sigma$-álgebra**

Seja $X$ um conjunto **não vazio**, uma $\sigma$-álgebra sobre o conjunto $X$ é o conjunto

$$ 
    \mathcal{S} \subseteq \mathcal{P}(X)
$$

que satisfaz as seguintes propriedades:

### **Axiomas de uma $\sigma$-álgebra**

1. **Contém o espaço total:**

   $$
   X \in \mathcal{S}
   $$
2. **Fechamento por complemento:**

   $$
   \forall A \in \mathcal{S} \implies A^c = X \setminus A \in \mathcal{S}
   $$
3. **Fechamento por uniões enumeráveis:**

   $$
   \forall \{A_i\}_{i=1}^\infty \subseteq \mathcal{S}, \quad \bigcup_{i=1}^\infty A_i \in \mathcal{S}
   $$

---

## **2. Propriedades Derivadas**

A partir dos axiomas, podemos deduzir automaticamente que:

* **Fechamento por interseções enumeráveis**:
  Pelo **De Morgan**:

  $$
  \bigcap_{i=1}^\infty A_i
  = \left(\bigcup_{i=1}^\infty A_i^c\right)^c \in \mathcal{S}
  $$
* **Contém o conjunto vazio**:
  Como $X \in \mathcal{S}$ e $X^c = \varnothing$, temos:

  $$
  \varnothing \in \mathcal{S}
  $$
* **Fechamento por diferenças**:
  Se $A,B \in \mathcal{S}$, então:

  $$
  A \setminus B = A \cap B^c \in \mathcal{S}
  $$

---

## **3. Intuição para Probabilidade e Estatística**

Uma **$\sigma$-álgebra** é um **sistema de conjuntos** que representa **todos os eventos mensuráveis** de um experimento aleatório.

* **$\Omega$** → espaço de todos os resultados possíveis.
* **$\mathcal{F}$** → **conjunto dos eventos que podem ter probabilidade definida**.
* Cada $A \in \mathcal{F}$ é chamado de **evento mensurável**.

---