# Documento de Estrutura

## Definição Estrutura

Visando buscar remédios organizados em prateleiras, o braço robótico será construído para se mover horizontal e verticalmente até a coordenada do remédio selecionado para que, em seguida, sua garra possa pegar e retirar a caixa de remédio da prateleira e a depositar em um local fixo para sua retirada.</br>
Para isso, o projeto constará de dois motores responsáveis pela movimentação da garra ao longo da prateleira, sendo um para o eixo x e outro para o eixo y, e a garra possuirá mais dois motores para executar sua função, um para o eixo z e outro para o movimento de abrir e fechar. Sendo assim, a estrutura do projeto terá o objetivo de acomodar os motores e fazer com que o braço execute seus movimentos da forma mais simples, segura e rápida possível.</br>

## Descrição Detalhada das partes da estrutura

O braço robótico se baseará em movimentações simples em três dimensões, logo, existirão três motores e três mecanismos de movimentação principais.A parte superior da estrutura possuirá duas barras horizontais, a primeira possuirá a função de deixar a estrutura mais estável e equilibrada em relação seus esforços. A segunda, além de servir de sustentação do robô, será a responsável por manter fixa o mecanismo de movimentação horizontal.</br>
A barra voltada para a projeção da garra, isto é, a barra mais próxima dos remédios a serem pegados, estará diretamente conectada com a estrutura de movimentação vertical. Desse modo, será um elemento da estrutura que provavelmente terá que ser reforçado, pois pode haver uma concentração de esforços verticais e devido a barra estar na horizontal pode ser apresentado um certo tipo de deflexão.</br>
A barra mais afastada terá a função de reduzir os esforços sobre a primeira barra. Analisando-se o projeto, observa-se que a referida barra não possui nenhum tipo de possível carga, desse modo, será posto uma terceira barra. Contudo, esta será inserida transversalmente às outras duas.</br>
O elemento transversal possuirá dupla função, pois além de transferir os esforços para a barra menos crítica auxiliará na movimentação horizontal. O componente estará conectado ao motor responsável pela movimentação horizontal e à estrutura que abrange a locomoção noutros eixos. O comprimento da referida barra será significativamente menor se comparada com as outras duas.Dessa forma, apesar da sua dupla função, prevê-se que a mesma não apresente muitas complicações.</br>
O projeto apresenta, além de tais barras superiores, um elemento vertical, central e móvel. Tal componente será o responsável por compreender o mecanismo de movimentação vertical e o mecanismo de projeção da garra. Sendo assim, será possivelmente o elemento mais crítico de toda estrutura, pois além de movimentar- se horizontalmente, terá diversos esforços atuando no mesmo.</br>
Contudo, para solucionar esse problema é proposto a adição de três peças triangulares na base do objeto vertical, distribuindo os esforços.Porém, tais objetos terão um tamanho tal que não prejudique intensamente a amplitude do movimento vertical e seja suficiente para seu fim.As três peças, no entanto, não estarão encostadas no chão ou em alguma superfície livre devido ao fato da estrutura vertical ter a possibilidade de movimento.</br>
A fim da movimentação de tal parte, serão colocadas na base da mesma, pequenos rolamentos e um trilho na barra inferior ligada ao componente vertical.A quantidade de tais rodas ou rolamentos dependerá do seu tamanho e da espessura na base com as estruturas de reforço.Os elementos em questão deverão possuir o mínimo de atrito possível com o solo para um bom funcionamento do braço robótico.</br>
Todavia, destacam-se outras duas porções móveis da estrutura, uma garra e uma barra responsável pelo movimento de profundidade.A garra, um elemento que será comprado (modelo Crock V2), possuirá dentes e será provavelmente revestido de algum material que aumenta o atrito.Assim, o contato com o medicamento será mais eficiente, evitando impasse, como, por exemplo, soltar o medicamento antes do momento adequado.</br>
A barra será conectada a um mecanismo que possibilitará sua projeção e sua retração em uma extremidade e noutra estará a garra.No entanto, ela deverá ter um tamanho suficiente para que ao ser projetada uma parcela de seu comprimento situe-se anterior ao mecanismo de movimentação nesse eixo.A medida é proposta com o intuito de reduzir o momento fletor.</br>
As duas barras na parte inferior da estrutura servirão para a fixar melhor, reduzindo balanços e deslocamentos indesejados.Ademais, os dois componentes laterais servirão de apoio, sendo os principais na integridade estrutural e na fixação de componentes eletrônicos.Ambas estruturas estarão em contato com o solo ou com uma superfície livre no seu ambiente de execução.

## Materiais

