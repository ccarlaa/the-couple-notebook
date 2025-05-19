# Produto Interno

A **produto interno** (ou **forma bilinear positiva definida**, no caso real) é uma operação que, a cada par de vetores num espaço vetorial, associa um número escalar de modo a generalizar as noções de “comprimento” e “ângulo”. A seguir, a definição completa em notação formal.

---

## 1. Contexto

Seja $V$ um espaço vetorial sobre um corpo $\mathbb{K}$, onde:

* $\mathbb{K} = \mathbb{R}$ (caso real) ou $\mathbb{K} = \mathbb{C}$ (caso complexo);
* As operações em $V$ são:

  * adição: $+\colon V\times V\to V$;
  * multiplicação escalar: $\cdot\colon \mathbb{K}\times V\to V$.

---

## 2. Definição

Um **produto interno** em $V$ é uma aplicação

$$
\langle \,\cdot\,,\,\cdot\,\rangle \colon V \times V \;\longrightarrow\; \mathbb{K}
$$

tal que, para todos $u,v,w\in V$ e todo escalar $\alpha\in\mathbb{K}$, valem as seguintes propriedades:

1. **(Conjugado-simetria)**

   $$
     \langle u, v \rangle
     = \overline{\langle v, u \rangle}
     \quad
     (\text{se }\mathbb{K}=\mathbb{C})
     \quad\text{ou}\quad
     \langle u, v \rangle = \langle v, u \rangle
     \quad
     (\mathbb{K}=\mathbb{R}).
   $$

2. **(Linearidade no primeiro argumento)**

   $$
     \langle \alpha u + v,\;w\rangle
     = \alpha\,\langle u,w\rangle \;+\;\langle v,w\rangle.
   $$

3. **(Positividade)**

   $$
     \langle v, v \rangle \;>\; 0
     \quad\text{para todo }v\neq 0,
     \quad\text{e}\quad
     \langle v,v\rangle = 0 \iff v=0.
   $$

> Quando $\mathbb{K}=\mathbb{C}$, diz‑se normalmente que o produto interno é **sesquilinear** (linear num argumento e conjugado‑linear no outro) e **definido positivo**.

---

## 3. Construções Induzidas

Dado $\langle\cdot,\cdot\rangle$, definimos:

* **Norma**

  $$
    \|v\| \;=\;\sqrt{\langle v, v\rangle}.
  $$

* **Distância**

  $$
    d(u,v) \;=\;\|u - v\|.
  $$

* **Ângulo**

  $$
    \cos\theta
    = \frac{\Re\,\langle u,v\rangle}{\|u\|\;\|v\|},
  $$

  onde $\Re$ é a parte real (no caso complexo).

---

## 4. Exemplos Canônicos

1. **$\mathbb{R}^n$ real**
   $\displaystyle \langle u,v\rangle = \sum_{i=1}^n u_i\,v_i.$

2. **$\mathbb{C}^n$ complexo**
   $\displaystyle \langle u,v\rangle = \sum_{i=1}^n u_i\,\overline{v_i}.$

3. **Espaço de funções**
   Em $C[a,b]$,
   $\displaystyle \langle f,g\rangle = \int_a^b f(x)\,\overline{g(x)}\,dx.$

---

## **Espaço Vetorial Euclidiano**

Um **espaço vetorial euclidiano** é um espaço vetorial real de dimensão finita no qual é definido um **produto interno**. Isso permite medir **distâncias, ângulos, comprimentos** e realizar a **geometria analítica** com base vetorial.

---

### **Definição**

Um **espaço vetorial euclidiano** é um par $(V, \langle \cdot,\cdot \rangle)$, onde:

* $V$ é um espaço vetorial real de dimensão finita;
* $\langle \cdot,\cdot \rangle$ é um produto interno definido em $V$.

Esse produto interno permite definir:

* **Norma** (comprimento):
  $\|v\| = \sqrt{\langle v, v \rangle}$

* **Distância** entre vetores:
  $d(u, v) = \|u - v\|$

* **Ângulo** entre vetores:
  $\cos \theta = \dfrac{\langle u, v \rangle}{\|u\| \cdot \|v\|}$

---

### **Exemplo Canônico**

O espaço $\mathbb{R}^n$, com o produto interno padrão:

$$
\langle u, v \rangle = \sum_{i=1}^{n} u_i v_i
$$

é o exemplo mais comum de espaço vetorial euclidiano.

---
