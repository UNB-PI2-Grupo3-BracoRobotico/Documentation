# Definição de esforços e momentos

## Esforços em pontos críticos

A avaliação dos pontos críticos deu-se através da analise de esforços em pontos de engaste, ou ligação entre partes mecânicas.Sendo assim, a tabela 1 mostra o a localização de tais pontos e os respectivos esforços em tais pontos.


Observa-se na tabela 1 o aparecimento de seis constantes, tal fato deve-se a algumas medidas serem passíveis de modificação, entre elas, o peso da barra horizontal(P=2,153 kg * 9,8 m/s²), o tamanho do carro de movimentação(M = 2x motor) e o peso das estruturas de sustentação do braço robótico(S = 0,2 kg ), as quais são conectadas na estante.Contudo, tais constantes podem ser calculadas através de parâmetros simples descritos nas equações 1 a 6.
Ademais, mostra-se na tabela  dois casos, nomeados de caso 1 e caso 2.Os referidos casos remetem a duas posições do eixo vertical móvel, quando a estrutura está centralizada e quando a estrutura está na extremidade, respectivamente.Desse modo, percebe-se que o caso 1 possui os dois apoios sujeitos a mesma tensão, contrapondo o caso 2.

A fórmula quadrática é definida por:

$$
C0 = -\frac{{43.67 - P}}{2}                                                         (1)

C1 = \frac{{-0.55 \times P + 21.835 \times M}}{{1.1 - \frac{M}{2}}}                         (2)

C2 = 43.67 - (P + C1)                                                       (3)

K0 = C0 + (0.22 + S) \times 9.8                                                (4)

K1 = C1 + (0.22 + S) \times 9.8                                                (5)

K2 = C2 + (0.22 + S) \times 9.8     
$$

As equações de 1 a 6 mostram os resultados em newtons(N),mas deve-se utilizar as medidas do sistema internacional de unidades(Si) para substituir as constantes.

## Momento Crítico

O objetivo desse tópico será apenas descrever o momento devido a projeção da garra no eixo z, ou seja , o uso da barra rosqueada.Realizando as equações de momento, foi possível perceber que para o engaste da barra rosqueada houve o maior momento fletor de magnitude 22,313 N.m.
