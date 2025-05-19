# Norma

A norma é uma função que generaliza a função Valor Absoluto.

## 1. Definição

Seja $V$ um espaço vetorial sobre o corpo $\Bbb K$ (onde $\Bbb K = \mathbb{R}$ ou $\mathbb{C}$). Uma **norma** sobre $V$ é uma aplicação

$$
\|\cdot\|\colon V \;\longrightarrow\; [0,\infty)
$$

que a cada vetor $x\in V$ associa um número real $\|x\|$, e que satisfaz, para todos $x,y\in V$ e todo escalar $\alpha\in\Bbb K$, as seguintes propriedades:

## 2. Propriedades

1. **Positividade**

   $$
   \|x\|\;\geq\;0.
   $$

2. **Definitude**

   $$
   \|x\| = 0
   \quad\Longleftrightarrow\quad
   x = 0.
   $$

3. **Homogeneidade (ou absoluto–homogeneidade)**

   $$
   \|\alpha\,x\|
   \;=\;
   |\alpha|\;\|x\|.
   $$

4. **Desigualdade triangular**

   $$
   \|x + y\|
   \;\le\;
   \|x\| \;+\;\|y\|.
   $$

A partir de uma norma $\|\cdot\|$ define‑se naturalmente uma métrica

$$
d\colon V\times V\;\longrightarrow\;\mathbb{R},\qquad
d(x,y)\;=\;\|x - y\|,
$$

que torna $(V,d)$ num espaço métrico.
