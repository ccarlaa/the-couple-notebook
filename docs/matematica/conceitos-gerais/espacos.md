# Espaços

## **Definição geral de espaço**

 Um **espaço** é um par $(X, \mathcal{E})$, onde:

 * $X$ é um conjunto não vazio, chamado de **conjunto de pontos** (ou conjunto suporte);
 * $\mathcal{E}$ é uma **estrutura** adicional sobre $X$, definida por axiomas próprios, dependendo do tipo de espaço considerado (topológico, vetorial, métrico, etc.).

---

## Espaço Métrico

Um **espaço métrico** é uma estrutura fundamental na Análise e na Topologia em que se quantifica a “distância” entre pares de pontos. Formalmente, consiste de um par $(X,d)$ onde:

1. **Conjunto de pontos**

   $$
     X\neq\varnothing
   $$

   é um conjunto arbitrário (pode ser finito ou infinito).

2. **Métrica**

   $$
     d : X \times X \;\to\; \mathbb{R}
   $$

   é uma função, chamada de **distância**, que associa a cada par $(x,y)\in X\times X$ um número real $d(x,y)$.

---

### Axiomas da Métrica

Para todo $x,y,z\in X$, a função $d$ deve satisfazer:

1. **Positividade**

   $$
     d(x,y)\;\ge\;0.
   $$

2. **Identidade dos indiscerníveis**

   $$
     d(x,y)=0 \;\iff\; x=y.
   $$

3. **Simetria**

   $$
     d(x,y)=d(y,x).
   $$

4. **Desigualdade triangular**

   $$
     d(x,z)\;\le\;d(x,y)+d(y,z).
   $$

---

### Propriedades e Construções Induzidas

* **Bolas abertas e fechadas**

  * Bola aberta de raio $r>0$ em torno de $x$:
    $\displaystyle B(x,r)=\{\,y\in X\mid d(x,y)<r\}.$
  * Bola fechada de raio $r$:
    $\displaystyle \overline{B}(x,r)=\{\,y\in X\mid d(x,y)\le r\}.$

* **Topologia induzida**
  O conjunto de todas as bolas abertas forma uma base para uma topologia em $X$. Assim, todo espaço métrico é, em particular, um **espaço topológico**.

* **Convergência de sequências**
  Uma sequência $(x_n)\subset X$ **converge** a $x\in X$ se, para todo $\varepsilon>0$, existe $N$ tal que

  $$
    n\ge N \;\implies\; d(x_n,x)<\varepsilon.
  $$

* **Completude**
  $(X,d)$ é **completo** se toda sequência de Cauchy (onde $d(x_m,x_n)\to0$ quando $m,n\to\infty$) converge a um ponto em $X$.

---

## Espaço Vetorial 

Um **espaço vetorial** (também chamado de **espaço linear**) é uma estrutura algébrica fundamental que generaliza o conceito de vetores do espaço tridimensional para qualquer dimensão e qualquer corpo (como $\mathbb{R}$, $\mathbb{C}$, etc.).

---

### **Definição Formal**

Um **espaço vetorial** é um par $(V, \mathbb{K})$, onde:

* $V$ é um conjunto cujos elementos são chamados de **vetores**;
* $\mathbb{K}$ é um **corpo** (por exemplo, $\mathbb{R}$, $\mathbb{C}$, $\mathbb{Q}$);
* estão definidas duas operações:

  1. **Adição de vetores**:
     $+\colon V \times V \to V$, \quad $(u,v) \mapsto u + v$
  2. **Multiplicação por escalar**:
     $\cdot\colon \mathbb{K} \times V \to V$, \quad $(\alpha, v) \mapsto \alpha v$

essas operações devem satisfazer os **oito axiomas** abaixo:

---

### **Axiomas dos Espaços Vetoriais**

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

### **Exemplos de Espaços Vetoriais**

1. $\mathbb{R}^n$ com adição e multiplicação escalar usuais.
2. O conjunto de todas as funções contínuas $f : \mathbb{R} \to \mathbb{R}$.
3. O conjunto das matrizes $n \times m$ com entradas em $\mathbb{R}$.
4. O espaço das polinomiais de grau ≤ $n$:
   $\mathbb{P}_n = \{\,p(x) = a_0 + a_1x + \dots + a_nx^n \mid a_i \in \mathbb{K}\,\}$

---

### **Conceitos Relacionados**

* **Subespaço vetorial**: subconjunto de $V$ que é ele próprio um espaço vetorial.
* **Base**: conjunto de vetores linearmente independentes que gera $V$.
* **Dimensão**: número de vetores em qualquer base de $V$.
* **Dependência linear**: relação não trivial entre vetores pela combinação linear.
* **Transformações lineares**: funções entre espaços vetoriais que preservam a estrutura (i.e., lineares).

---

### **Usos**

* **Geometria e Física**: representação de forças, deslocamentos, etc.
* **Álgebra Linear**: resolução de sistemas lineares, mudança de base.
* **Ciência de Dados e IA**: vetores de características, embeddings, PCA.
* **Análise Funcional**: espaços de funções, espaços de Hilbert e Banach.
* **Computação Gráfica**: manipulação de imagens, rotação e translação de objetos.

---

### **Resumo**

Um **espaço vetorial** é um conjunto de objetos (vetores) que podem ser somados entre si e multiplicados por escalares, obedecendo regras bem definidas. Essa estrutura é a base de grande parte da matemática moderna, especialmente da álgebra linear.

