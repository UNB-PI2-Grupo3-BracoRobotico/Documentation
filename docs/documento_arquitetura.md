# Documento de Arquitetura

<!-- Adicionar explicação do que é o documento de arquitetura e sua finalidade -->

# Diagrama de implementação

O Diagrama de Implementação é uma representação visual que mostra a estrutura física da arquitetura de um sistema de software. Ele se concentra na organização do ambiente físico em que o software será implantado e executado, incluindo o hardware necessário, como computadores pessoais e servidores que suportarão o sistema. O diagrama é a visão mais tangível da UML e ajuda a entender como os diferentes componentes do sistema se relacionam entre si em termos físicos.

O Diagrama de Implementação será usado para descrever a conexão das máquinas e os protocolos de comunicação utilizados para transferir informações. O objetivo é obter uma visão clara da implementação do software, o que facilita o processo de desenvolvimento, uma vez que a modelagem é focada em um nível arquitetural mais específico em relação ao hardware. Com o Diagrama de Implementação, é possível entender como os componentes do sistema se interconectam fisicamente e quais recursos de hardware são necessários para executar o software. Dessa forma, é possível identificar e resolver problemas de desempenho ou escalabilidade antes de implementar o sistema, o que pode economizar tempo e recursos. O diagrama também ajuda a comunicar a arquitetura do sistema para as partes interessadas de forma clara e eficaz.

## v1.0

![Versão v1.0 do diagrama de implementação](./assets/documento_arquitetura/diagrama_implementacao.png)

A primeira versão desse diagrama se concentrou em um nível de desenvolvimento e tangibilizou uma implantação mais simples. Partindo dessa perspectiva, temos o servidor da aplicação englobando o ambiente do Front End, Back End e o Banco de Dados rodando localmente.

## v2.0

![Versão v1.0 do diagrama de implementação](./assets/documento_arquitetura/diagrama_implementacaoV2.png)

A segunda versão desse diagrama apresenta todos os ambientes estão dentro do container do Docker. O acesso é feito pelo protocolo HTTP a partir de navegadores e do protocolo TCP/IP para comunicação com o Banco de Dados.

# Diagrama de Pacote (Front-End)

Diagramas de pacotes são diagramas estruturais comumente usados para simplificar os diagramas de classe complexos e organizar as classes em pacotes. Um grande benefício desse artefato é a visibilidade de alto nível do sistema a ser desenvolvido. Abaixo o grupo criou o diagrama de pacotes referente a aplicação front-end com estruturação na _Clean Architecture_.

## v1.0

![Diagrama de Pacote Front-End v1.0](./assets/documento_arquitetura/diagrama_pacote_frontend_v1.png)

O diagrama indica a estrutura do projeto, sendo divida em features, onde cada feature possui as seguintes camadas: infra, data, domain, presentation. Essa estrutura possui diversas classes abstratas, o que entra em acordo com a pasta de testes onde o criamos mocks a partir dessas classes abstratas. A arquitetura do projeto será a _Clean Architecture_, filosofia para design de software, ela separa os elementos do software em anéis de acesso.<br>
Isso tem como objetivo organizar o código a fim de encapsular as regras de negócio. A principal regra dessa metodologia de design é que anéis mais externos podem ter conhecimento de anéis internos, porém o inverso não é verdade, dessa forma, camadas internas, não conhecem funções/ métodos de camadas externas.

### Infra

Camada que faz o intermédio com à api do sistema, tem a responsabilidade de fazer a request e receber o dado "cru" sem nenhuma tratativa.

### Data

Camada responsável por tratar o dado adquirido pela infra e passá-lo ao domínio já estruturado como é requisitado. Caso o dado não esteja como esperado, será essa camada que levantará uma exceção que irá ser tratada no domínio da aplicação.

### Domain

Camada encapsulado do sistema frontend que não é afetada por mudanças fora dessa camada (com exceções de mudanças na regra do negócio). Nessa camada que é definida os usecases, entidades e falhas específicas do domínio. No caso de necessidade de vários usecases pode-se criar uma rotina que faz uso de um agrupamento de usecases.

