Se os vigilantes forem considerados pessoas distintas, procedemos assim:

1. **O posto principal deve estar ocupado.** Primeiro, escolhemos qual dos 4 vigilantes ficará no posto principal: são 4 possibilidades.

2. **Distribuição dos demais 3 vigilantes nos outros 6 postos:**

   * Das 6 vagas restantes, precisamos escolher 3 para abrigar os outros 3 vigilantes. Isso pode ser feito de $\binom{6}{3}=20$ maneiras (escolhemos 3 postos dentre os 6).
   * Para cada escolha de 3 postos, ainda temos que decidir qual vigilante vai para qual posto. Como são 3 vigilantes distintos e 3 postos, há $3!=6$ maneiras de atribuição.

Portanto, o número total de formas é:

$$
\underbrace{4}_{\substack{\text{escolha do vigilante}\\\text{do posto principal}}}
\times
\underbrace{\binom{6}{3}}_{20}
\times
\underbrace{3!}_{6}
\;=\;
4 \times 20 \times 6 \;=\; 480.
$$

Logo, existem **480** maneiras de distribuir os 4 vigilantes nos 7 postos, garantindo que o posto principal fique sempre ocupado.

