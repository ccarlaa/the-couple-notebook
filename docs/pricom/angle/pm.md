**Modulação em Fase (PM) – Definição Formal, Potência e Características Espectrais**

A seguir apresento uma descrição detalhada e formal da modulação em fase (PM), incluindo (1) a forma geral de s(t) para um sinal modulante arbitrário m(t), (2) o cálculo de potência média do sinal modulado e (3) as principais características espectrais, tanto para o caso geral quanto para o caso de modulação sinusoidal.

---

## 1. Definição Formal de PM para um sinal $m(t)$ arbitrário

1. **Sinal Portadora**

   * Seja

     $$
       c(t) \;=\; A_c \cos\bigl(\omega_c t\bigr)
     $$

     onde

     * $A_c$ é a amplitude (constante) da portadora;
     * $\omega_c = 2\pi f_c$ é a frequência angular da portadora.

2. **Sinal Modulante**

   * Denotamos por $m(t)$ o sinal de informação (ou modulante), que pode ser arbitrário (analógico ou digital), com variações em tempo contínuo.
   * Assumimos que $m(t)$ é limitado em amplitude, isto é, existe $M_{\max}$ tal que $\lvert m(t)\rvert \le M_{\max}$, para todos os $t$.

3. **Índice de Modulação de Fase**

   * Introduzimos a constante $k_p$ (ou, às vezes, $\Delta\theta$) como coeficiente de sensibilidade de fase, de modo que a variação instantânea de fase seja proporcional a $m(t)$.
   * Unidade de $k_p$: radianos por unidade de amplitude de $m(t)$.
   * Define-se o **índice de modulação de fase** como

     $$
       \beta_p \;=\; k_p \, M_{\max}.
     $$

     (Em caso de m(t) sinusoidal de amplitude $A_m$, usa‐se $\beta_p = k_p\,A_m$.)

4. **Fase Instantânea**

   * A fase instantânea $\varphi(t)$ do sinal modulado em fase é dada por

     $$
       \varphi_{\text{PM}}(t)
       \;=\; \omega_c\,t \;+\; k_p\,m(t).
     $$
   * Observação: toda variação de fase é relativa à fase “não modulada” $\omega_c t$.

5. **Sinal Modulado em Fase**

   * O sinal modulado em fase (PM) é, então,

     $$
       s_{\text{PM}}(t)
       \;=\; A_c \,\cos\!\bigl(\varphi_{\text{PM}}(t)\bigr)
       \;=\; A_c \,\cos\bigl(\omega_c\,t \;+\; k_p\,m(t)\bigr).
     $$
   * **Observação**:

     * Ao contrário da modulação em amplitude (AM), aqui a amplitude de $s_{\text{PM}}(t)$ permanece constante igual a $A_c$.
     * Todo o “conteúdo de informação” é embutido na fase instantânea através de $k_p\,m(t)$.

6. **Frequência Instantânea**

   * A frequência instantânea $\omega_i(t)$ do sinal PM obtém‐se derivando a fase:

     $$
       \omega_i(t)
       \;=\; \frac{d}{dt}\bigl[\varphi_{\text{PM}}(t)\bigr]
       \;=\; \omega_c \;+\; k_p \,\frac{d\,m(t)}{dt}.
     $$
   * Em termos de frequência ($f_i = \omega_i/2\pi$):

     $$
       f_i(t)
       \;=\; f_c \;+\; \frac{k_p}{2\pi}\,\frac{d\,m(t)}{dt}.
     $$
   * Logo, mesmo na modulação em fase, a frequência instantânea “flutua” em função da derivada de $m(t)$.

---

## 2. Cálculo da Potência Média de $s_{\text{PM}}(t)$

1. **Sinal PM de Amplitude Constante**

   * Como $s_{\text{PM}}(t) = A_c \cos\bigl(\omega_c t + k_p m(t)\bigr)$ $\Rightarrow$ amplitude fixa igual a $A_c$ para todo $t$.

2. **Potência Instantânea**

   * A potência instantânea (assumindo carga de $1\ \Omega$ para simplificar) é

     $$
       p(t) \;=\; [\,s_{\text{PM}}(t)\,]^2 
       \;=\; A_c^2\,\cos^2\bigl(\omega_c t + k_p\,m(t)\bigr).
     $$

