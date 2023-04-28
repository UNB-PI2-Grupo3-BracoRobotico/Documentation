# <center> Introspecção

## Histórico de Versão<br>
Versão|Data|Descrição|Autor(es)
------|----|---------|--------
1.0   | 27/04/2023 | Criação do documento | Davi matheus


##  Introdução

<p style="text-align: justify; text-indent: 20px">A introspecção é uma técnica essencialmente voltada para especialistas em requisitos, que devem extrair as melhores informações por meio de uma análise profunda sobre como e quais requisitos são necessários para satisfazer os usuários e stakeholders do sistema. Embora seja uma técnica rica em detalhes e informações, pode não ser adequada quando não é um especialista da área realizando-a. No entanto, mesmo que não seja um especialista, ainda pode ser útil realizar a técnica de introspecção para extrair o máximo de suas vantagens e obter informações valiosas para o projeto. </p>
<p style="text-align: justify; text-indent: 20px">
A técnica utilizada consiste em o engenheiro de requisitos utilizar a imaginação como principal ferramenta, colocando-se no lugar do usuário do sistema e imaginando o que ele gostaria de realizar ao desempenhar determinadas atividades no sistema. Dessa forma, é possível obter informações valiosas sobre as necessidades e desejos dos usuários, contribuindo para a elaboração de requisitos mais precisos e efetivos para o projeto.
</p>

## Metodologia

<p style="text-align: justify; text-indent: 20px"> A fim de elaborar o artefato de requisitos, cada membro do grupo utilizou individualmente a técnica da introspecção para elicitar requisitos, os quais foram posteriormente compilados em um único artefato, eliminando duplicações de requisitos. Dessa forma, foi possível obter uma visão geral dos requisitos desejados pelos stakeholders do projeto, evitando redundâncias e garantindo a precisão das informações coletadas</p>



## 4. Requisitos levantados
<p style="text-align: justify; text-indent: 20px"> 
    A partir dos dados obtidos pelo brainstorming foi possível levantar possíveis requisitos da aplicação.
</p>
<p style="text-align: justify; text-indent: 20px"> 
    Dessa forma, foram detectados os seguintes requisitos:
</p>

## 4. Requisitos levantados
|ID|Descrição|Tipo de Requisito
|--|--|--|
|I01|Cadastro e login de <a href="../../modelagem/lexicos#usuario">usuário</a> com opção de recuperar senha|RF|
|I02|O <a href="../../modelagem/lexicos#produtor">produtor</a> deve visualizar suas <a href="../../modelagem/lexicos#propriedade">propriedades</a>|RF|
|I03|O sistema deverá  deve <a href="../../modelagem/lexicos#cadastrar_plantio">cadastrar uma plantação</a>|RF|
|I04|O produtor pode visualizar o histórico de suas <a href="../../modelagem/lexicos#visualizar_plantio">plantações</a> e <a href="../../modelagem/lexicos#visualizar_aplicacao_agrotoxico">agrotóxicos</a>|RF|
|I05|O produtor pode visualizar o perfil do <a href="../../modelagem/lexicos#tecnico">técnico</a> que está monitorando sua propriedade|RF|
|I06|O produtor pode visualizar o <a href="../../modelagem/lexicos#plantio_plantado">status de cada plantação</a>|RF|
|I07|O produtor deve <a href="../../modelagem/lexicos#aplicar_agrotoxico">cadastrar o uso do agrotóxico</a> com foto e data apenas|RF|
|I08|O técnico deve ter <a href="../../modelagem/lexicos#analisar_aplicacao_agrotoxico">acesso a foto dos agrotóxicos</a> enviadas pelos produtores|RF|
|I09|O técnico deve <a href="../../modelagem/lexicos#visualizar_propriedade">visualizar as propriedades</a> supervisionadas por ele|RF|
|I10|O aplicativo deve ter uso simples|RNF|
|I11|O usuário deve <a href="../../modelagem/lexicos#visualizar_plantio">visualizar as informações das plantações</a> responsáveis|RF|
|I12|O produtor pode ter acesso a recomendações e boas práticas para o produto agrícola plantado|RF|
|I13|O produtor deve adicionar a data de colheita <a href="../../modelagem/lexicos#plantio_finalizado">encerrando a plantação</a>|RF|
|I14|O produtor pode programar o uso de um agrotóxico |RF|
|I15|O técnico deve  editar as informações necessárias da plantação e do agrotóxico |RF|
|I16|O usuário pode editar suas informações pessoais|RF|
|I17|O usuário deve ter acesso a informações pertinentes ao uso do app (<a href="../../modelagem/lexicos#plantio_finalizado">plantações concluídas</a>, <a href="../../modelagem/lexicos#aplicacao_agrotoxico">agrotóxicos utilizados</a>)|RF|
|I18|O aplicativo deve ser seguro para garantir o <a href="../../modelagem/lexicos#cardeneta_de_campo">rastreamento das plantações</a>|RNF| 
|I19|O aplicativo deve ser intuitivo|RNF|
|I20|O aplicativo deve ser acessível|RNF|
<h6 align = "center">Tabela 1: Tabela contendo os requisitos levantados pela introspecção</h6>
<h6 align = "center">Fonte: Autor</h6>


<center>


|Legenda|Descrição|
|:--:|:--:|
|I|Introspecção|
|RF|Requisito Funcional|
|RNF|Requisito Não Funcional|
<h6>Tabela 2: Legenda dos acrônimos contidos na Tabela 1</h6>
<h6>Fonte: Autor</h6>

</center>


## 5. Referências

> [1] - SERRANO, Maurício; SERRANO, Milene. Disponível em: Requisitos - Aula 07. 1º/2019. 50 slides. Material apresentado para a disciplina de Requisitos de Software no curso de Engenharia de Software da UnB, FGA.<br> > [2] - ANDRADE DE MORAIS, E. Utilização de uma estratégia para Identificação de fontes de informação na fase de Elicitação. Doutorado—[s.l.] Pontifícia Universidade Católica Do Rio De Janeiro, 2021.<br>
