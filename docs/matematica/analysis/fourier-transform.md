# Transformada de Fourier

## 1. Introdução

A Transformada de Fourier também foi introduzida por Jean-Baptiste Joseph Fourier em seu trabalho seminal *Théorie analytique de la chaleur (1822)*. Joseph Fourier, após o desenvolvimento da sua [série](fourier-series.md), decidiu estender a ideia de decompor um sinal em função de seus componentes de frequência para funções aperiódicas. Tornou-se, assim, possível a análise de funções não periódicas no domínio da frequência.

---

## 2. Definição 

A Transformada de Fourier contínua bilateral pode ser vista como um operador linear

$$
\mathcal{F} : L^1(\mathbb{R}) \;\to\; C_0(\mathbb{R})
$$

definido por:

$$
\mathcal{F}\{f\}(\omega)
\;:=\;
\int_{-\infty}^{+\infty} f(t)\,e^{-j\,\omega\,t}\,\mathrm{d}t,
$$

ou também:

$$
F(\omega)
\;:=\;
\int_{-\infty}^{+\infty} f(t)\,e^{-j\,\omega\,t}\,\mathrm{d}t,
$$

onde

* $f : \mathbb{R}\to\mathbb{C}$ é a função‐sinal no domínio do tempo,
* $F : \mathbb{R}\to\mathbb{C}$ é sua representação no domínio da frequência angular $\omega\in\mathbb{R}$,
* $j = \sqrt{-1}$.

---

**Fórmula de inversão**
Sejam $f\in L^1(\mathbb{R})$ e $F=\mathcal{F}\{f\}$. Sob condições adicionais (por exemplo $f\in L^1\cap L^2$), vale

$$
f(t)
\;=\;
\mathcal{F}^{-1}\{F\}(t)
\;=\;
\frac{1}{2\pi}\,
\int_{-\infty}^{+\infty}
F(\omega)\,e^{+j\,\omega\,t}\,\mathrm{d}\omega.
$$

---

## 3. Outras convenções

1. **Frequência em hertz** $\xi$:

$$
F(\xi)
=\int_{-\infty}^{+\infty} f(t)\,e^{-j\,2\pi \xi t}\,\mathrm{d}t,
\quad
x(t)
=\int_{-\infty}^{+\infty} F(\xi)\,e^{+j\,2\pi \xi t}\,\mathrm{d}\xi.
$$

2. **Fatores de normalização**: às vezes se adotam $\tfrac{1}{\sqrt{2\pi}}$ em ambas as fórmulas.

---

## 4. Espaços funcionais e propriedades

### 1. **O domínio: $L^1(\mathbb{R})$**

Este é o **espaço das funções absolutamente integráveis** em $\mathbb{R}$:

$$
L^1(\mathbb{R}) = \left\{ f : \mathbb{R} \to \mathbb{C} \;\middle|\; \int_{-\infty}^{+\infty} |f(t)|\,dt < \infty \right\}
$$

### 2. **O contradomínio: $C_0(\mathbb{R})$**

Esse é o espaço das **funções contínuas que tendem a zero no infinito**:

$$
C_0(\mathbb{R}) = \left\{ F : \mathbb{R} \to \mathbb{C} \;\middle|\; F \text{ é contínua e } \lim_{|\omega|\to\infty} F(\omega) = 0 \right\}
$$

### 3. **Teorema de Riemann–Lebesgue**

Este teorema afirma que:

> Se $x \in L^1(\mathbb{R})$, então sua transformada de Fourier $X(\omega)$ **existe** e **tende a zero** quando $|\omega| \to \infty$.

Formalmente:

$$
x \in L^1(\mathbb{R}) \;\Rightarrow\; \lim_{|\omega|\to\infty} \int_{-\infty}^{\infty} x(t)\,e^{-j\omega t} dt = 0
$$

### 4. **Teorema de Plancherel**
Se $f\in L^2(\mathbb{R})$, a transformada é estendida como operador unitário em $L^2$, **preservando energia**. Em termos formais:

Seja $\mathcal{F}$ o operador de Transformada de Fourier, definido inicialmente para funções $f \in L^1(\mathbb{R}) \cap L^2(\mathbb{R})$ por:

$$
\mathcal{F}\{f\}(\omega) = \int_{-\infty}^{\infty} f(t)\,e^{-j\omega t}\,dt,
$$

então, existe uma **extensão única** e **unitária** de $\mathcal{F}$ para todo $L^2(\mathbb{R})$, denotada também por $\mathcal{F}: L^2(\mathbb{R}) \to L^2(\mathbb{R})$, tal que:

$$
\boxed{
\forall f \in L^2(\mathbb{R}), \quad
\|\mathcal{F}\{f\}\|_{L^2(\mathbb{R})} = \|f\|_{L^2(\mathbb{R})}
}
$$

Em termos de produto interno, o teorema afirma:

$$
\boxed{
\forall f, g \in L^2(\mathbb{R}), \quad
\langle \mathcal{F}\{f\}, \mathcal{F}\{g\} \rangle_{L^2}
=
\langle f, g \rangle_{L^2}
}
$$

---

## 5. Desenvolvimento

Tendo em vista a [Série de Fourier](fourier-series.md) em sua forma exponencial, temos:

$$
c_n = \frac{1}{2T}\int_{-T}^{T} f(t)\,e^{-jn\omega_0 t}\,dt,
\qquad n\in\mathbb{Z}.
$$

$$
f(t) = \sum_{n=-\infty}^{\infty} c_n\,e^{jn\omega_0 t}.
$$

com $f$ com período $P = 2T$ e $\omega_0 = \frac{2\pi}{P}$.

Vamos reorganizar um pouco essa equação para usarmos $\Delta\omega_n$, onde $\omega_n = \frac{2\pi n}{P}$.

$$
\Delta\omega =\frac{2\pi (n+1)}{P} - \frac{2\pi n}{P} \quad \Rightarrow \quad \Delta\omega = \frac{2\pi}{P} = \omega_0
$$

Fourier, quando desenvolveu a Transformada, assumiu as funções aperiódicas como funções de período infinito, $P \rightarrow \infty$. Ou seja, para a transformada, queremos decompor uma função $f$, ao invés de em $n$ frequências discretas $n\omega_0$, queremos que a função seja decomposta em todas as possíveis frequências. Portanto, $\omega_0 \rightarrow 0$. Substituindo na formula:

$$
P = \frac{2\pi}{\Delta\omega}
$$

$$
f(t) = \lim_{P \rightarrow \infty} \sum_{n=-\infty}^{\infty} \frac{1}{P}\int_{-T}^{T} f(t)\,e^{-j\omega t}\,dt\,e^{j\omega t} = \lim_{P \rightarrow \infty} \sum_{n=-\infty}^{\infty} \frac{\Delta\omega}{2\pi}\int_{-T}^{T} f(t)\,e^{-j\omega t}\,dt\,e^{jn\omega_0 t}
$$

$$
\therefore\, f(t) = \lim_{P \rightarrow \infty} \sum_{n=-\infty}^{\infty} \frac{1}{2\pi}\int_{-T}^{T} f(t)\,e^{-j\omega t}\,dt\,e^{j\omega t} \Delta\omega
$$

$$
\therefore\, 
    f(t) = \frac{1}{2\pi}\, \int_{-\infty}^{\infty} \bigl[\int_{-\infty}^{\infty} f(t)\,e^{-j\omega t}\,dt \bigl]\, e^{j\omega t}\,dt
$$

$$
\Rightarrow \boxed{
    F(\omega) = \int_{-\infty}^{\infty} f(t)\,e^{-j\omega t}\,dt 
}
$$