# Diagrama de Pacote (Back-end)

Diagrama de pacotes são diagramas estruturais comumente usados para simplificar os diagramas de classe complexos e organizar as classes em pacotes. Um grande benefício desse artefato é a visibilidade de alto nível do sistema a ser desenvolvido. Abaixo o grupo criou o diagrama de pacotes referente a aplicação back-end com estruturação na _Clean Architecture_.

## v1.0

![Diagrama de Pacote Back-End v1.0](./assets/documento_arquitetura/diagrama_pacote_backend_v1.png)

Os componentes com o sufixo 'Consumer' e 'Producer' são respectivamente responsáveis por se conectarem com o sistema Apache Kafka para enviar e receber mensagens de outros sistemas e/ou pacotes.

Os componentes com o sufixo 'Processor' têm a responsabilidade de implementar a lógica do pacote, sem se preocupar em como a comunicação com outros sistemas e/ou pacotes é feita.

Os pacotes 'Models' são responsáveis por modelos de objetos a serem utilizados.

Os pacotes 'Exceptions' são responsáveis por especificar excessões para que erros não sejam tratados de forma genérica.

### order_manager

Tem a responsabilidade de gerenciar as ordens de compra, fazendo a comunicação com o banco de dados e com o sistema de pagamento.

### payment_manager

Tem a responsabilidade de gerenciar e verificar os pagamentos.

### robotic_arm_controller

Tem a responsabilidade de gerar e enviar os comandos para o braço robótico.

### database_manager

Tem a responsabilidade de realizar operações de leitura, registro, atualização e remoção de dados no banco de dados.

### config

Tem a responsabilidade de armazenar valores de configurações do sistema.

### tests

Tem a responsabilidade de armazenar os testes unitários e de integração do sistema.

## Diagrama de Sequência

Os diagramas de sequência são uma representação gráfica fundamental para modelar a interação entre objetos em um sistema. Eles fornecem uma visão detalhada da sequência de mensagens trocadas entre os objetos ao longo do tempo, permitindo que se visualize o comportamento dinâmico do sistema em questão. Além disso, os diagramas de sequência são amplamente utilizados na modelagem de processos de negócios, fluxos de trabalho e interações de software[3]. Como resultado, eles são ferramentas valiosas para os desenvolvedores de software e usuários finais, auxiliando na identificação de requisitos funcionais do sistema e na lógica de processamento de dados. Em resumo, os diagramas de sequência são uma parte essencial do processo de engenharia de software, permitindo uma comunicação clara e concisa de ideias e requisitos.


### Diagrama do aplicativo de compras

```mermaid
sequenceDiagram
    participant Cliente
    participant Loja
    participant Carrinho
    participant Pagamento
    participant Grupo

    activate Cliente

    Cliente->>Loja: Fazer cadastro
    Loja->>Cliente: Solicitar nome completo
    Cliente->>Loja: Enviar nome completo
    Loja->>Cliente: Solicitar CPF
    Cliente->>Loja: Enviar CPF
    Loja->>Cliente: Solicitar confirmação por foto de documento
    Cliente->>Loja: Enviar foto de documento
    Loja->>Cliente: Solicitar endereço
    Cliente->>Loja: Enviar endereço

    Loja->>Cliente: Cadastro concluído

    Cliente->>Loja: Acessar área logada
    activate Loja

    loop Enquanto logado
        Cliente->>Loja: Gerenciar carrinho
        Loja->>Carrinho: Adicionar/Remover produtos
        Loja->>Cliente: Carrinho atualizado

        Cliente->>Loja: Juntar-se a um grupo de compra
        Loja->>Cliente: Grupos disponíveis
        activate Grupo
        Grupo-->>Cliente: Lista de grupos

        Cliente->>Grupo: Escolher grupo
        Grupo->>Loja: Solicitar entrada no grupo
        Loja->>Grupo: Verificar disponibilidade e aprovar entrada
        alt Entrada aprovada
            Loja-->>Cliente: Entrada aprovada no grupo
            Cliente->>Loja: Carrinho compartilhado do grupo

            Cliente->>Loja: Efetuar compra
            Loja->>Cliente: Oferecer formas de pagamento
            activate Pagamento

            Pagamento-->>Cliente: Escolher forma de pagamento

            deactivate Pagamento
            Loja->>Cliente: Compra realizada com sucesso
        else Entrada negada
            Loja-->>Cliente: Entrada negada no grupo
        end

        deactivate Grupo
    end

    deactivate Loja
    deactivate Cliente
```

