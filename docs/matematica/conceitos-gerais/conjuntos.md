# Conjuntos

## Conjuntos

### **Definição**

Seja $U$ um “universo” de discurso (conjunto de referência). Um **conjunto** $A$ é determinado por uma propriedade (predicado) $P$ que seus elementos satisfazem:

$$
A \;=\; \{\,x \in U \mid P(x)\,\}.
$$

Ou, de forma abreviada, quando o universo estiver implícito,

$$
A \;=\; \{\,x \mid P(x)\,\}.
$$

---
### **Propriedades**

**1. Axioma da Extensão**

Dois conjuntos são iguais **exatamente** quando possuem os mesmos elementos:

$$
\forall X\,\forall Y\;\Bigl(\,X = Y \;\iff\;\forall z\,(z\in X \iff z\in Y)\Bigr).
$$

---

**2. Conjunto vazio**

Define-se o conjunto vazio como aquele que não contém elemento algum:

$$
\varnothing \;=\;\{\,x\mid x \neq x\,\}.
$$

Em particular, vale

$$
\forall x\;\bigl(x \notin \varnothing\bigr).
$$

---

**3. Operações básicas**

* **União**
  $\displaystyle X\;\cup\;Y \;=\;\{\,z\mid z\in X \;\lor\; z\in Y\,\}.$

* **Interseção**
  $\displaystyle X\;\cap\;Y \;=\;\{\,z\mid z\in X \;\land\; z\in Y\,\}.$

* **Subconjunto**
  $\displaystyle X\subseteq Y \;\iff\;\forall z\,(z\in X\implies z\in Y).$

* **Diferença**
  $\displaystyle X\setminus Y \;=\;\{\,z\mid z\in X \;\land\; z\notin Y\,\}.$

---

## **Corpo** (em Álgebra Abstrata)

Um **corpo** (do latim *corpus*, em inglês *field*) é uma estrutura algébrica fundamental que generaliza as propriedades dos números racionais $\mathbb{Q}$, reais $\mathbb{R}$ e complexos $\mathbb{C}$, permitindo as operações de adição, subtração, multiplicação e divisão (exceto por zero), obedecendo certos axiomas.

---

### **Definição Formal**

Um **corpo** é um conjunto não vazio $\mathbb{K}$ munido de duas operações binárias:

* **Adição**: $(a,b) \mapsto a + b$
* **Multiplicação**: $(a,b) \mapsto a \cdot b$

tais que os seguintes **axiomas** são satisfeitos para todos $a, b, c \in \mathbb{K}$:

---

### **Axiomas dos Corpos**

#### **1. Axiomas da adição:**

1. (Associatividade) $(a + b) + c = a + (b + c)$
2. (Comutatividade) $a + b = b + a$
3. (Elemento neutro aditivo) Existe $0 \in \mathbb{K}$ tal que $a + 0 = a$
4. (Inverso aditivo) Para todo $a$, existe $(-a)$ tal que $a + (-a) = 0$

#### **2. Axiomas da multiplicação:**

5. (Associatividade) $(a \cdot b) \cdot c = a \cdot (b \cdot c)$
6. (Comutatividade) $a \cdot b = b \cdot a$
7. (Elemento neutro multiplicativo) Existe $1 \in \mathbb{K}$, com $1 \ne 0$, tal que $a \cdot 1 = a$
8. (Inverso multiplicativo) Para todo $a \ne 0$, existe $a^{-1}$ tal que $a \cdot a^{-1} = 1$

#### **3. Distributividade entre as operações:**

9. (Distributividade) $a \cdot (b + c) = a \cdot b + a \cdot c$

---

### **Exemplos de Corpos**

* $\mathbb{Q}$: corpo dos números racionais
* $\mathbb{R}$: corpo dos números reais
* $\mathbb{C}$: corpo dos números complexos

---

### **Observações Importantes**

