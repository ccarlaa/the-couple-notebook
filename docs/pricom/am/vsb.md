# VSB AM

---

### 1. Descrição Geral

A **modulação VSB-AM** (*Vestigial Sideband Amplitude Modulation*) é uma técnica que transmite:

* **uma banda lateral completa** (superior ou inferior),
* mais **uma pequena porção (vestígio)** da outra banda lateral.

Ela é usada principalmente quando:

* deseja-se reduzir a largura de banda em relação à DSB-AM,
* mas a geração ou demodulação da SSB-AM é complexa demais (como no caso de sinais com conteúdo espectral próximo da origem, ex: vídeo analógico).

---

### 2. Sinal Mensagem e Portadora

* $m(t)$: sinal mensagem real, limitado em banda $B$, com transformada $M(f)$;
* $c(t) = A_c\cos(\omega_c t)$: portadora de amplitude $A_c$, frequência $f_c \gg B$.

---

### 3. Geração do Sinal VSB

O sinal VSB é obtido aplicando um filtro de vestígio ao sinal DSB, que mantém:

* uma **banda lateral inteira** (ex: superior),
* e um **vestígio gradual** da banda oposta (ex: parte da inferior).

$$
S_{\rm VSB}(f) = H_{\rm VSB}(f) \cdot S_{\rm DSB}(f),
$$

onde $H_{\rm VSB}(f)$ é a resposta em frequência do **filtro vestigial**, e $S_{\rm DSB}(f)$ é o espectro DSB (sem portadora):

$$
S_{\rm DSB}(f) = \frac{A_c}{2}\left[M(f - f_c) + M(f + f_c)\right].
$$

---

### 4. Características do Filtro Vestigial $H_{\rm VSB}(f)$

Esse filtro é projetado com:

* Banda lateral **inteira** (ex: $f > f_c + B$) com ganho unitário;
* Região de **transição gradual** (ex: $f_c - B < f < f_c + B$) com ganho variando suavemente;
* Banda lateral oposta **atenuada**, mas não totalmente suprimida;
* **Simetria apropriada** para possibilitar demodulação coerente.

---

### 5. Expressão no Domínio do Tempo

Não há expressão analítica simples como nas outras modulações. O sinal modulado VSB é, em geral:

$$
s(t) = \mathcal{F}^{-1}\{S_{\rm VSB}(f)\},
$$

onde $\mathcal{F}^{-1}$ denota a transformada de Fourier inversa.

---

### 6. Potência do Sinal

A potência do sinal VSB depende do filtro vestigial aplicado e da potência $P_m = \mathbb{E}\{m^2(t)\}$ do sinal mensagem. Como há supressão parcial de uma banda lateral:

$$
P_{\rm VSB} = \alpha P_m,
$$

com $0.5 < \alpha < 1$, dependendo do grau de vestígio mantido. Por exemplo, um vestígio de 25% da banda inferior resulta em $\alpha \approx 0.75$.

A portadora pode ser **suprimida** (como em DSB-SC) ou **transmitida com pequena amplitude**, permitindo **demodulação por detector de envoltória**, se desejado.

---

### 7. Demodulação

A VSB pode ser demodulada por:

#### a) **Demodulação coerente**:

Multiplica-se $s(t)$ por $\cos(\omega_c t)$, e aplica-se um filtro passa-baixa compensando o efeito do filtro vestigial original.

Esse filtro compensador tem resposta:

$$
H_{\text{rec}}(f) = H_{\rm VSB}(f - f_c) + H_{\rm VSB}(-f - f_c).
$$

Se $H_{\text{rec}}(f) = 1$, a mensagem é recuperada sem distorção.

#### b) **Detector de envoltória** (caso portadora esteja presente):

Se $s(t) = [1 + \mu m(t)]\cos(\omega_c t)$ com $\mu \le 1$, o detector de envoltória pode recuperar $m(t)$ com distorção pequena, desde que o vestígio seja projetado adequadamente.

---

Essa modulação é usada, por exemplo, no sistema **NTSC de televisão analógica**, onde a portadora de vídeo é modulada em VSB para economia de banda e facilidade de demodulação.
