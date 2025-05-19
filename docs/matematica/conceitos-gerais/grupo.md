# Grupo

## 1. Definição

Um **grupo** é um par

$$
\boxed{(G, \ast)}
$$

onde $G$ é um conjunto e $\ast : G \times G \to G$ é uma **operação binária interna**, tal que:

## 2. Axiomas (para todo $a, b, c \in G$):

1. **Associatividade**:

    $$
    (a \ast b) \ast c = a \ast (b \ast c)
    $$

2. **Elemento neutro (identidade)**:

    $$
    \exists\, e \in G \;\text{tal que}\; \forall a \in G,\; a \ast e = e \ast a = a
    $$

3. **Inverso**:

    $$
    \forall a \in G,\; \exists\, a^{-1} \in G \;\text{tal que}\; a \ast a^{-1} = a^{-1} \ast a = e
    $$

---

## 🔹 2. **Grupo Abeliano** (ou **grupo comutativo**)

É um grupo $(G, \ast)$ que **também satisfaz**:

4. **Comutatividade**:

   $$
   \forall a, b \in G,\quad a \ast b = b \ast a
   $$

---