O material escolhido para a estrutura é o alumínio devido a diversos fatores. A densidade do metal é uma das menores se comparada a de outros metais, ao passo que sua densidade é de 2,70 g/cm³, materiais como o aço e cobre possuem densidade por volta de 7,86 g/cm³ e 8,92 g/cm³, respectivamente. Ademais, a facilidade em seu uso apresenta-se como outra vantagem, pois a ductilidade do alumínio é elevada, facilitando processos de montagem e possibilitando a previsão de rompimento. Além disso, devido à existência de um fornecedor conhecido pelo grupo, seu preço torna-se acessível.</br>


### Matriz de decisão sobre materiais

|     Material    |     Densidade     (g/cm³)    |     Preço     (Reais/Kg)    |     Dureza    |     Limite de escoamento(MPa)     |     Facilidade de Uso    |     Resistência a oxidação    |
|---|---|---|---|---|---|---|
|     Alumínio    |     2,70    |     10,00    |     26 HB    |     220    |     Alta    |     Elevada    |
|     Aço com baixo teor de   carbono(1020)    |     7,87    |     6,50    |     170 HB    |     205    |     Alta    |     Baixa    |
|     Aço com médio teor de   carbono(1045)    |     7,87    |     7,50    |     240 HB    |     430    |     Alta    |     Baixa    |
|     Cobre    |     8,96    |     23,00    |     45 HB    |     190    |     Média    |     Média    |
|     Madeira    |     1,53    |     15,30    |     73 HB    |     40    |     Média    |     Não Oxida    |
|     Polipropileno    |     0,90    |     23,35    |     66 Shore D    |     32    |     Baixa    |     Não Oxida    |
|     UHMW    |     0,93    |     64,10    |     64 Shore D    |     40    |     Baixa    |     Não Oxida    |

Pode-se observar na tabela 1 sete materiais usuais para sistemas mecânicos simples de acordo com um artigo da Universidade Federal de Santa Maria,”Materiais de construção Mecânica” .Analisando-se o aspecto densidade, o menor valor foi o do polímero polipropileno(0,9 g/cm³),valor descrito pelo site Imperlast.Contudo, em relação aos metais, o do alumínio possuiu destaque(2,7 g/cm³).Apesar de ser o segundo metal mais caro, referente aos metais da tabela 1, foi o terceiro material mais barato com o preço médio de dez reais,preços tabelados com valores encontrados no Mercado Livre .
Ademais, a ductilidade do alumínio também mostra-se como uma vantagem pois apesar de ser o material mais dúctil da tabela, sem considerar os polímeros(mostrado pela menor dureza de 26 HB), seu limite de escoamento é o segundo maior(220 Mpa) de acordo com o artigo da UFSM.Assim, pode-se perceber uma característica importante do material para sistemas mecânicos, a resistência do material a deformações plásticas atrelada a baixa fragilidade,isto é, um material tenaz.
Outrossim, a elevada resistência a oxidação do alumínio e sua facilidade de uso apresentam-se como aspectos positivos.A primeira propriedade se deve ao fato do alumínio reagir rapidamente com o oxigênio criando uma camada de óxido de alumínio que impede prolongação da oxidação.Porém, a segunda característica deve-se a diversidade de perfis comerciais e sua baixa dureza, tornando-se um material de fácil utilização.

## Dimensões Gerais

A estrutura possuirá um metro de comprimento, um metro de largura e 22 cm de profundidade. Além disso, a barra a qual a garra está conectada possuirá o comprimento de 52 cm para reduzir o momento, visto que, a profundidade máxima de projeção da garra será 30 cm.</br>

## Desenhos

![Visão 3D](assets/desenho_visao_3d.png)

![Visão 3D](assets/desenho_visao_vertical.png)

![Visão 3D](assets/desenho_visao_vertical.png)

## Definição de esforços e momentos

### Esforços em pontos críticos

A avaliação dos pontos críticos deu-se através da analise de esforços em pontos de engaste, ou ligação entre partes mecânicas.Sendo assim, a tabela 1 mostra o a localização de tais pontos e os respectivos esforços em tais pontos.


Observa-se na tabela 1 o aparecimento de seis constantes, tal fato deve-se a algumas medidas serem passíveis de modificação, entre elas, o peso da barra horizontal(P=2,153 kg * 9,8 m/s²), o tamanho do carro de movimentação(M = 2x motor) e o peso das estruturas de sustentação do braço robótico(S = 0,2 kg ), as quais são conectadas na estante.Contudo, tais constantes podem ser calculadas através de parâmetros simples descritos nas equações 1 a 6.
Ademais, mostra-se na tabela  dois casos, nomeados de caso 1 e caso 2.Os referidos casos remetem a duas posições do eixo vertical móvel, quando a estrutura está centralizada e quando a estrutura está na extremidade, respectivamente.Desse modo, percebe-se que o caso 1 possui os dois apoios sujeitos a mesma tensão, contrapondo o caso 2.

