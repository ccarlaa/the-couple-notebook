# Série de Fourier

## Um pouco de história

A série de Fourier surgiu no início do século XIX, quando o matemático francês Joseph Fourier buscava compreender a propagação do calor em corpos sólidos. Em 1807, ele apresentou à Academia Francesa seu trabalho "Mémoire sur la propagation de la chaleur dans les corps solides", no qual propôs que qualquer função periódica poderia ser expressa como uma soma infinita de senos e cossenos — o que hoje conhecemos como série de Fourier. 

---

## 1. Resumo
Uma **série de Fourier** expressa uma função periódica $f$ como uma soma de funções trigonométricas ou fasores. Assim, qualquer forma de onda ou função periódica — desde sinais elétricos até vibrações mecânicas — pode ser “decomposta” em **harmônicos puros**, o que é fundamental em Análise de Sinais, Física e Engenharia.

## 2. Contexto e Espaço Funcional

Seja $f\colon \mathbb{R}\to\mathbb{R}$ (ou $\mathbb{C}$) **periódica** de período $P=2T$, isto é,

$$
f(t + 2T) = f(t)\quad\forall t\in\mathbb{R}.
$$

Suponha que $f$ satisfaça as **condições de Dirichlet** em um período (por exemplo, seja de classe $C^1$ por partes). Então $f$ pertence ao espaço $L^2([-T,T])$ ou ao espaço das funções de quadrado-integrável em $[-T,T]$.

No espaço de Hilbert $\bigl(L^2([-T,T]),\langle\cdot,\cdot\rangle\bigr)$, tomamos o **produto interno**

$$
\langle g, h\rangle \;=\;\int_{-T}^{T} g(x)\,\overline{h(x)}\,dt
$$

e a norma associada $\|g\|^2=\langle g,g\rangle$.

As funções

$$
1,\quad \cos(n \omega t),\quad \sin(n\omega t)\quad \text{com}\;\; (n=1,2,3,\dots)
$$

formam um **sistema ortogonal** em $L^2([-T,T])$.

---

## 3. Forma Trigonométrica da Série de Fourier

Para $f$ periódico de período $P=2T$, definimos os **coeficientes**:

$$
\begin{aligned}
a_0 &= \frac{1}{T}\int_{-T}^{T} f(t)\,dt,\\
a_n &= \frac{1}{T}\int_{-T}^{T} f(t)\,\cos(n\omega t)\,dt,\quad n\ge1,\\
b_n &= \frac{1}{T}\int_{-T}^{T} f(t)\,\sin(n\omega t)\,dt,\quad n\ge1.
\end{aligned}
$$

A **série de Fourier** de $f$ é então:

$$
\boxed{
f(t)\sim \frac{a_0}{2}
\;+\;\sum_{n=1}^{\infty}\bigl[a_n\cos(n\omega t)+b_n\sin(n\omega t)\bigr].
}
$$

— Aqui “$\sim$” indica que a série converge (em norma $L^2$, ponto a ponto ou uniformemente, conforme hipóteses adicionais) para $f$ ou para $\bigl(f(x^+)+f(x^-)\bigr)/2$ se houver descontinuidades.

## 4. Forma Exponencial (Complexa)

Em vez de seno e cosseno, usa-se a base completa de exponenciais:

$$
e^{jn\omega t},\quad n\in\mathbb{Z},
$$

ortogonais em $L^2([-T,T])$. Definem‑se

$$
c_n = \frac{1}{2T}\int_{-T}^{T} f(t)\,e^{-jn\omega t}\,dt,
\qquad n\in\mathbb{Z}.
$$

A **série de Fourier complexa** é:

$$
\boxed{
f(t)\sim \sum_{n=-\infty}^{\infty} c_n\,e^{jn\omega t}.
}
$$

Relação com a forma trigonométrica:

$$
c_0 = \frac{a_0}{2},\quad
c_n = \frac{a_n - j\,b_n}{2},\quad
c_{-n} = \frac{a_n + j\,b_n}{2}.
$$

---

## 5. Teoremas de Convergência

* **Convergência em $L^2$**: Se $f\in L^2([-T,T])$, então sua série de Fourier converge para $f$ em norma $L^2$.

* **Convergência pontual** (Dirichlet): Se $f$ é periódica e com número finito de descontinuidades e de máximos/minimos por período, então para todo $t$,

  $$
  S_N(t)
  := \frac{a_0}{2} + \sum_{n=1}^N [a_n\cos(n\omega t)+b_n\sin(n\omega t)]
  \;\longrightarrow\;
  \frac{f(t^+)+f(t^-)}{2}
  \quad(N\to\infty).
  $$

* **Convergência uniforme**: Se $f$ é contínua e de classe Lipschitz ou com derivada contínua, a convergência é uniforme.

---

## 6. Desenvolvimento

Seja $f(t)$ uma função periódica de período $P=2T$, assumamos que ela pode ser representada por um soma de funções periódicas ortogonais entre si. Em outras palavras, $f(t)$ pode ser projetada em bases periódicas ortogonais. Para este caso, utilizemos as seguintes bases:

