# Série de Fourier

## Um pouco de história

A série de Fourier surgiu no início do século XIX, quando o matemático francês Joseph Fourier buscava compreender a propagação do calor em corpos sólidos. Em 1807, ele apresentou à Academia Francesa seu trabalho "Mémoire sur la propagation de la chaleur dans les corps solides", no qual propôs que qualquer função periódica poderia ser expressa como uma soma infinita de senos e cossenos — o que hoje conhecemos como série de Fourier. 

## 1. Resumo
Uma **série de Fourier** expressa uma função periódica $f$ como uma soma de funções trigonométricas ou fasores. Assim, qualquer forma de onda ou função periódica — desde sinais elétricos até vibrações mecânicas — pode ser “decomposta” em **harmônicos puros**, o que é fundamental em Análise de Sinais, Física e Engenharia.

---

## 1. Contexto e Espaço Funcional

Seja $f\colon \mathbb{R}\to\mathbb{R}$ (ou $\mathbb{C}$) **periódica** de período $2\pi$, isto é,

$$
f(x + 2\pi) = f(x)\quad\forall x\in\mathbb{R}.
$$

Suponha que $f$ satisfaça as **condições de Dirichlet** em um período (por exemplo, seja de classe $C^1$ por partes). Então $f$ pertence ao espaço $L^2([-\pi,\pi])$ ou ao espaço das funções de quadrado-integrável em $[-\pi,\pi]$.

No espaço de Hilbert $\bigl(L^2([-\pi,\pi]),\langle\cdot,\cdot\rangle\bigr)$, tomamos o **produto interno**

$$
\langle g, h\rangle \;=\;\int_{-\pi}^{\pi} g(x)\,\overline{h(x)}\,dx
$$

e a norma associada $\|g\|^2=\langle g,g\rangle$.

As funções

$$
1,\quad \cos(nx),\quad \sin(nx)\quad(n=1,2,3,\dots)
$$

formam um **sistema ortogonal** em $L^2([-\pi,\pi])$.

---

## 2. Forma Trigonométrica da Série de Fourier

Para $f$ periódico de período $2\pi$, definimos os **coeficientes**:

$$
\begin{aligned}
a_0 &= \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\,dx,\\
a_n &= \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\,\cos(nx)\,dx,\quad n\ge1,\\
b_n &= \frac{1}{\pi}\int_{-\pi}^{\pi} f(x)\,\sin(nx)\,dx,\quad n\ge1.
\end{aligned}
$$

A **série de Fourier** de $f$ é então:

$$
\boxed{
f(x)\sim \frac{a_0}{2}
\;+\;\sum_{n=1}^{\infty}\bigl[a_n\cos(nx)+b_n\sin(nx)\bigr].
}
$$

— Aqui “$\sim$” indica que a série converge (em norma $L^2$, ponto a ponto ou uniformemente, conforme hipóteses adicionais) para $f$ ou para $\bigl(f(x^+)+f(x^-)\bigr)/2$ se houver descontinuidades.

---

## 3. Forma Exponencial (Complexa)

Em vez de seno e cosseno, usa-se a base completa de exponenciais:

$$
e^{inx},\quad n\in\mathbb{Z},
$$

ortogonais em $L^2([-\pi,\pi])$. Definem‑se

$$
c_n = \frac{1}{2\pi}\int_{-\pi}^{\pi} f(x)\,e^{-inx}\,dx,
\qquad n\in\mathbb{Z}.
$$

A **série de Fourier complexa** é:

$$
\boxed{
f(x)\sim \sum_{n=-\infty}^{\infty} c_n\,e^{inx}.
}
$$

Relação com a forma trigonométrica:

$$
c_0 = \frac{a_0}{2},\quad
c_n = \frac{a_n - i\,b_n}{2},\quad
c_{-n} = \frac{a_n + i\,b_n}{2}.
$$

---

## 4. Teoremas de Convergência

* **Convergência em $L^2$**: Se $f\in L^2([-\pi,\pi])$, então sua série de Fourier converge para $f$ em norma $L^2$.

* **Convergência pontual** (Dirichlet): Se $f$ é periódica e com número finito de descontinuidades e de máximos/minimos por período, então para todo $x$,

  $$
  S_N(x)
  := \frac{a_0}{2} + \sum_{n=1}^N [a_n\cos(nx)+b_n\sin(nx)]
  \;\longrightarrow\;
  \frac{f(x^+)+f(x^-)}{2}
  \quad(N\to\infty).
  $$

* **Convergência uniforme**: Se $f$ é contínua e de classe Lipschitz ou com derivada contínua, a convergência é uniforme.

---

## 5. Exemplos

1. **Onda quadrada** de período $2\pi$:

   $$
   f(x) =
   \begin{cases}
   1, & 0<x<\pi,\\
   -1,& -\pi<x<0,
   \end{cases}
   $$

   tem expansão

   $$
   f(x)=\frac{4}{\pi}\sum_{k=0}^\infty \frac{\sin\bigl((2k+1)x\bigr)}{2k+1}.
   $$

2. **Sinal dente de serra** $f(x)=x$ em $(-\pi,\pi]$:

   $$
   x = 2\sum_{n=1}^\infty \frac{(-1)^{n+1}}{n}\,\sin(nx).
   $$

3. **Função módulo** $f(x)=|x|$ em $[-\pi,\pi]$:

   $$
   |x| = \frac{\pi}{2} - \frac{4}{\pi}\sum_{n=1}^\infty \frac{\cos\bigl((2n-1)x\bigr)}{(2n-1)^2}.
   $$

---

Essas fórmulas permitem analisar qualquer sinal periódico, obter aproximações com quantos termos forem desejados e entender propriedades de suavização, Gibbs phenomenon, entre outros fenômenos clássicos da Série de Fourier.
