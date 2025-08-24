# Espaço Métrico

Um **espaço métrico** é uma estrutura fundamental na Análise e na Topologia em que se quantifica a “distância” entre pares de pontos. Formalmente, consiste de um par $(X,d)$ onde:

**1. Conjunto de pontos**

   $$
     X\neq\varnothing
   $$

   é um conjunto arbitrário (pode ser finito ou infinito).

**2. Métrica**

   $$
     d : X \times X \;\to\; \mathbb{R}
   $$

   é uma função, chamada de **distância**, que associa a cada par $(x,y)\in X\times X$ um número real $d(x,y)$.

---

### 1. Axiomas da Métrica

Para todo $x,y,z\in X$, a função $d$ deve satisfazer:

1. **Positividade**:
   $d(x,y)\;\ge\;0.$

2. **Identidade dos indiscerníveis**:
   $d(x,y)=0 \;\iff\; x=y.$

3. **Simetria**:
   $d(x,y)=d(y,x)$

4. **Desigualdade triangular**:
   $d(x,z)\;\le\;d(x,y)+d(y,z)$

### 2. Propriedades e Construções Induzidas

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
  $(X,d)$ é **completo** se toda [sequência de Cauchy](../conceitos-gerais/cauchy-sequence.md) (onde $d(x_m,x_n)\to0$ quando $m,n\to\infty$) converge a um ponto em $X$.

---

## Leia também:

- [Espaço](../conceitos-gerais/espacos.md)