<center>

<p> Figura 3: diagrama de sequência para o aplicativo de compras do Projeto Integrador 2, Med Grabber(Fonte: autores, 2023).</p>

</center>

Descrevendo o fluxo apresentado, o cliente começa fazendo o cadastro, fornecendo informações como nome completo, CPF, confirmação por foto de documento e endereço. Após o cadastro, o cliente faz login na loja e pode gerenciar seu carrinho de compras, adicionando ou removendo produtos. Em seguida, o cliente pode escolher efetuar a compra, onde são oferecidas três formas de pagamento: cartão de crédito, cartão de débito e Pix. Além disso, o diagrama foi atualizado para incluir a funcionalidade de compra em grupo, onde o cliente pode se juntar a outros usuários para realizar uma compra conjunta, compartilhando o carrinho de compras. A loja verifica a disponibilidade e aprova a entrada do cliente no grupo, permitindo que a compra seja concluída.

### Diagrama do aplicativo de estoque

```mermaid
sequenceDiagram
    participant Usuario
    participant Aplicativo
    participant Estoque
    participant Prateleira
    participant Pedido
    participant Relatorio
    participant Dashboard
    participant Notificacoes

    activate Usuario

    Usuario->>Aplicativo: Fazer cadastro
    Aplicativo->>Usuario: Cadastro concluído

    Usuario->>Aplicativo: Fazer login
    activate Aplicativo

    loop Enquanto logado
        
        Usuario->>Aplicativo: Vincular prateleira autônoma
        Aplicativo->>Prateleira: Vincular prateleira ao estoque
        Prateleira-->>Aplicativo: Prateleira vinculada com sucesso

        Usuario->>Aplicativo: Gerenciar produtos em estoque
        Aplicativo->>Estoque: Consultar produtos em estoque
        Estoque-->>Aplicativo: Lista de produtos

        Usuario->>Aplicativo: Adicionar produto em estoque
        Aplicativo->>Estoque: Cadastrar novo produto
        Estoque-->>Aplicativo: Produto adicionado com sucesso

        Usuario->>Aplicativo: Atualizar produto em estoque
        Aplicativo->>Estoque: Atualizar informações do produto
        Estoque-->>Aplicativo: Produto atualizado com sucesso

        Usuario->>Aplicativo: Remover produto em estoque
        Aplicativo->>Estoque: Remover produto do estoque
        Estoque-->>Aplicativo: Produto removido com sucesso

        Usuario->>Aplicativo: Acessar status de pedidos
        Aplicativo->>Pedido: Consultar status de pedidos
        Pedido-->>Aplicativo: Lista de status de pedidos

        Usuario->>Aplicativo: Gerar relatório de vendas
        Aplicativo->>Relatorio: Gerar relatório em PDF
        Relatorio-->>Aplicativo: Relatório gerado com sucesso

        Usuario->>Aplicativo: Acessar dashboard de vendas
        Aplicativo->>Dashboard: Exibir dashboard de vendas
        Dashboard-->>Aplicativo: Dashboard exibido

        Usuario->>Aplicativo: Personalizar notificações
        Aplicativo->>Notificacoes: Configurar preferências de notificação
        Notificacoes-->>Aplicativo: Notificações personalizadas configuradas

        Usuario->>Aplicativo: Solicitar alteração de status da prateleira autônoma
        Aplicativo->>Prateleira: Alterar status da prateleira
        Prateleira-->>Aplicativo: Novo status de funcionamento da prateleira

    end

    deactivate Aplicativo
```

