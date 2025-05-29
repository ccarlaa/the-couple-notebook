# Modulação

A modulação é o processo matemático pelo qual uma “forma de onda” transportadora (portadora) é alterada em suas características (amplitude, frequência ou fase) de acordo com um sinal informativo (mensagem), de modo a permitir sua transmissão eficiente por um meio de comunicação passabanda. 

---

## 1. Sinais de referência

* **Sinal mensagem (base‐band)**: $m(t)$, onde $t\in\mathbb{R}$.
* **Portadora**:

  $$
    c(t) = A_c \cos\bigl(\omega_c t + \phi_c\bigr)
    \quad\text{com}\quad
    \omega_c = 2\pi f_c,
  $$

  em que

  * $A_c > 0$ é a amplitude da portadora,
  * $f_c$ sua frequência em Hz,
  * $\phi_c$ sua fase inicial em radianos.

---

## 2. Definição geral de modulação

Formalmente, a modulação é um operador $\mathcal{M}$ que, a partir de $m(t)$ e $c(t)$, gera o sinal modulado $s(t)$:

$$
  s(t) \;=\; \mathcal{M}\bigl\{\,m(t),\,c(t)\bigr\}.
$$

Esse operador costuma ser projetado para que $s(t)$ ocupe banda centrada em ±$f_c$ em vez de banda-base (abaixo de $B$), permitindo uso de antenas e canais passabanda.

### Descrito em texto:

A modulação é, em termos formais, um **operador** $\mathcal{M}$ que transforma um sinal de banda-baixa $m(t)$ em um sinal de banda-passante $s(t)$ por meio de alterações na amplitude, frequência ou fase de uma portadora $c(t)$. Cada esquema de modulação (AM, FM, PM, DSB-SC, e digital) tem sua fórmula específica, que define explicitamente como $s(t)$ depende de $m(t)$ e dos parâmetros do sistema.

---

## 3. Representação em Domínio Complexo (Sinal de Banda-Passante)

Define‐se o **sinal complexo equivalente**:

$$
  u(t) = a(t)\,e^{j\theta(t)},
$$

onde $a(t)$ e $\theta(t)$ capturam a variação de amplitude e fase conforme o tipo de modulação. O sinal transmitido real é então

$$
  s(t) = \Re\bigl\{u(t)\,e^{j\omega_c t}\bigr\}.
$$

* **AM clássica**: $u(t) = A_c + m(t)$.
* **DSB-SC**: $u(t) = m(t)$.
* **FM/PM**: $u(t) = A_c\,e^{j\,k_f\!\int m + j\phi_0}$ ou $u(t) = A_c\,e^{j\,k_p m(t) + j\phi_0}$.

---

## 4. Critérios e métricas

1. **Eficiência espectral** $\displaystyle \eta = \frac{R_b}{B}$ (bits/s por Hz) – importante em modulações digitais.
2. **Razão sinal-ruído (SNR)** no receptor: afeta desempenho de detecção.
3. **Índice de modulação** ($\mu$, $\Delta f$, etc.) – garante qualidade sem distorção.

---

## 5. Extensões a modulação digital

Embora a definição acima cubra modulação analógica, digitalmente fala-se de constelações complexas:

$$
  s[n] = \Re\bigl\{\,a_k\,e^{j\omega_c nT_s}\bigr\},\quad a_k\in\mathcal{S},
$$

onde $\mathcal{S}$ é o conjunto de símbolos (e.g. QPSK, QAM), $T_s$ a duração de símbolo.

---