* Em um corpo, **todo elemento diferente de zero tem inverso multiplicativo**.
* Um corpo **não admite divisão por zero**, pois $0^{-1}$ não está definido.
* Um corpo com número finito de elementos é chamado de **corpo finito** ou **corpo de Galois**.

### **Resumo**

> Um **corpo** é um conjunto onde se pode **somar, subtrair, multiplicar e dividir** (exceto por zero), de maneira que essas operações obedeçam regras semelhantes às dos números reais.

---

## **Produto Cartesiano**

O **produto cartesiano** é uma construção fundamental da matemática que combina dois (ou mais) conjuntos em um novo conjunto formado por **pares ordenados**. 

---

### **Definição Formal**

Sejam $A$ e $B$ dois conjuntos. O **produto cartesiano** de $A$ e $B$, denotado por $A \times B$, é o conjunto de **pares ordenados** $(a, b)$ tais que:

$$
A \times B = \{\, (a, b) \mid a \in A \;\text{e}\; b \in B \,\}
$$

Cada elemento de $A \times B$ é um par ordenado onde o **primeiro elemento vem de $A$** e o **segundo de $B$**.

---

### **Propriedades**

* A ordem **importa**:
  Se $A \ne B$, então geralmente $A \times B \ne B \times A$.
  Mesmo que $A = B$, temos:

  $$
  (a,b) \ne (b,a) \quad \text{a menos que } a = b
  $$

* Se $A$ e $B$ têm cardinalidades $m$ e $n$, respectivamente, então:

  $$
  |A \times B| = |A| \cdot |B| = m \cdot n
  $$

* A noção se generaliza para mais conjuntos:

  $$
  A_1 \times A_2 \times \cdots \times A_n = \{\, (a_1, a_2, \dots, a_n) \mid a_i \in A_i \,\}
  $$

---

### **Exemplos**

1. Se $A = \{1,2\}$ e $B = \{a,b\}$, então:

   $$
   A \times B = \{ (1,a), (1,b), (2,a), (2,b) \}
   $$

2. $\mathbb{R} \times \mathbb{R} = \mathbb{R}^2$:
   O plano cartesiano, onde cada ponto é um par $(x,y)$ com $x,y \in \mathbb{R}$

3. $A \times \varnothing = \varnothing$:
   O produto com o conjunto vazio é vazio.

---

## **Lei da Composição Interna** 

Uma **lei de composição interna** (ou **operação interna**) é uma aplicação que **combina dois elementos de um mesmo conjunto** e retorna **um elemento ainda dentro desse conjunto**.

---

### **Definição**

Seja $A$ um conjunto não vazio. Uma **lei de composição interna** em $A$ é uma função:

$$
\ast \colon A \times A \to A
$$

que associa a cada par $(a, b) \in A \times A$ um único elemento $a \ast b \in A$.

---

### **Explicação**

* A operação $\ast$ **fecha em $A$**, isto é, para quaisquer $a, b \in A$, o resultado $a \ast b$ também pertence a $A$.
* O símbolo $\ast$ pode representar qualquer operação binária: soma, produto, máximo, etc.

---

### **Exemplos**

1. **Soma em $\mathbb{Z}$**:

   $$
   + \colon \mathbb{Z} \times \mathbb{Z} \to \mathbb{Z}, \quad (a, b) \mapsto a + b
   $$

   é uma lei de composição interna.

2. **Máximo em um conjunto $A = \{1, 2, 3\}$**:

   $$
   \max(a, b)
   $$

   define uma operação interna se os resultados sempre estiverem em $A$.

3. **Produto de matrizes quadradas $n \times n$**:
   A multiplicação é uma lei de composição interna no conjunto das matrizes quadradas de ordem $n$.

---

### **Observação**

Se a imagem da operação **não está contida em $A$**, diz-se que a operação é **externa**.
Por exemplo, a multiplicação escalar em um espaço vetorial $V$,

$$
\cdot \colon \mathbb{K} \times V \to V
$$

é uma **lei de composição externa**.

---


