# Composição Interna

## 1. Definição Formal 

Seja $A$ um conjunto não vazio. Uma **lei de composição interna** (ou **operação binária**) em $A$ é uma função:

$$
\ast: A \times A \to A
$$

que associa a cada par ordenado $(a, b) \in A \times A$ um elemento $a \ast b \in A$. Isso significa que a operação $\ast$ é **fechada** em $A$, ou seja, o resultado da operação entre quaisquer dois elementos de $A$ também pertence a $A$.

## 2. Propriedades 

1. **Associatividade**:

   $$
   \forall a, b, c \in A,\quad (a \ast b) \ast c = a \ast (b \ast c)
   $$

2. **Comutatividade**:

   $$
   \forall a, b \in A,\quad a \ast b = b \ast a
   $$

3. **Elemento Neutro**:
   Existe $e \in A$ tal que:

   $$
   \forall a \in A,\quad a \ast e = e \ast a = a
   $$

4. **Elemento Inverso**:
   Para cada $a \in A$, existe $a' \in A$ tal que:

   $$
   a \ast a' = a' \ast a = e
   $$

   onde $e$ é o elemento neutro.

5. **Regularidade**:
   Um elemento $a \in A$ é regular se:

   $$
   \forall x, y \in A,\quad a \ast x = a \ast y \Rightarrow x = y \quad \text{e} \quad x \ast a = y \ast a \Rightarrow x = y
   $$

## 3. Exemplos

1. **Adição em $\mathbb{N}$**:
   A operação $+: \mathbb{N} \times \mathbb{N} \to \mathbb{N}$, definida por $(a, b) \mapsto a + b$, é uma lei de composição interna em $\mathbb{N}$. É associativa e comutativa, com elemento neutro $0$.

2. **Multiplicação em $\mathbb{Z}$**:
   A operação $\cdot: \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}$, definida por $(a, b) \mapsto a \cdot b$, é uma lei de composição interna em $\mathbb{Z}$. É associativa e comutativa, com elemento neutro $1$.

3. **Subtração em $\mathbb{N}$**:
   A operação $-: \mathbb{N} \times \mathbb{N} \to \mathbb{N}$, definida por $(a, b) \mapsto a - b$, não é uma lei de composição interna em $\mathbb{N}$, pois, por exemplo, $2 - 3 = -1 \notin \mathbb{N}$.

4. **Interseção de Conjuntos**:
   Seja $\mathcal{P}(S)$ o conjunto das partes de um conjunto $S$. A operação $\cap: \mathcal{P}(S) \times \mathcal{P}(S) \to \mathcal{P}(S)$, definida por $(A, B) \mapsto A \cap B$, é uma lei de composição interna em $\mathcal{P}(S)$. É associativa, comutativa e tem como elemento neutro o conjunto $S$.

## Observações

* A existência de uma lei de composição interna em um conjunto $A$ permite a definição de estruturas algébricas mais complexas, como semigrupos, monóides e grupos, dependendo das propriedades adicionais que a operação $\ast$ satisfaz.
* A análise das propriedades da operação é fundamental para a classificação da estrutura algébrica formada pelo conjunto $A$ com a operação $\ast$.
