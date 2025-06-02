# Modulação DSB-FC AM

## 1. Definição da Modulação DSB-FC AM (AM Convencional)

A modulação **DSB-FC AM (*Double Sideband – Full Carrier Amplitude Modulation*)**, também conhecida como **AM convencional**. Ela é uma extensão da DSB-SC, mas inclui a portadora no sinal transmitido.

A **modulação DSB-FC AM** consiste em **modular a amplitude** de uma portadora senoidal de frequência $f_c$ com base em um sinal mensagem $m(t)$. O sinal resultante contém:

* a **portadora não suprimida**,
* e as **duas bandas laterais (inferior e superior)** com a informação do sinal mensagem.

---

## 2. Definições e Hipóteses

$$
s_{BSB-FC}(t) := A_c [1 + k_a m(t)]\cos (\omega_c t\, +\, \phi_c)
$$

* $m(t) \in \mathbb{R}$: sinal mensagem, limitado em banda $B$ e com valor médio nulo (sem componente DC);
* $|k_a m(t)| \leq 1$;
* $A_c > 0$: amplitude da portadora;
* $f_c \gg B$: frequência da portadora muito maior que a largura de banda da mensagem;
* $k_a \in [0,1]$: constante de sensibilidade de amplitude.

---

## 3. Expressão no Domínio do Tempo

A modulação DSB-FC é definida como:

$$
s(t) := \mathcal{M}_{\mathrm{DSB\text{-}FC}}\{m(t)\} = A_c[1 + k_a\, m(t)] \cos(\omega_c t),
$$

onde $\omega_c = 2\pi f_c$.

### 3.1 Índice de Modulação

$$
    \mu := k_a m_p,\, m_p = \max(|m(t)|) 
$$

* $\mu = 0$: só a portadora.
* $\mu < 1$: Submodulação
* $\mu = 1$: modulação máxima sem distorção (evita *overmodulation*).
* $\mu > 1$: *overmodulation* (supermodulação), causa distorção na demodulação envelope.

Na maioria das vezes, m(t) é normalizado, de forma com que $\max(|m(t)|]) = 1 \Rightarrow m_p = 1$.

### 3.2 Mensagem normalizada

Chamamos um sinal mensagem de normalizado:

$$
    m_n(t) = \frac{m(t)}{\max(|m(t)|)}
$$

* Neste caso, a constante de sensibilidade será igual ao índice de modulação: $m_p = 1\, \Rightarrow\, \mu = k_a$

---

## 4. Representação no Domínio da Frequência

Seja $M(f)$ a transformada de Fourier de $m(t)$, então:

$$
S(f) = \frac{A_c}{2} \left[ \delta(f - f_c) + \delta(f + f_c) \right] 
+ \frac{k_a A_c}{2} \left[ M(f - f_c) + M(f + f_c) \right].
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
P_{b} = \frac{(k_a A_c)^2}{2} P_m = \frac{(\frac{\mu}{m_p} A_c)^2}{2},
$$

onde $P_m = \mathbb{E}\{m^2(t)\}$ é a potência média do sinal mensagem.

### 5.3. Potência Total:

$$
P_s = P_{\text{c}} + P_{b} = \frac{A_c^2}{2} + \frac{(k_a A_c)^2}{2} P_m = \frac{A_c^2}{2}[1 + k_aP_m] = \frac{A_c^2}{2}[1 + \frac{\mu}{m_p}P_m].
$$

> Observação: a portadora transporta **nenhuma informação**, mas consome grande parte da potência (geralmente > 80%).

---

## 6. Demodulação

### 6.1. **Demodulação por Envoltória (Envelope Detector)**

Quando $0 < \mu \leq 1$, é possível usar um **detector de envoltória**:

$$
|s(t)| = A_c|1 + k_a\,m(t)| \approx A_c (1 + k_a m(t)),
$$

caso não haja inversões de fase (evita $\mu > 1$).

### 6.2. **Demodulação Coerente**

Alternativamente, usa-se demodulação síncrona (como em DSB-SC):

$$
s(t)\cos(\omega_c t) \to \text{filtro LP} \Rightarrow \frac{k_aA_c}{2} m(t).
$$

---

## 7. Eficiência de Potência

Define-se a eficiência como:

$$
\eta = \frac{P_{\text{b}}}{P_s}\, =\, \frac{k_a^2 P_m}{1 + k_a P_m}\, =\, \frac{(\frac{\mu}{m_p})^2P_m}{1+ (\frac{\mu}{m_p})^2P_m}.
$$

* Como para que não haja perda de informação $\mu \le 1$, temos a potência máxima para uma mensagem normalizada $m_n(t)$ quando $\mu = 1$:

$$
    \eta_{\max} = \frac{P_m}{P_m + 1}.
$$

* Para $m(t) = cos(\omega_m t) \Rightarrow P_m = \frac{1}{2}$, e portanto: $\eta = \frac{1}{3} \approx 33\%$.
