### Definição Formal Completa — Modulação DSB-SC AM

A **modulação DSB-SC AM** (*Double Sideband - Suppressed Carrier Amplitude Modulation*) é uma técnica de modulação linear na qual o sinal mensagem $m(t)$ é multiplicado diretamente pela portadora $c(t) = A_c \cos(\omega_c t)$, **sem** incluir a componente da portadora no sinal transmitido. Isso suprime a portadora e transmite apenas as duas bandas laterais (upper e lower sidebands), duplicando a eficiência de potência em relação à modulação AM convencional.

---

### 1. Definição formal do sinal modulado

Seja:

* $m(t) \in \mathbb{R}$: sinal mensagem, limitado em banda $B$, ou seja:

  $$
    \mathcal{F}\{m(t)\} = M(f) = 0 \quad \text{para } |f| > B.
  $$
* $c(t) = A_c \cos(\omega_c t)$: portadora, com $A_c > 0$, $\omega_c = 2\pi f_c$, e $f_c \gg B$.

Define-se o **sinal DSB-SC modulado** como:

$$
  s(t) = \mathcal{M}_{\mathrm{DSB\text{-}SC}}\{m(t)\} = A_c\,m(t)\cos(\omega_c t).
$$

---

### 2. Representação no domínio da frequência

Aplicando a Transformada de Fourier:

$$
  S(f) = \frac{A_c}{2} \left[ M(f - f_c) + M(f + f_c) \right],
$$

ou seja, a modulação DSB-SC desloca espectralmente $M(f)$ para as frequências $\pm f_c$, produzindo **duas bandas laterais simétricas**, sem a componente $\delta(f - f_c)$ da portadora (que aparece na AM convencional).

---

### 3. Representação usando sinal analítico

Usando a notação de sinal analítico $u(t) = m(t)$, o sinal transmitido pode ser descrito por:

$$
  s(t) = \Re\bigl\{ u(t)\,e^{j\omega_c t} \bigr\} = m(t)\cos(\omega_c t),
$$

ou seja, é a modulação em banda passante obtida a partir da multiplicação direta com a portadora.

---

### 4. Demodulação coerente (sincrônica)

Para recuperar $m(t)$, usa-se um detector coerente:

* Multiplica-se $s(t)$ novamente por $\cos(\omega_c t)$,
* E filtra-se o resultado com um filtro passa-baixa:

$$
  s(t) \cdot \cos(\omega_c t) = \frac{A_c}{2} m(t) \big[1 + \cos(2\omega_c t)\big],
$$

$$
  \Rightarrow \text{Filtro passa-baixa} \Rightarrow \frac{A_c}{2} m(t).
$$

---

### 5. Propriedades principais

* **Banda ocupada**: $2B$ Hz (dupla em relação à banda da mensagem).
* **Eficiência de potência**: 100% da potência vai para as bandas laterais.
* **Requer sincronismo** de fase e frequência no receptor para demodulação correta.
* **Não é possível demodular com detector de envoltória**, diferentemente da AM clássica.

---

Claro! Vamos estender a definição formal da **modulação DSB-SC AM** com uma análise rigorosa da **potência do sinal transmitido e recebido**.

---

### 6. Potência do sinal DSB-SC

#### 6.1. Potência Instantânea

O sinal modulado é:

$$
s(t) = A_c\,m(t)\cos(\omega_c t).
$$

A potência instantânea é:

$$
P(t) = [s(t)]^2 = A_c^2\,m^2(t)\cos^2(\omega_c t).
$$

---

#### 6.2. Potência Média

Assumindo que $m(t)$ é um sinal estacionário com potência média $P_m = \mathbb{E}\{m^2(t)\}$, e que $\cos^2(\omega_c t)$ tem média $\frac{1}{2}$, a **potência média do sinal modulado** é:

$$
P_s = \mathbb{E}\{s^2(t)\} = A_c^2\,\mathbb{E}\{m^2(t)\cos^2(\omega_c t)\}
= A_c^2\,P_m \cdot \frac{1}{2}.
$$

Portanto:

$$
\boxed{P_s = \frac{A_c^2}{2} P_m.}
$$

Essa potência representa **toda** a potência do sinal transmitido, já que não há portadora explícita (ao contrário da AM convencional, que consome potência adicional na portadora).

---

#### 6.3. Potência Recebida

Suponha que o sinal receba um atenuamento linear do canal, modelado por um fator de ganho $G \in (0, 1]$. Assim, o sinal recebido é:

$$
r(t) = \sqrt{G} \cdot s(t) = \sqrt{G} \cdot A_c\,m(t)\cos(\omega_c t),
$$

e a potência média recebida é:

$$
P_r = G \cdot P_s = \boxed{P_r = \frac{G A_c^2}{2} P_m.}
$$

---