3. **Potência Média**

   * Em regime estacionário, a potência média $P_{\text{PM}}$ é calculada como a média temporal de $p(t)$.
   * Para qualquer função $\theta(t)$, a média de $\cos^2[\theta(t)]$ ao longo de “várias” oscilações em torno de $\omega_c$ é $1/2$. Isso vale mesmo que $\theta(t)$ varie lentamente (idealmente, sabemos que $\varphi_{\text{PM}}(t)$ está “dominada” pela componente $\omega_c t$).
   * Portanto:

     $$
       P_{\text{PM}}
       \;=\; \langle \,A_c^2\,\cos^2(\omega_c t + k_p\,m(t))\,\rangle 
       \;=\; A_c^2 \,\left\langle \cos^2(\cdot)\right\rangle 
       \;=\; A_c^2 \,\frac{1}{2}
       \;=\; \frac{A_c^2}{2}.
     $$
   * **Comentário**:

     * Como a amplitude é mantida constante, a potência média não depende de $m(t)$ nem de $k_p$.
     * Se a carga fosse $R$ em vez de $1\,\Omega$, usaríamos $\tfrac{A_c^2}{2R}$.

---

## 3. Características Espectrais de $s_{\text{PM}}(t)$

### 3.1 Caso Geral (Sinal $m(t)$ Arbitrário)

* Para um modulante completamente arbitrário, o sinal $s_{\text{PM}}(t)$ tem espectro “contínuo” em torno de $f_c$, pois a fase é afetada por $m(t)$.
* A transformada de Fourier de $s_{\text{PM}}(t)$ pode ser escrita, formalmente, como

  $$
    S_{\text{PM}}(f)
    \;=\; \mathcal{F}\Bigl\{A_c \cos(\omega_c t + k_p\,m(t))\Bigr\}\,,
  $$

  mas não há expressão fechada geral em termos de uma única função simples, exceto via **expansão por série de Fourier** (caso $m(t)$ seja periódico) ou **densidade espectral de potência** (caso seja aleatório ou senoidal composto).
* Em particular, o **espectro de potência** $S_{s}(f)$ (densidade espectral) dependerá da distribuição de frequências de $\exp\bigl[j\,k_p\,m(t)\bigr]$.

  * Se $m(t)$ for de banda limitada ou “lento” (comparado a $\omega_c$), pode‐se aplicar aproximações de banda estreita (narrowband PM); caso contrário, teremos uma **banda larga** (wideband PM) com espalhamento amplo.
* Um resultado geral (para $m(t)$ com densidade espectral $S_m(f)$) é que parte da energia do sinal PM “se espalha” formando lóbulos laterais em torno de $f_c$, cuja forma exata depende de $S_m(f)$ e de $k_p$. Em resumo:

  1. **Banda teórica infinita** (para qualquer sinal de informação que não seja estritamente de banda zero), pois qualquer fase que se modifica “desloca” energia fora da linha central.
  2. **Concentração espectral** em torno de $f_c$, cujo “peso” depende da taxa de variação de fase (i.e., do valor médio e variações de $\frac{d\,m(t)}{dt}$).

### 3.2 Caso Específico: Sinal Modulante Sinusoidal

Para ilustrar melhor e obter fórmulas fechadas, consideremos

$$
  m(t) \;=\; A_m\,\cos(\omega_m\,t), 
  \quad A_m \;\le\; M_{\max}.
$$

1. **Índice de Modulação**

   * Define‐se

     $$
       \beta_p \;=\; k_p \, A_m.
     $$
   * Em PM, o nome “índice de modulação” é $\beta_p$ (sem unidade).

2. **Sinal Modulado**

   $$
     s_{\text{PM}}(t)
     \;=\; A_c \,\cos\Bigl(\omega_c\,t \;+\; \beta_p\,\cos(\omega_m\,t)\Bigr).
   $$