A fórmula quadrática é definida por:

(1): C0 = -(43,67 - P) / 2</br>
(2): C1 = (-0,55×P + 21,835×M) / (1,1 - M/2)</br>
(3): C2 = 43,67 - (P +C1)</br>
(4): K0 = C0 + (0,22 + S)×9,8 </br>
(5): K1 = C1 + (0,22 + S)×9,8 </br>
(6): K2 = C2 + (0,22 + S)×9,8 </br>


As equações de 1 a 6 mostram os resultados em newtons(N),mas deve-se utilizar as medidas do sistema internacional de unidades(Si) para substituir as constantes.

### Momento Crítico

O objetivo desse tópico será apenas descrever o momento devido a projeção da garra no eixo z, ou seja , o uso da barra rosqueada.Realizando as equações de momento, foi possível perceber que para o engaste da barra rosqueada houve o maior momento fletor de magnitude 22,313 N.m.


## Tensão

### Esforços em pontos críticos

Os materiais possuem certas propriedades que podem prever sua falha dependendo de uma carga aplicada.Sendo assim, a tensão de escoamento aparece como principal característica com esse fim.Desse modo, será mostrado na tabela 1 as principais tensões encontradas e o tipo de material que é feito a estrutura.

|     Posição    |     Material    |     Tensão (Pa)    | Efeito | Impacto |
|---|---|---|---|---|
|     Engaste da barra rosqueada    |     Aço    |     48x106    | Retrabalho da equipe | Alto |
|     Contato inferior da barra vertical    |     Alumínio    |     ----    | Escopo mal definido | Alto |
|     Contato superior da barra vertical    |     Alumínio    |     0,94x106    | Sobrecarga dos integrantes restantes da equipe | Alto |
|     Apoios da barra horizontal(caso 1)    |     Alumínio    |     ----    | Falha no alinhamento entre as equipes multidisciplinares | Baixo |
|     Apoio 1 da barra horizontal(caso 2)    |     Alumínio    |     -----    | Atraso no desenvolvimento do produto | Alto |
|     Apoio 2 da barra horizontal(caso 2)    |     Alumínio    |     43,87x103    | Postergação na entrega de funcionalidades | Baixo |
|     Engastes na estante(caso 1)    |     Alumínio    |     -----    | Atraso no desenvolvimento do produto | Médio |
|     Engaste 1 na estante (caso 2)    |     Alumínio    |     -----    |  |  |
|     Engaste 2 na estante (caso 2)    |     Alumínio    |     7,46x10³    |  |  |

Observa-se na tabela 1 lacunas com os valores de tensão não descritos, isto se deve ao fato de ser descrito para uma mesma estrutura apenas os valores máximos de tensão.Desse modo, é possível perceber que para a barra vertical, o apoio superior,aquele que está diretamente ligado com a barra de movimentação horizontal, concentrou maiores tensões.Ademais, para a barra horizontal,a maior tensão surge quando o carro de movimentação localiza-se em uma das extremidades(caso 2), o mesmo ocorrendo para o local de engaste na estante.

## Bibliografia

[1]Polímeros de engenharia, disponível em: https://www.imperplast.com.br/polimeros-de-engenharia-o-que-sao-e-quais-suas-finalidades/
[2]Materiais comuns na engenharia, disponível em : https://www.ufsm.br/app/uploads/sites
/413/2018/11/02_materiais_construcao_mecanica.pdf
[3]Materiais de construção mecânica, disponível em:https://www.ufsm.br/app/uploads/sites
/413/2018/11/02_materiais_construcao_mecanica.pdf
[4]Ligas de aço e suas características,disponível em:https://serrametal.com.br/acos-influencias-das-ligas-dos-materiais-e-suas-aplicacoes/
[5]Preço do Polietileno,disponível em:https://produto.mercadolivre.com.br/MLB-1867935915-tarugo-polietileno-pe-uhmw-natural-30mmx1000mm-_JM#position=4&search_layout=stack&type=item&tracking_id=9290c6c7-6b4e-4e9e-af56-2c75d8687605
[6]Características do cobre, disponível em:https://shockmetais.com.br/tabelas/cobre/pmec
[7]Características do uhmw,disponível em:https://incomplast.com.br/uhmw/

## Histórico de Versionamento

| Versão | Data       | Descrição                          | Autor            |
| ------ | ---------- | ---------------------------------- | ---------------- |
| 1.0    | 02/05/2023 | Criação do documento de estruturas | Mauricio Machado |
| 1.1    | 23/05/2023 | Adição de novos topicos de material e tensao | Natanael Fernandes |
