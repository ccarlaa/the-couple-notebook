# Polinômios formais

Seja $K$ um corpo e seja $X$ um símbolo («indeterminada»). Definimos o anel dos **polinômios formais** em $X$ sobre $K$, denotado $K[X]$, como segue:

---

## 1. Definição via sequências de suporte finito

$$
K[X]
:=
\Bigl\{\,a = (a_i)_{i\in\mathbb{N}}\in K^{\mathbb{N}}
  \;\Big|\;\exists N\in\mathbb{N}\;\forall i > N:\;a_i=0
\Bigr\}.
$$

Cada $a = (a_0,a_1,\dots)$ corresponde ao polinômio formal

$$
a(X) \;=\;\sum_{i=0}^{\infty} a_i\,X^i
$$

onde, por hipótese de suporte finito, essa soma é na prática finita.

---

## 2. Operações em $K[X]$

1. **Adição**
    Dados $a=(a_i)$ e $b=(b_i)$ em $K[X]$, define‑se

    $$
    a + b \;=\;(a_i + b_i)_{\,i\in\mathbb{N}}.
    $$

2. **Multiplicação**
    Dados $a=(a_i)$ e $b=(b_i)$, define‑se $c = a\cdot b$ por

    $$
    c_i
    \;=\;
    \sum_{j+k = i} a_j\,b_k,
    \quad i\in\mathbb{N}.
    $$

    Em notação de soma finita,

    $$
    (a\cdot b)(X)
    = 
    \sum_{i=0}^{\infty} \biggl(\sum_{j+k=i}a_j\,b_k\biggr)\,X^i.
    $$

3. **Elemento neutro**

    * Soma: $0 = (0,0,0,\dots)$, que corresponde ao polinômio $0$.
    * Produto: $1 = (1,0,0,\dots)$, que corresponde ao polinômio constante $1$.

---

## 3. Grau

Para $a=(a_i)\neq 0$, define‑se

$$
\deg(a)
:=
\max\{\,i\in\mathbb{N} : a_i \neq 0\}.
$$

---

## 4. Identificação usual

Pode‑se escrever cada $a\in K[X]$ como

$$
a(X)
\;=\;
\sum_{i=0}^{n}a_i\,X^i,
$$

onde $n = \deg(a)$.

Em particular, o monômio $X$ corresponde à sequência
$\displaystyle X = (0,1,0,0,\dots)$.

---

## 5. Propriedades

* $(K[X],+,\cdot)$ é um **anel comutativo** com unidade.
* Como $K$ é corpo, $K[X]$ é um **domínio de integridade**.
* A unidade e o monômio $X$ geram livremente $K[X]$ como álgebra sobre $K$.

---

Em resumo, $K[X]$ é o conjunto de somas finitas $\sum a_iX^i$ com $a_i\in K$, dotado de adição coeficiente a coeficiente e de multiplicação por convolução de coeficientes.