<center>

<p> Figura 4: diagrama de sequência para o aplicativo de estoques do Projeto Integrador 2, Med Grabber(Fonte: autores, 2023).</p>

</center>

Descrevendo o fluxo apresentando na figura, O usuário realiza o cadastro e faz login no aplicativo. Em seguida, o usuário pode vincular uma prateleira autônoma ao aplicativo do estoque. Após a vinculação, o usuário pode gerenciar os produtos em estoque, realizando ações como adicionar, consultar, atualizar e remover produtos. O usuário também pode acessar o status dos pedidos existentes. Além disso, o aplicativo permite a geração de relatórios de vendas em formato PDF e exibe um dashboard de vendas. O usuário pode personalizar as notificações de acordo com suas preferências. Por fim, o usuário pode solicitar a alteração do status de funcionamento da prateleira autônoma, e o aplicativo informa o status atual conforme necessário.

### Composição do Diagrama de Sequência

1. **Participante:** Os objetos ou atores envolvidos na interação são representados como participantes no diagrama.[4]

```mermaid
sequenceDiagram
    participant Cliente
    participant Sistema
```

<center>

<p> Figura 5: exemplo de participante, composição do diagrama de sequência(Fonte: autores, 2023).</p>

</center>

1. **Mensagens:** As mensagens representam a comunicação entre os participantes, indicando as informações trocadas e a ordem em que as mensagens são enviadas.[2]

```mermaid
sequenceDiagram
    Cliente->>Sistema: Seleciona itens da loja
```

<center>

<p> Figura 6: exemplo de mensagem, composição do diagrama de sequência(Fonte: autores, 2023).</p>

</center>

3. **Linhas de vida:** As linhas de vida representam o tempo durante o qual um participante está ativo no sistema.[4]

```mermaid
sequenceDiagram
    participant Cliente
    participant Sistema
    Cliente->>Sistema: Seleciona itens da loja
    activate Sistema
    Sistema->>Sistema: Adiciona itens ao carrinho de compra
    deactivate Sistema

```

<center>

<p> Figura 7: exemplo de linha de vida, composição do diagrama de sequência(Fonte: autores, 2023).</p>

</center>

4. **Ativação:** A ativação é usada para indicar quando um participante está executando uma tarefa específica em resposta a uma mensagem recebida.[4]

```mermaid
sequenceDiagram
    participant Cliente
    participant Sistema
    Cliente->>Sistema: Entra no fluxo de pagamento
    activate Cliente
    Cliente->>Sistema: Seleciona vincular CPF
    activate Sistema
    Sistema->>Cliente: Solicita CPF
    Cliente->>Sistema: Informa CPF
    deactivate Cliente
    Sistema->>Sistema: Processa pagamento
    deactivate Sistema

```

<center>

<p> Figura 8: exemplo de ativação, composição do diagrama de sequência(Fonte: autores, 2023).</p>

</center>

5. **Desvios de condição:** Desvios de condição são usados para indicar fluxos alternativos na sequência de mensagens, dependendo das condições específicas que ocorrem durante a interação.[4]

```mermaid
sequenceDiagram
    participant Cliente
    participant Sistema
    alt Item fora de estoque
        Cliente->>Sistema: Seleciona item
        Sistema->>Cliente: Retorna que item está fora de estoque
    else
        Cliente->>Sistema: Solicita itens
        Sistema->>Sistema: Remove itens do carrinho
        Cliente->>Sistema: Envia solicitação de compra
        Sistema->>Cliente: Confirmação de compra
    end

```

<center>

<p> Figura 9: exemplo de desvio de condicional, composição do diagrama de sequência(Fonte: autores, 2023).</p>

</center>

6. **Anotações:** As anotações são usadas para adicionar informações adicionais ao diagrama, como notas ou explicações sobre a interação.[4]

