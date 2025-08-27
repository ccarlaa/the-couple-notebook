# Função

## **Definição Formal de Função**

Sejam $A$ e $B$ dois conjuntos não vazios.

Uma **função** $f$ de $A$ em $B$ é uma relação especial $f \subseteq A \times B$ tal que:

$$
\forall x \in A \; \exists! \, y \in B \; : \; (x,y) \in f
$$

### **Explicação dos símbolos**:

* $f \subseteq A \times B$ → $f$ é um subconjunto do [produto cartesiano](../conceitos-gerais/produto-cartesiano.md) $A \times B$;
* $(x,y) \in f$ → o par ordenado $(x,y)$ pertence à função;
* $\exists!$ → significa **“existe um único”**. Ou seja, um $x$ pode estar associado a **somente um** $y$.

---

## **Notação usual**

Denotamos essa função por:

$$
f: A \to B
$$

e, para cada $x \in A$, escrevemos:

$$
f(x) = y \quad \text{com} \quad y \in B
$$

---

## **Domínio, Contradomínio e Imagem**

Dada $f: A \to B$, temos:

* **Domínio**:

  $$
  \operatorname{Dom}(f) = A
  $$
* **Contradomínio**:

  $$
  \operatorname{CD}(f) = B
  $$
* **Imagem**:

  $$
  \operatorname{Im}(f) = \{ y \in B \mid \exists x \in A \, : \, f(x) = y \}
  $$

---

## **Definição Completa com Conjunto de Pares**

Podemos definir formalmente a função como um **conjunto de pares ordenados**:

$$
f = \{ \, (x,y) \in A \times B \mid y = f(x) \, \}
$$

com a **propriedade de univalência**:

$$
\forall x \in A \; \forall y_1, y_2 \in B :
\Big[ (x,y_1) \in f \land (x,y_2) \in f \Big] \implies y_1 = y_2
$$

---

