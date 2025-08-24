# Espaço Vetorial 

Consideremos um [Espaço](../conceitos-gerais/espacos.md) com coordenadas e em que cada ponto $P$ está associado a uma única grandeza chamada *vetor*, ou seja $v = \overrightarrow{OP}$, em que o ponto $O$ representa o ponto de origem das coordenadas. Um **espaço vetorial** (também chamado de **espaço linear**) é uma estrutura algébrica fundamental que caracteriza o conceito de vetores para qualquer dimensão e qualquer corpo (como $\mathbb{R}$, $\mathbb{C}$, etc.).

---

## **1. Definição Formal**

Um **espaço vetorial** é uma quádrupla

$$
(V, K, +, \cdot)
$$

tal que:

1. $V$ é um conjunt de vetores;
2. $K$ é um conjunto de números em um **corpo**;

E estão definidas duas operações:

  1. **Adição de vetores**:
     $+\colon V \times V \to V, \quad (u,v) \mapsto u + v$
  2. **Multiplicação por escalar**:
     $\cdot\colon \mathbb{K} \times V \to V, \quad (\alpha, v) \mapsto \alpha v$

essas operações devem satisfazer os **oito axiomas** abaixo:

## **2. Axiomas dos Espaços Vetoriais**

Para todos $u, v, w \in V$ e $\alpha, \beta \in \mathbb{K}$:

1. **Associatividade da adição**:
   $(u + v) + w = u + (v + w)$

2. **Comutatividade da adição**:
   $u + v = v + u$

3. **Elemento neutro da adição**:
   Existe $0 \in V$ tal que $u + 0 = u$

4. **Inverso aditivo**:
   Para cada $u\in V$, existe $(-u)\in V$ tal que $u + (-u) = 0$

5. **Compatibilidade da multiplicação escalar**:
   $\alpha(\beta v) = (\alpha\beta)v$

6. **Elemento neutro da multiplicação escalar**:
   $1 \cdot v = v$, onde $1$ é o elemento neutro de $\mathbb{K}$

7. **Distributividade em relação à adição de vetores**:
   $\alpha(u + v) = \alpha u + \alpha v$

8. **Distributividade em relação à adição de escalares**:
   $(\alpha + \beta)v = \alpha v + \beta v$

---

## **3. Exemplos de Espaços Vetoriais**

1. $\mathbb{R}^n$ com adição e multiplicação escalar usuais.
2. O conjunto de todas as funções contínuas $f : \mathbb{R} \to \mathbb{R}$.
3. O conjunto das matrizes $n \times m$ com entradas em $\mathbb{R}$.
4. O espaço das polinomiais de grau ≤ $n$:
   $\mathbb{P}_n = \{\,p(x) = a_0 + a_1x + \dots + a_nx^n \mid a_i \in \mathbb{K}\,\}$

---

## **4. Conceitos Relacionados**

* **Subespaço vetorial**: subconjunto de $V$ que é ele próprio um espaço vetorial.
* **Base**: conjunto de vetores linearmente independentes que gera $V$.
* **Dimensão**: número de vetores em qualquer base de $V$.
* **Dependência linear**: relação não trivial entre vetores pela combinação linear.
* **Transformações lineares**: funções entre espaços vetoriais que preservam a estrutura (i.e., lineares).

## Leia também:

- [Espaço](../conceitos-gerais/espacos.md)