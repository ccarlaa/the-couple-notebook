# Modulação DSB-FC AM

## 1. Definição da Modulação DSB-FC AM (AM Convencional)

A modulação DSB-FC AM** (*Double Sideband – Full Carrier Amplitude Modulation*), também conhecida como **AM convencional**. Ela é uma extensão da DSB-SC, mas inclui a portadora no sinal transmitido.

A **modulação DSB-FC AM** consiste em **modular a amplitude** de uma portadora senoidal de frequência $f_c$ com base em um sinal mensagem $m(t)$. O sinal resultante contém:

* a **portadora não suprimida**,
* e as **duas bandas laterais (inferior e superior)** com a informação do sinal mensagem.

---

## 2. Definições e Hipóteses

* $m(t) \in \mathbb{R}$: sinal mensagem, limitado em banda $B$ e com valor médio nulo (sem componente DC);
* $|m(t)| \leq 1$, se normalizado;
* $A_c > 0$: amplitude da portadora;
* $f_c \gg B$: frequência da portadora muito maior que a largura de banda da mensagem;
* $\mu \in [0,1]$: índice de modulação.

---

## 3. Expressão no Domínio do Tempo

A modulação DSB-FC é definida como:

$$
s(t) = \mathcal{M}_{\mathrm{DSB\text{-}FC}}\{m(t)\} = A_c[1 + \mu\, m(t)] \cos(\omega_c t),
$$

onde $\omega_c = 2\pi f_c$.

* $\mu = 0$: só a portadora.
* $\mu = 1$: modulação máxima sem distorção (evita overmodulation).
* $\mu > 1$: overmodulation, causa distorção na demodulação envelope.

---

## 4. Representação no Domínio da Frequência

Usando a Transformada de Fourier:

Seja $M(f)$ a transformada de $m(t)$, então:

$$
S(f) = \frac{A_c}{2} \left[ \delta(f - f_c) + \delta(f + f_c) \right] 
+ \frac{\mu A_c}{2} \left[ M(f - f_c) + M(f + f_c) \right].
$$

O espectro contém:

* **Portadora**: dois deltas em $\pm f_c$;
* **Bandas laterais**: transladadas para $f_c \pm f$, com largura de banda $B$.

---

## 5. Potência do Sinal Modulado

A potência total é composta por três componentes:

### 5.1. Portadora:

$$
P_{\text{c}} = \frac{A_c^2}{2}.
$$

### 5.2. Bandas laterais (ambas):

$$
P_{\text{BL}} = \frac{(\mu A_c)^2}{4} P_m,
$$

onde $P_m = \mathbb{E}\{m^2(t)\}$ é a potência média do sinal mensagem.

### 5.3. Potência Total:

$$
P_s = P_{\text{c}} + P_{\text{BL}} = \frac{A_c^2}{2} + \frac{(\mu A_c)^2}{4} P_m.
$$

> Observação: a portadora transporta **nenhuma informação**, mas consome grande parte da potência (geralmente > 80%).

---

## 6. Demodulação

### 6.1. **Demodulação por Envoltória (Envelope Detector)**

Quando $0 < \mu \leq 1$, é possível usar um **detector de envoltória**:

$$
|s(t)| = A_c|1 + \mu\,m(t)| \approx A_c (1 + \mu m(t)),
$$

caso não haja inversões de fase (evita $\mu > 1$).

### 6.2. **Demodulação Coerente**

Alternativamente, usa-se demodulação síncrona (como em DSB-SC):

$$
s(t)\cos(\omega_c t) \to \text{filtro PB} \Rightarrow \frac{A_c \mu}{2} m(t).
$$

---

## 7. Eficiência de Potência

Define-se a eficiência como:

$$
\eta = \frac{P_{\text{BL}}}{P_s} = \frac{\mu^2 P_m}{\mu^2 P_m + 2}.
$$

* Valor máximo quando $\mu = 1$:

$$
\eta_{\max} = \frac{P_m}{P_m + 2}.
$$

* Para $P_m = 1$, por exemplo: $\eta = \frac{1}{3} \approx 33\%$.
* Significa que no **máximo 1/3 da potência transmite informação**.


