# Espaço Amostral

## 1. Introdução

Um **experimento aleatório** (ou estatístico) é um experimento em que, **sob condições fixas e bem definidas**, pode ser repetido sob condições identicas e cujos **possíveis resultados são conhecidos**, mas o **resultado específico do experimento não pode ser previsto**. 

Na **Teoria da Probabilidade** nós estudamos esse tipo de incerteza em um experimento aleatório. Onde normalmente esse tipo de experimento é associado a um conjunto $\Omega$, o conjunto de todos os possíveis resultados do experimento. E associamos $\Omega$ a uma [$\sigma$-álgebra](../conceitos-gerais/sigma-algebra.md) de subconjuntos de $\Omega$.

## 2. Definição Formal

Um Espaço Amostral de um esperimento estatístico é um par $(\Omega, \mathcal{S})$, tal que:

1. $\Omega$ é o conjunto de **todos os possíveis resultados** do experimento;

2. $\mathcal{S}$ é uma $\sigma$-álgebra dos subconjuntos de $\Omega$.

Os elementos de $\Omega$ representão **um único** resultado é são representados por $\omega$. E qualquer conjunto $E \in \mathcal{S}$ é chamado de **Evento**.