$$
\boxed{\;\cos(n \omega t),\quad \sin(n\omega t), \quad 1\;}\quad \text{com}\;\; (n=1,2,3,\dots)
$$

Portanto:

$$
f(t) \sim \sum_{n=0}^\infty \bigl[a_n\cos(n\omega t)+b_n\sin(n\omega t)\bigr]
$$

Agora precisamos descobrir quais os valores de $a_n$ e $b_n$, portanto, vamos projetar a função em cada uma das bases

1. Base $1$:
$$
\langle f, 1\rangle \;=\;\int_{-T}^{T} f(t)\,\overline{1}\,dt
$$
$$
\therefore \int_{-T}^{T} f(t)\,dt = \int_{-T}^{T} \sum_{n=0}^\infty \bigl[a_n\cos(n\omega t)+b_n\sin(n\omega t)\bigr]\,dt = \int_{-T}^{T} a_0\,dt 
$$
$$
\text{Tendo em vista que:} \quad \forall n>0,\;\int_{-T}^{T} \cos(n\omega t)\,dt = \int_{-T}^{T} \sin(n\omega t)\,dt = 0
$$
$$
\therefore \int_{-T}^{T} f(t)\,dt = a_0 \cdot 2T \Rightarrow \boxed{2\cdot a_0 = \frac{1}{T}\int_{-T}^{T} f(t)\,dt}
$$

2. Base $\cos(n\omega t)$:

Assumamos uma base $\cos(m\omega t)$:
$$
\langle f, \cos(m\omega t)\rangle \;=\;\int_{-T}^{T} f(t)\,\overline{\cos(m\omega t)}\,dt
$$
$$
\therefore \int_{-T}^{T} f(t)\,\cos(m\omega t)\,dt = \frac{a_0}{2}\; +\; \sum_{n=1}^{\infty}\; \bigl[ a_n \int_{-T}^{T} \cos(n\omega t)\cos(m\omega t)\, dt\; +\; b_n \int_{-T}^{T} \sin(n\omega t)\cos(m\omega t)\, dt \bigr]
$$
$$
\text{Como }\cos(n\omega t)\, \text{é uma base ortogonal: }\; \int_{-T}^{T} \cos(n\omega t)\cos(m\omega t)\, dt = T\cdot\delta_{nm}, \quad\delta_{ij} = 
\begin{cases}
1 & \text{if } i = j, \\
0 & \text{if } i \ne j.
\end{cases}
$$
$$
\therefore \int_{-T}^{T} f(t)\,\cos(m\omega t)\,dt\; = \; a_n \cdot 1 \Rightarrow \boxed{a_n\, =\, \frac{1}{T}\int_{-T}^{T} f(t)\,\cos(n\omega t)\,dt}
$$
3. Por fim, para base $\sin(n\omega t)$ usamos a mesma lógica anterior:
$$
\langle f, \sin(m\omega t)\rangle \;=\;\int_{-T}^{T} f(t)\,\overline{\sin(m\omega t)}\,dt
$$
$$
\Rightarrow \boxed{b_n\, =\, \frac{1}{T}\int_{-T}^{T} f(t)\,\sin(n\omega t)\,dt}
$$

### Síntese:

E assim chegamos ao valor de cada um dos valores dos coeficientes da fórmula da série de Fourier descrita no ponto 3:

$$
f(t) = \frac{a_0}{2}
\;+\;\sum_{n=1}^{\infty}\bigl[a_n\cos(n\omega t)+b_n\sin(n\omega t)\bigr].
$$

E para chegarmos na sua forma **Exponencial** precisamos apenas substituir os senos e cossenos por suas fórmulas exponenciais e atribuir $n$ a todos os Inteiros:

$$
n \in \mathbb{Z}
$$

$$
\cos(n\omega t)\, =\, \frac{e^{jn\omega t} + e^{-jn\omega t}}{2} 
$$

$$
\sin(n\omega t)\, =\, \frac{e^{jn\omega t} - e^{-jn\omega t}}{2j}
$$

---

## 7. Exemplos

1. **Onda quadrada** de período $2T$:

   $$
   f(t) =
   \begin{cases}
   1, & 0<t<T,\\
   -1,& -T<t<0,
   \end{cases}
   $$

   tem expansão

   $$
   f(t)=\frac{4}{T}\sum_{k=0}^\infty \frac{\sin\bigl((2k+1)t\bigr)}{2k+1}.
   $$

2. **Sinal dente de serra** $f(t)=t$ em $(-T,T]$:

   $$
   t = 2\sum_{n=1}^\infty \frac{(-1)^{n+1}}{n}\,\sin(nt).
   $$

3. **Função módulo** $f(t)=|t|$ em $[-T,T]$:

   $$
   |t| = \frac{T}{2} - \frac{4}{T}\sum_{n=1}^\infty \frac{\cos\bigl((2n-1)t\bigr)}{(2n-1)^2}.
   $$

---

Essas fórmulas permitem analisar qualquer sinal periódico, obter aproximações com quantos termos forem desejados e entender propriedades de suavização, Gibbs phenomenon, entre outros fenômenos clássicos da Série de Fourier.
