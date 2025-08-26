# Corpo

## Definição Formal

Seja $\mathbb{K}$ um conjunto não vazio com duas leis de composição interna:

* **adição**: $+ : \mathbb{K} \times \mathbb{K} \to \mathbb{K}$,
* **multiplicação**: $\cdot : \mathbb{K} \times \mathbb{K} \to \mathbb{K}$.

Chamamos $(\mathbb{K}, +, \cdot)$ de um **corpo** (ou **field**, em inglês) se as seguintes propriedades forem satisfeitas:

## Propriedades:

### 1. Soma:

$(\mathbb{K}, +)$ é um **grupo abeliano**

* **Associatividade**: $\forall a,b,c\in \mathbb{K},\; (a+b)+c = a+(b+c)$,
* **Elemento neutro aditivo**: $\exists 0\in \mathbb{K},\; \forall a\in \mathbb{K},\; a+0 = 0+a = a$,
* **Inverso aditivo**: $\forall a\in \mathbb{K},\; \exists -a\in \mathbb{K},\; a + (-a) = 0$,
* **Comutatividade**: $\forall a,b\in \mathbb{K},\; a+b = b+a$.

---

### 2. Multiplicação:

$(\mathbb{K}^*, \cdot)$ é um **grupo abeliano**, onde $\mathbb{K}^* = \mathbb{K} \setminus \{0\}$

* **Associatividade**: $\forall a,b,c\in \mathbb{K}^*,\; (a\cdot b)\cdot c = a\cdot(b\cdot c)$,
* **Elemento neutro multiplicativo**: $\exists 1\in \mathbb{K},\; 1\ne 0,\; \forall a\in \mathbb{K},\; a\cdot 1 = 1\cdot a = a$,
* **Inverso multiplicativo**: $\forall a\in \mathbb{K}^*,\; \exists a^{-1}\in \mathbb{K},\; a\cdot a^{-1} = 1$,
* **Comutatividade**: $\forall a,b\in \mathbb{K}^*,\; a\cdot b = b\cdot a$.

---

### 3. **Distributividade**:

$$
\forall a,b,c\in \mathbb{K},\quad a\cdot(b+c) = a\cdot b + a\cdot c.
$$

---

### Corpo vs Corpo Comutativo

Na definição moderna, **todo corpo já é comutativo** na multiplicação. Portanto, a expressão "corpo comutativo" é redundante na maioria das abordagens contemporâneas.

Porém, em abordagens mais antigas (ou em generalizações), distinguem-se:

* **Corpo (field)**: Multiplicação **comutativa** — padrão.
* **Corpo não comutativo** (ou **"divisão não comutativa"**, ou **"anel de divisão"**): Multiplicação **não necessariamente comutativa** — ex.: os **quaternions** $\mathbb{H}$.

---

### Exemplos

1. **Corpo dos números racionais**: $\mathbb{Q}$
   Com as operações usuais de $+$ e $\cdot$, é um corpo.

2. **Corpo dos números reais**: $\mathbb{R}$

3. **Corpo dos números complexos**: $\mathbb{C}$

4. **Corpo finito**:
   $$
   \mathbb{F}_p = \mathbb{Z}/p\mathbb{Z}
   $$
   onde $p$ é primo — corpo com $p$ elementos.

5. **Não é corpo**:
   $\mathbb{Z}$ (os inteiros) **não formam um corpo**, pois nem todo elemento diferente de zero possui inverso multiplicativo em $\mathbb{Z}$.