```mermaid
sequenceDiagram
    participant Cliente
    participant Sistema
    Cliente->>Sistema: Seleciona itens da loja
    note right of Sistema: Adiciona itens ao carrinho
```

<center>

<p> Figura 10: exemplo de anotações, composição do diagrama de sequência(Fonte: autores, 2023).</p>

</center>

<!--Bibitex para referencia

@article{LuLunjin2014Rbos,
  title={Required behavior of sequence diagrams: Semantics and conformance},
  author={Lu, Lunjin and Kim, Dae-Kyoo},
  journal={ACM transactions on software engineering and methodology},
  volume={23},
  number={2},
  pages={1--28},
  year={2014}
}

@misc{IBM,
  title={Sequence diagrams},
  author={IBM},
  howpublished={\url{https://www.ibm.com/docs/pt-br/rsm/7.5.0?topic=uml-sequence-diagrams}},
  year={Acesso em: 27 abr. 2023},
}

-->

# Diagrama de Classes

Os diagramas de classes são usados para descrever a estrutura de um sistema orientado a objetos. Ele representa a estrutura estática do sistema em termos de classes, interfaces, atributos, métodos e relacionamentos entre eles.

As classes são representadas como retângulos, com o nome da classe no topo do retângulo. Os atributos são listados abaixo do nome da classe, enquanto os métodos são listados abaixo dos atributos.

## v1.0

![Diagrama de classes Modelo v1.0](./assets/documento_arquitetura/diagrama_classe_v1.png)

O diagrama indica o modelo do projeto. Esse modelo possui diversas classes que represemtam as funções do sistema.

## Classes

Inventário: representa uma quatidade de um tipo de produto e sua devida localização, com uma id e um objeto do tipo Produto e uma localização x e outra y para saber sua localidade exata.

Estoque: representa uma lista de objetos do tipo Inventário.

Produto: representa um Produto do Inventário, com um id, nome, descrição e preço.

Pagamento: representa o pagamento de um cliente, com um id, um valor total, um status (concluído ou não), e uma informação do cliente.

Braço: representa o controlador do braço robótico, com um objeto do tipo Estoque, que controla a lista de itens, uma localização atual e um status (ocupado ou livre). Tem métodos para receber a localização, pegar um Produto e entrega-lo em uma posição.

# Diagrama de entidade relacional

Um Diagrama de Entidade-Relacionamento (DER) é uma representação gráfica que ilustra as entidades, atributos e relacionamentos entre as entidades de um modelo de dados.O DER permite que os desenvolvedores de banco de dados visualizem e compreendam as relações entre as diferentes entidades em um sistema, e isso pode ajudar a garantir que o modelo de dados seja completo, preciso e fácil de entender.

# v1.0

![Diagrama de entidade relacional v1.0](assets/documento_arquitetura/diagrama_entidade_relacional.png)

O diagrama indica a estrutura do banco que será utilizado no projeto, sendo dividido em 3 tabelas (Produto,Inventario,Transações) onde cada uma contem as colunas nescessarias para o controle do estoque e compra de cada produto.

## Entidades

Produto: representa os produtos oferecidos e contém os atributos id (identificador único do produto), nome, categoria, valor, descrição.

Inventario: representa as informações de cada produto e contém os atributos de idInventario (identificador único do produto dentro do inventario), x-Localização (posição no eixo x do produto), y-Localização (posição no eixo y do produto),quantidade, produto.

Transação: representa as informações de transações feitas e contém os atributos id(identificador único do produto), total, data, cpf, produtos (lista com todos os produtos da compra), status.

# Modelo Relacional

O modelo relacional é uma representação do banco de dados utilizando tabelas, colunas e chaves primárias e estrangeiras, que permitem armazenar e relacionar informações de forma organizada e eficiente.

# v1.0

![Modelo Relacional v1.0](assets/documento_arquitetura/modelagem%20relacional.png)

# Tabelas

## Produto

- idProduto (chave primária)
- nome
- valor
- categoria
- descrição

# Inventário

- idInventario (chave primária)
- idProduto (chave estranjeira)
- xLocalização
- yLocalização
- quantidade

# Transações

- idTransação (chave primária)
- total
- data
- cpf
- status

# Itens_da_compra

- idItens (chave primária)
- idTransação (chave estranjeira)
- idProduto (chave estranjeira)

Cada tabela possui uma chave primária para identificar cada registro de forma única.

Chaves Estrangeiras:

As chaves estrangeiras são utilizadas para relacionar informações entre as tabelas. As chaves estrangeiras são definidas em uma tabela e referenciam a chave primária de outra tabela.

# Referências

- [1] - Clean architecture in flutter part 1. Disponível em: <https://devmuaz.medium.com/flutter-clean-architecture-series-part-1-d2d4c2e75c47>. Acesso em 23 de Abril de 2023.
- [2] - Designing Software Using Clean Architecture: Domain-Driven Design. Disponível em: <https://betterprogramming.pub/how-to-design-in-clean-architecture-way-part-2-8524e76f2720>. Acesso em 23 de Abril de 2023.
- [3] LU, L.; KIM, D.-K. Required behavior of sequence diagrams: Semantics and conformance. ACM Transactions on Software Engineering and Methodology, v. 23, n. 2, p. 1-28, 2014.
- [4] IBM. IBM Rational Software Modeler. Sequence diagrams. Disponível em: https://www.ibm.com/docs/pt-br/rsm/7.5.0?topic=uml-sequence-diagrams. Acesso em: 27 abr. 2023.
- [5] - Pilone, D., & Pitman, N. (2005). UML 2.0 in a Nutshell. O'Reilly Media.
- [6] - Booch, G., Rumbaugh, J., & Jacobson, I. (1999). UML - Guia do Usuário. Bookman.
- [7] - Pilone, D., & Pitman, N. (2005). UML 2.0 in a Nutshell. O'Reilly Media.
- [8] - Booch, G., Rumbaugh, J., & Jacobson, I. (1999). UML - Guia do Usuário. Bookman.
- [9] - TEORY, T. LIGHTSTONE, S., NADEAU, T. and JAGADISH, H. V. Database Modeling and Design: Logical Design. USA: Morgan Kaufmann, 2005
- [10] - SILBERSCHATZ, A., KORTH, H. F. e SUDARSHAN, S. Sistemas de Bancos de Dados. Editora Campus. 2006.
- [11] -Diagramas de Implementação. Disponível em: https://www.ibm.com/docs/pt-br/rsas/7.5.0?topic=topologies-deployment-diagrams. Acesso em: 26 de abr. 2022
- [12] - Diagrama de Implantação .Disponível em: https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-implantacao/. Acesso em: 26 de abr. 2022
- [13] - VISUAL PARADIGM. UML Deployment Diagram. Disponível em: https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-deployment-diagram/. Acesso em: 27 abr. 2023.

## Versionamento

| Versão | Data       | Descrição                                 | Autor(es)        |
| ------ | ---------- | ----------------------------------------- | ---------------- |
| 1.0    | 23/04/2023 | Criação do documento                      | Mauricio Machado |
| 1.1    | 23/04/2023 | Adição do diagrama de pacotes             | Mauricio Machado |
| 1.2    | 27/04/2023 | Adição do diagrama de classes             | Samuel Macedo    |
| 1.3    | 27/04/2023 | Adição do diagrama de entidade relacional | Pedro Moraes     |
| 1.4    | 27/04/2023 | Adição do modelo relacional               | Pedro Moraes     |
| 1.5    | 28/04/2023 | Adição do diagrama de sequência           | Natanael Filho   |
| 1.6    | 28/04/2023 | Correção e Revisaão do Documento Geral    | Davi Mateus      |
| 1.7    | 28/04/2023 | Adição do diagrama de implementação       | Sávio Cunha      |
