Com certeza, Victor. Aqui está a **definição completa e formal** do **Teorema de Plancherel**, no contexto da **Transformada de Fourier em $L^2(\mathbb{R})$**.

---

## 🔹 Enunciado formal do Teorema de Plancherel

Seja $\mathcal{F}$ o operador de Transformada de Fourier, definido inicialmente para funções $x \in L^1(\mathbb{R}) \cap L^2(\mathbb{R})$ por:

$$
\mathcal{F}\{x\}(\omega) = \int_{-\infty}^{\infty} x(t)\,e^{-j\omega t}\,dt,
$$

então:

### ✅ Existe uma **extensão única** e **unitária** de $\mathcal{F}$ para todo $L^2(\mathbb{R})$, denotada também por $\mathcal{F}: L^2(\mathbb{R}) \to L^2(\mathbb{R})$, tal que:

$$
\boxed{
\forall x \in L^2(\mathbb{R}), \quad
\|\mathcal{F}\{x\}\|_{L^2(\mathbb{R})} = \|x\|_{L^2(\mathbb{R})}
}
$$

---

## 🔹 Forma com produto interno

Em termos de produto interno, o teorema afirma:

$$
\boxed{
\forall x, y \in L^2(\mathbb{R}), \quad
\langle \mathcal{F}\{x\}, \mathcal{F}\{y\} \rangle_{L^2}
=
\langle x, y \rangle_{L^2}
}
$$

onde:

$$
\langle x, y \rangle_{L^2}
=
\int_{-\infty}^{\infty} x(t)\,\overline{y(t)}\,dt
\quad \text{e} \quad
\langle \mathcal{F}\{x\}, \mathcal{F}\{y\} \rangle
=
\int_{-\infty}^{\infty} X(\omega)\,\overline{Y(\omega)}\,d\omega.
$$

---

## 🔹 Consequências

O Teorema de Plancherel implica que:

* $\mathcal{F}$ é um **operador unitário** no espaço de Hilbert $L^2(\mathbb{R})$
* A transformada de Fourier é **bijetiva**, **linear**, e **isométrica** em $L^2(\mathbb{R})$
* $$
  \int_{-\infty}^{\infty}
  |x(t)|^2\,dt =
  \int_{-\infty}^{\infty}
  |X(\omega)|^2\,d\omega
  \quad \text{(conservação de energia)}
  $$

---

## 🔹 Forma condensada

$$
\boxed{
\mathcal{F} : L^2(\mathbb{R}) \to L^2(\mathbb{R})
\text{ é unitária, i.e., }
\langle \mathcal{F}x, \mathcal{F}y\rangle = \langle x, y\rangle
}
$$

---

Se quiser, posso também enunciar a versão do **Teorema de Plancherel** para $L^2(\mathbb{R}^n)$ ou em forma espectral para operadores autoadjuntos. Deseja que estendamos?
