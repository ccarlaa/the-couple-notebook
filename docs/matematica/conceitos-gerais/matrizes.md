# Matrizes

Uma **matriz** é uma estrutura matemática fundamental na álgebra linear, representando uma disposição retangular de elementos (números, variáveis ou expressões) organizados em linhas e colunas. Formalmente, uma matriz é definida como uma função que associa a cada par ordenado de índices um elemento de um conjunto, geralmente um corpo numérico.

---

## 1. Definição Formal

Sejam $m, n \in \mathbb{N}^*$ (números naturais positivos) e $K$ um corpo (como $\mathbb{R}$ ou $\mathbb{C}$). Uma **matriz de ordem $m \times n$** sobre $K$ é uma função:

$$
A: \{1, 2, \dots, m\} \times \{1, 2, \dots, n\} \to K
$$

Para cada par $(i, j)$, o valor $A(i, j) = a_{ij} \in K$ é chamado de **elemento** da matriz na posição $i$-ésima linha e $j$-ésima coluna.

A matriz $A$ pode ser representada como:

$$
A = [a_{ij}]_{m \times n} = 
\begin{bmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{m1} & a_{m2} & \cdots & a_{mn}
\end{bmatrix}
$$

---

## 2. Notação e Terminologia

* **Ordem da matriz**: $m \times n$, onde $m$ é o número de linhas e $n$ o número de colunas.
* **Elemento $a_{ij}$**: Valor na interseção da $i$-ésima linha com a $j$-ésima coluna.
* **Matriz quadrada**: Quando $m = n$.
* **Matriz linha**: Quando $m = 1$.
* **Matriz coluna**: Quando $n = 1$.
* **Matriz nula**: Todos os elementos são zero.
* **Matriz identidade $I_n$**: Matriz quadrada de ordem $n$ com 1's na diagonal principal e 0's nos demais elementos.

---

## 3. Operações com Matrizes

1. **Adição**: Duas matrizes $A$ e $B$ de mesma ordem $m \times n$ podem ser somadas elemento a elemento:

$$
(A + B)_{ij} = a_{ij} + b_{ij}
$$

2. **Multiplicação por escalar**: Multiplicação de cada elemento da matriz $A$ por um escalar $\lambda \in K$:

$$
(\lambda A)_{ij} = \lambda \cdot a_{ij}
$$

3. **Multiplicação de matrizes**: Se $A$ é de ordem $m \times p$ e $B$ de ordem $p \times n$, o produto $C = AB$ é uma matriz de ordem $m \times n$ com elementos:

$$
c_{ij} = \sum_{k=1}^{p} a_{ik} \cdot b_{kj}
$$

---

## 4. Propriedades Importantes

* **Associatividade da multiplicação**: $(AB)C = A(BC)$
* **Distributividade**: $A(B + C) = AB + AC$ e $(A + B)C = AC + BC$
* **Elemento neutro**: A matriz identidade $I_n$ satisfaz $AI_n = I_nA = A$ para qualquer matriz quadrada $A$ de ordem $n$
* **Transposta**: A transposta de $A$, denotada $A^T$, é obtida trocando linhas por colunas: $(A^T)_{ij} = a_{ji}$
* **Determinante**: Para matrizes quadradas, o determinante é uma função que associa um escalar à matriz, útil para verificar invertibilidade e resolver sistemas lineares.

---

## Exemplos

1. **Matriz $2 \times 3$**:

$$
A = 
\begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6
\end{bmatrix}
$$

2. **Matriz identidade $3 \times 3$**:

$$
I_3 = 
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

3. **Matriz nula $2 \times 2$**:

$$
O_{2 \times 2} = 
\begin{bmatrix}
0 & 0 \\
0 & 0
\end{bmatrix}
$$

---


