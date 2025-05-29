**Definição Formal Completa — Modulação SSB-AM (Single Sideband Amplitude Modulation)**

---

### 1. Descrição Geral

A **modulação SSB-AM** consiste em transmitir apenas **uma única banda lateral** (inferior ou superior) do espectro produzido por uma modulação DSB, suprimindo tanto a portadora quanto a banda lateral redundante. Isso reduz pela metade a largura de banda e concentra toda a potência útil em uma das bandas laterais.

---

### 2. Sinal Mensagem e Portadora

* $m(t)$: sinal mensagem real, limitado em banda a $B$, com transformada $M(f)$ nula para $|f|>B$.
* $c(t) = A_c\cos(\omega_c t)$: portadora de amplitude $A_c$ e frequência angular $\omega_c = 2\pi f_c$, com $f_c\gg B$.

---

### 3. Sinal Analítico de Banda-Base

Define-se o **sinal analítico** de $m(t)$:

$$
m_a(t) = m(t) + j\,\hat{m}(t),
$$

onde $\hat{m}(t)$ é a transformada de Hilbert de $m(t)$.

---

### 4. Expressão no Domínio do Tempo

* **Banda Lateral Superior (SSB-USB)**:

  $$
    s_{\rm USB}(t)
    = \Re\bigl\{m_a(t)\,e^{j\omega_c t}\bigr\}
    = m(t)\cos(\omega_c t) - \hat{m}(t)\sin(\omega_c t).
  $$
* **Banda Lateral Inferior (SSB-LSB)**:

  $$
    s_{\rm LSB}(t)
    = \Re\bigl\{m_a^*(t)\,e^{j\omega_c t}\bigr\}
    = m(t)\cos(\omega_c t) + \hat{m}(t)\sin(\omega_c t).
  $$

---

### 5. Representação no Domínio da Frequência

* Para USB, o espectro é

  $$
    S_{\rm USB}(f) =
    \begin{cases}
      M(f - f_c), & f > 0,\\
      0, & f \le 0.
    \end{cases}
  $$
* Para LSB,

  $$
    S_{\rm LSB}(f) =
    \begin{cases}
      0, & f \ge 0,\\
      M(f + f_c), & f < 0.
    \end{cases}
  $$

Em ambas, não há componente em $\pm f_c$ de portadora.

---

### 6. Potência do Sinal

Assumindo $m(t)$ estacionário com potência média $P_m = \mathbb{E}\{m^2(t)\}$ e $A_c = 1$ para normalização:

$$
P_{\rm SSB} = \mathbb{E}\{s_{\rm USB}^2(t)\}
= \mathbb{E}\{\bigl[m(t)\cos(\omega_c t) - \hat{m}(t)\sin(\omega_c t)\bigr]^2\}
= P_m.
$$

Ou seja, toda a potência do sinal SSB é igual à potência do sinal original em banda-base.

---

### 7. Demodulação Coerente

Para recuperação de $m(t)$, utiliza-se um oscilador local em fase com a portadora:

1. Multiplica-se $s_{\rm USB/LSB}(t)$ por $\cos(\omega_c t)$ e $\sin(\omega_c t)$.
2. Passa-se cada produto por filtro passa-baixa para obter:

   $$
   \begin{cases}
     m(t) = \text{LP}\{2\,s(t)\cos(\omega_c t)\},\\
     \hat{m}(t) = -\text{LP}\{2\,s(t)\sin(\omega_c t)\}.
   \end{cases}
   $$
3. Reconstrói-se $m(t)$ a partir de $m(t)$ e $\hat{m}(t)$, se necessário.

---

Esta formulação mostra explicitamente como a SSB-AM gera e recupera o sinal usando apenas uma das bandas laterais, sem portadora, otimizando largura de banda e potência transmitida.
