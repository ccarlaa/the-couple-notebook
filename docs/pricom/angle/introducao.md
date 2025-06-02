# Introdução a Modulação de Ângulo

A modulação de ângulo é uma técnica de modulação analógica na qual a fase de uma onda portadora senoidal é variada de acordo com o sinal de informação. Essa variação pode ocorrer de duas formas principais: pela **Modulação da Frequência (FM)** ou pela **Modulação da Fase (PM)**.

## Portadora

A forma geral de uma onda portadora modulada em ângulo é expressa por:

$$
    c(t) = A_c\cos(\omega_c t + \phi(t)),\; \omega_c = 2\pi f_c
$$

onde:

- $A_c$ é a amplitude da portadora;
- $\omega_c$ é a frequência ângular da portadora (em rads/s);
- $\phi(t)$ é a variação de fase introduzida pelo sinal modulante.

Na modulação de ângulo, a amplitude $A_c$ permanece constante, e a informação é transmitida por meio de variações na fase $\phi(t)$ da portadora.

## Fase instantânea

A fase instantânea do sinal da portadora será:

$$
    \theta(t) = \omega_c t + \phi(t)
$$

Esse conceito será utilizado para a modulação de fase (PM)

## Frequência instatânea

Os seguintes conceitos serão utilizados para a modulação em frequência:

### Frequência angular

A frequência angular instantânea da portadora será:

$$
    \frac{d}{dt}\theta(t) = \omega_c + \frac{d}{dt}\phi(t)
$$

### Frequência em Hz

A frequência instantânea em Hz:

$$
    \frac{d}{dt}\theta(t) = 2\pi f_c + 2\pi\frac{d}{dt}\phi(t)
$$