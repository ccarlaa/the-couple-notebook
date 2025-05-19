# Corpo

Um **corpo** (do latim *corpus*, em inglês *field*) é uma estrutura algébrica fundamental que generaliza as propriedades dos números racionais $\mathbb{Q}$, reais $\mathbb{R}$ e complexos $\mathbb{C}$, permitindo as operações de adição, subtração, multiplicação e divisão (exceto por zero), obedecendo certos axiomas.

---

## **Definição Formal**

Um **corpo** é um conjunto não vazio $\mathbb{K}$ munido de duas operações binárias:

* **Adição**: $(a,b) \mapsto a + b$
* **Multiplicação**: $(a,b) \mapsto a \cdot b$

tais que os seguintes **axiomas** são satisfeitos para todos $a, b, c \in \mathbb{K}$:

---

## **Axiomas dos Corpos**

### **1. Axiomas da adição:**

1. (Associatividade) $(a + b) + c = a + (b + c)$
2. (Comutatividade) $a + b = b + a$
3. (Elemento neutro aditivo) Existe $0 \in \mathbb{K}$ tal que $a + 0 = a$
4. (Inverso aditivo) Para todo $a$, existe $(-a)$ tal que $a + (-a) = 0$

### **2. Axiomas da multiplicação:**

5. (Associatividade) $(a \cdot b) \cdot c = a \cdot (b \cdot c)$
6. (Comutatividade) $a \cdot b = b \cdot a$
7. (Elemento neutro multiplicativo) Existe $1 \in \mathbb{K}$, com $1 \ne 0$, tal que $a \cdot 1 = a$
8. (Inverso multiplicativo) Para todo $a \ne 0$, existe $a^{-1}$ tal que $a \cdot a^{-1} = 1$

### **3. Distributividade entre as operações:**

9. (Distributividade) $a \cdot (b + c) = a \cdot b + a \cdot c$

---

## **Exemplos de Corpos**

* $\mathbb{Q}$: corpo dos números racionais
* $\mathbb{R}$: corpo dos números reais
* $\mathbb{C}$: corpo dos números complexos

---

## **Observações Importantes**

* Em um corpo, **todo elemento diferente de zero tem inverso multiplicativo**.
* Um corpo **não admite divisão por zero**, pois $0^{-1}$ não está definido.
* Um corpo com número finito de elementos é chamado de **corpo finito** ou **corpo de Galois**.

## **Resumo**

> Um **corpo** é um conjunto onde se pode **somar, subtrair, multiplicar e dividir** (exceto por zero), de maneira que essas operações obedeçam regras semelhantes às dos números reais.