3. **Expansão em Série de Bessel**
   Usando a identidade para $\cos\bigl(\alpha + \beta \cos x\bigr)$, temos:

   $$
     \cos\bigl(\omega_c t + \beta_p \cos(\omega_m t)\bigr)
     \;=\; 
     J_{0}(\beta_p)\,\cos(\omega_c t)
     \;+\;\sum_{n=1}^{\infty} 
     \Bigl[
       J_{n}(\beta_p)\,\cos\bigl((\omega_c + n\,\omega_m)\,t\bigr)
       \;+\;
       (-1)^n\,J_{n}(\beta_p)\,\cos\bigl((\omega_c - n\,\omega_m)\,t\bigr)
     \Bigr],
   $$

   em que $J_n(\,\cdot\,)$ é a n‐ésima função de Bessel de primeira espécie.

   * Portanto:

     $$
       s_{\text{PM}}(t)
       \;=\; A_c\,\Biggl[
         J_{0}(\beta_p)\,\cos(\omega_c t)
         \;+\;\sum_{n=1}^{\infty} 
         J_{n}(\beta_p)\,\cos\bigl((\omega_c + n\,\omega_m)\,t\bigr)
         \;+\;(-1)^n\,J_{n}(\beta_p)\,\cos\bigl((\omega_c - n\,\omega_m)\,t\bigr)
       \Biggr].
     $$
   * **Observações**:

     1. Os coeficientes $J_n(\beta_p)$ determinam a “contribuição” de cada componente espectral.
     2. O termo de frequência central $f_c$ tem amplitude $A_c\,J_0(\beta_p)$.
     3. Cada par de “lóbulos laterais” em $f_c \pm n\,f_m$ tem amplitude $A_c\,J_n(\beta_p)$.
     4. Quando $\beta_p \ll 1$ (caso **banda estreita** – narrowband PM), temos aproximadamente

        $$
          J_0(\beta_p) \approx 1,\quad
          J_1(\beta_p)\approx \frac{\beta_p}{2},\quad 
          J_n(\beta_p)\approx 0 \;\;(n\ge2).
        $$

        Logo:

        $$
          s_{\text{PM}}(t)
          \;\approx\; A_c\,\Bigl[\cos(\omega_c t) 
          \;-\; \frac{\beta_p}{2}\,\cos\bigl((\omega_c + \omega_m)\,t\bigr)
          \;+\; \frac{\beta_p}{2}\,\cos\bigl((\omega_c - \omega_m)\,t\bigr)\Bigr].
        $$

        Isso mostra que, para $\beta_p$ pequeno, só há dois “lóbulos” laterais (órbitas de $f_c \pm f_m$) junto à linha central.

4. **Desvio de Frequência Máximo ($\Delta f$)**

   * Embora estejamos em PM, costuma‐se definir o “desvio de frequência máximo” resultante da modulação em fase quando $m(t)$ é senoidal:

     $$
       \omega_i(t)
       \;=\; \omega_c \;+\; k_p\,\frac{d\,m(t)}{dt}
       \;=\; \omega_c \;-\; k_p\,A_m\,\omega_m\,\sin(\omega_m t).
     $$
   * Logo, a **frequência angular máxima de desvio** é

     $$
       \Delta\omega 
       \;=\; k_p\,A_m\,\omega_m,
     $$

     e, convertendo para Hz,

     $$
       \Delta f
       \;=\; \frac{\Delta\omega}{2\pi}
       \;=\; \frac{k_p\,A_m\,\omega_m}{2\pi}
       \;=\; \frac{\beta_p\,\omega_m}{2\pi}.
     $$

5. **Largura de Banda Aproximada (Regra de Carson)**

   * Apesar de não ser exata, a regra de Carson fornece uma boa estimativa da região de frequência onde está concentrada a maior parte da energia:

     $$
       B_\text{PM} 
       \;\approx\; 2\,(\Delta f + f_m)
       \;=\; 2\,\Bigl(\frac{\beta_p\,\omega_m}{2\pi} \;+\; f_m\Bigr) 
       \;=\; 2\,f_m\,\bigl(\beta_p + 1\bigr).
     $$
   * Isto é válido para $\beta_p \ge 1$. Para o caso de $\beta_p \ll 1$ (banda estreita), a largura efetiva aproxima‐se de $2\,f_m$.

---

## 4. Resumo das Principais Fórmulas

**1. Definição Geral (qualquer $m(t)$):**

$$
\begin{cases}
  s_{\text{PM}}(t) = A_c \,\cos\bigl(\omega_c\,t + k_p\,m(t)\bigr),\\
  P_{\text{PM}} = \displaystyle\frac{A_c^2}{2},\\
  \omega_i(t) = \omega_c + k_p\,\dfrac{d\,m(t)}{dt}.
\end{cases}
$$

**2. Caso $m(t) = A_m \cos(\omega_m t)$:**

* Índice de modulação: $\beta_p = k_p\, A_m$.
* Sinal modulado:

  $$
    s_{\text{PM}}(t) 
    = A_c\,\cos\bigl(\omega_c\,t + \beta_p\,\cos(\omega_m t)\bigr).
  $$
* Expansão em Bessel:

  $$
    s_{\text{PM}}(t)
    = A_c\,J_0(\beta_p)\,\cos(\omega_c t)
    \;+\;\sum_{n=1}^\infty A_c\,J_n(\beta_p)\,
    \Bigl[\cos\bigl((\omega_c + n\,\omega_m)\,t\bigr)
    \;+\;(-1)^n \cos\bigl((\omega_c - n\,\omega_m)\,t\bigr)\Bigr].
  $$
* Desvio de frequência máximo:

  $$
    \Delta f 
    = \frac{k_p\,A_m\,\omega_m}{2\pi} 
    = \frac{\beta_p\,\omega_m}{2\pi}.
  $$
* Largura de banda (aprox. de Carson):

  $$
    B_\text{PM} \approx 2\,\bigl(\Delta f + f_m\bigr) 
    = 2\,f_m\,\bigl(\beta_p + 1\bigr).
  $$

---

## 5. Observações Finais

1. **Potência**

   * A potência média de $s_{\text{PM}}(t)$ independe do índice $\beta_p$; continua sendo $\tfrac{A_c^2}{2}$.
   * Isto contrasta com AM: em AM a potência varia com o índice de modulação.

2. **Banda Estreita vs. Banda Larga**

   * **Narrowband PM** ($\beta_p \ll 1$):

     * Apenas lóbulos de primeira ordem em $f_c \pm f_m$ são significativos (coeficientes $J_1(\beta_p)\approx \beta_p/2$).
     * Largura aproximada: $2\,f_m$.
   * **Wideband PM** ($\beta_p \gtrsim 1$):

     * Aparecem lóbulos laterais de ordens mais altas, estendendo‐se até $f_c \pm n_{\max} f_m$, onde $J_n(\beta_p)$ ainda é significativo.
     * Largura aproximada dada pela regra de Carson: $2 f_m (\beta_p + 1)$.

3. **Para $m(t)$ Arbitrário (não senoidal)**

   * O espectro é “contínuo” em vez de composto por linhas discretas.
   * A densidade espectral pode ser obtida via método de Wiener‐Khintchine (para sinais estocásticos) ou via transformada de Fourier de $\exp\bigl[j\,k_p\,m(t)\bigr]$ se $m(t)$ for determinístico de banda limitada.
   * Em aplicações práticas, sempre considera‐se a “banda ocupada” aproximada por $2\bigl(\,\max\limits_t \bigl|\tfrac{d\,\varphi(t)}{dt}\bigr|/(2\pi)\bigr)$, o que equivale a $2\bigl(f_c ± \max\limits_t |f_i(t)−f_c|\bigr)$.

---

### Conclusão

* **Definição Formal de PM:**

  $$
    s_{\text{PM}}(t) = A_c \,\cos\bigl(\omega_c\,t + k_p\,m(t)\bigr),
    \quad 
    \omega_i(t) = \omega_c + k_p\,\frac{d\,m(t)}{dt}.
  $$
* **Potência Média:**

  $$
    P_{\text{PM}} = \frac{A_c^2}{2}.
  $$
* **Características Espectrais:**

  * Para $m(t)$ arbitrário: banda teórica infinita, mas grande parte da energia concentrada dentro de aproximadamente $2\bigl(\,\max_t |k_p\,\tfrac{d\,m(t)}{dt}|/(2\pi) + f_\text{banda}(m)\bigr)$.
  * Para $m(t)=A_m\cos(\omega_m t)$: espectro discreto em múltiplos de $\omega_m$ em torno de $\omega_c$, com coeficientes de Bessel $J_n(\beta_p)$ e largura aproximada $B_\text{PM} \approx 2\,f_m\,(\beta_p + 1)$.

Essas expressões formam a base completa para entender tanto o modelo de PM em tempo‐contínuo, seu consumo de potência e como se comporta seu espectro, seja em banda estreita ou larga.
