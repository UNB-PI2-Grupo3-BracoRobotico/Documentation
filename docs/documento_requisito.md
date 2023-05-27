# Documento de Requisito

<!-- Adicionar explicação do que é o documento de requisito e sua finalidade -->

# Diagrama de Casos de Uso

O diagrama de casos de uso [2] descreve um conjunto de ações, chamados de casos de uso, que um sistema desempenha, levando em consideração os usuários externos ao sistema. Ele pode ser usado para descrever as principais funcionalidades do sistema e a interação com os usuários. </br>

Para a criação desse artefato foi utilizado a abordagem tradicional, ou seja, representação os casos de uso através de uma diagrama UML[1]. A ferramenta utilizada para a criação do diagrama foi o LucidChart [3], um software online para criação de diagramas.

## v2.0

![Diagrama de Casos de Uso Estoque v1.0](./assets/documento_requisito/casos_de_uso_comprador_v1.png)
![Diagrama de Casos de Uso Comprador v1.0](./assets/documento_requisito/casos_de_uso_estoque_v1.png)

## v1.0

[Diagrama de Casos de Uso v1.0](./assets/documento_requisito/diagrama_caso_de_uso_v1.png)

A seguir, a especificação dos casos de uso identificados.

### UC01. Visualizar lista de produtos

|          UC01           |                                                                                                                                                              Visualizar lista de produtos                                                                                                                                                              |
| :---------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                                                     <li> Comprador                                                                                                                                                                     |
|  **Frequência de uso**  |                                                                                                                                                                          Alta                                                                                                                                                                          |
|     **Requisitos**      |                                                                                                                                                            Acesso à internet e conta criada                                                                                                                                                            |
| **Condição de entrada** |                                                                                                        Usuário com conta criada acessa o app. Ao entrar nele será apresentado na tela inicial, que conterá os produtos disponíveis para compra                                                                                                         |
|   **Fluxo principal**   |                                                                                                    <ol> <li> Usuário abre o aplicativo <li> Usuário insere credenciais de acesso <li> Lista de produtos é carregada e apresentada ao usuário </ol>                                                                                                     |
| **Fluxos alternativos** |                                                                                                        <ol> <li> Usuário sem conta abre o aplicativo <li> Usuário cria conta <li> Lista de Produtos é carregada e apresentada ao usuário </ol>                                                                                                         |
|  **Fluxos de exceção**  | **Fluxo 1. Usuário não possui conexão com internet ao acessar área logada** <ol> <li> Usuário faz o processo de login <li> Usuário perde conexão com internet <li> Requisição tentar adquirir a lista de produtos <li> Requisição falha <li> Usuário é apresentado que está sem internet e por isso não foi possível carregar a lista de produtos</ol> |

<div style="text-align: center">
<p> Tabela 1: Especificação do caso de uso: Visualizar lista de produtos. (Fonte: autores, 2023).</p>
</div>

### UC02. Filtrar lista de produtos

|          UC02           |                                                                                                                                                                          Filtrar lista de produtos                                                                                                                                                                          |
| :---------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                                                               <li> Comprador                                                                                                                                                                                |
|  **Frequência de uso**  |                                                                                                                                                                                    Alta                                                                                                                                                                                     |
|     **Requisitos**      |                                                                                                                                                                      Acesso à internet e conta criada                                                                                                                                                                       |
| **Condição de entrada** |                                                                                                                                                            Usuário clica no ícone de adicionar filtro de buscas.                                                                                                                                                            |
|   **Fluxo principal**   |                                                                            <ol> <li> Usuário clica no ícone de adicionar filtro de buscas <li> Usuário seleciona alguns filtros <li> Usuário aplica os filtros <li> Usuário é apresentado com itens que condizem com os filtros aplicados </ol>                                                                             |
| **Fluxos alternativos** | **Fluxo 1. Filtros não tem nenhum item correspondente** <ol> <li> Usuário clica no ícone de adicionar filtro de buscas <li> Usuário seleciona alguns filtros <li> Usuário aplica os filtros <li> Nenhum produto é encontrado que seja condizente com o filtro <li> Usuário é apresentado com uma mensagem explicando que nenhum produto foi encontrado para essa busca</ol> |
|  **Fluxos de exceção**  |                                                                                                                                                                                   Não há                                                                                                                                                                                    |

<div style="text-align: center">
<p> Tabela 2: Especificação do caso de uso: Filtrar lista de produtos. (Fonte: autores, 2023).</p>
</div>

### UC03. Pesquisar produto

|          UC03           |                                                                                                                                             Pesquisar produto                                                                                                                                              |
| :---------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                               <li> Comprador                                                                                                                                               |
|  **Frequência de uso**  |                                                                                                                                                    Alta                                                                                                                                                    |
|     **Requisitos**      |                                                                                                                                      Acesso à internet e conta criada                                                                                                                                      |
| **Condição de entrada** |                                                                                                                                   Usuário clica no botão de fazer busca.                                                                                                                                   |
|   **Fluxo principal**   |                                                                                <ol> <li> Usuário clica no botão de buscas <li> Usuário digita o que está procurando <li> Itens com escrita similar serão apresentados </ol>                                                                                |
| **Fluxos alternativos** | **Fluxo 1. Busca não encontra nenhum produto correspondente ou similar** <ol> <li> Usuário clica no botão de buscas <li> Usuário digita o que está procurando <li> Nenhum item é encontrado <li> Usuário é apresentado com uma mensagem explicando que nenhum produto foi encontrado para essa busca </ol> |
|  **Fluxos de exceção**  |                                        **Fluxo 1. Usuário perde conexão de internet durante a busca** <ol> <li> Usuário perde conexão ao tentar fazer uma busca <li> Usuário é informado de que está sem internet e deve se reconectar para continuar a busca </ol>                                        |

<div style="text-align: center">
<p> Tabela 3: Especificação do caso de uso: Pesquisar produto. (Fonte: autores, 2023).</p>
</div>

### UC04. Visualizar produto

|          UC04           |                                                                                                                                                                                                                                        Visualizar produto                                                                                                                                                                                                                                         |
| :---------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                                                                                                                          <li> Comprador                                                                                                                                                                                                                                           |
|  **Frequência de uso**  |                                                                                                                                                                                                                                               Alta                                                                                                                                                                                                                                                |
|     **Requisitos**      |                                                                                                                                                                                                                                 Acesso à internet e conta criada                                                                                                                                                                                                                                  |
| **Condição de entrada** |                                                                                                                                                                                                                            Usuário seleciona em algum card de produto.                                                                                                                                                                                                                            |
|   **Fluxo principal**   |                                                                                                                                                                                              <ol> <li> Usuário clica no card de produto <li> Usuário é apresentado com os detalhes do produto </ol>                                                                                                                                                                                               |
| **Fluxos alternativos** | **Fluxo 1. Usuário acessa os detalhes de um produto via carrinho** <ol> <li> Usuário acessa o carrinhos de compras <li> Usuário clica em algum dos card de produtos do seu carrinho <li> Usuário é apresentado com os detalhes do produto selecionado </ol> **Fluxo 2. Produto tem estoque zerado enquanto usuário tenta acessar o produto** <ol> <li> Usuário clica em card do produto <li> Usuário é apresentado que o produto não está mais disponível para compra pois está sem estoque </ol> |
|  **Fluxos de exceção**  |                                                                                         **Fluxo 1. Erro ao carregar informações do produto** <ol> <li> Usuário clica no card de detalhes do produto <li> Erro acontece ao tentar carregar os detalhes <li> Usuário é apresentado tela dizendo que o processamento do carregamento do item teve um problema e que ele pode tentar carregar novamente </ol>                                                                                         |

<div style="text-align: center">
<p> Tabela 4: Especificação do caso de uso: Visualizar produto. (Fonte: autores, 2023).</p>
</div>

### UC05. Adicionar produto ao carrinho

|          UC05           |                                                                                                  Adicionar produto ao carrinho                                                                                                   |
| :---------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                          <li> Comprador                                                                                                          |
|  **Frequência de uso**  |                                                                                                               Alta                                                                                                               |
|     **Requisitos**      |                                                                            Acesso à internet, conta criada e estar numa página de detalhe de produtos                                                                            |
| **Condição de entrada** |                                                                                         Usuário clica em adicionar produto ao carrinho.                                                                                          |
|   **Fluxo principal**   |                                                     <ol> <li> Usuário clica em adicionar produto ao carrinho <li> Usuário recebe feedback de sucesso ao adicionar item </ol>                                                     |
| **Fluxos alternativos** |                                                                                                              Não há                                                                                                              |
|  **Fluxos de exceção**  | **Fluxo 1. Estoque inexistente ao clicar em adicionar** <ol> <li> Usuário clica em adicionar produto ao carrinho <li> Usuário recebe feedback de que o produto não está mais disponível para compra pois seu estoque acabou</ol> |

<div style="text-align: center">
<p> Tabela 5: Especificação do caso de uso: Adicionar produto ao carrinho. (Fonte: autores, 2023).</p>
</div>

### UC06. Contatar suporte

|          UC06           |                                                                                             Contatar suporte                                                                                              |
| :---------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                              <li> Comprador                                                                                               |
|  **Frequência de uso**  |                                                                                                   Média                                                                                                   |
|     **Requisitos**      |                                                                                             Acesso à internet                                                                                             |
| **Condição de entrada** |                                                                                     Usuário clica no botão de ajuda.                                                                                      |
|   **Fluxo principal**   |                                            <ol> <li> Usuário clica no botão de ajuda <li> Usuário é redirecionado para página de FAQ e abertura de chat </ol>                                             |
| **Fluxos alternativos** |                                                                                                  Não há                                                                                                   |
|  **Fluxos de exceção**  | **Fluxo 1. Sem internet** <ol> <li> Usuário clica no botão de ajuda <li> Usuário é redirecionado para página apresentando que ele está sem internet e que deve se reconectar para poder obter ajuda </ol> |

<div style="text-align: center">
<p> Tabela 6: Especificação do caso de uso: Contatar suporte. (Fonte: autores, 2023).</p>
</div>

### UC07. Realizar compras em grupo

|          UC07           |                                                                             Realizar compras em grupo                                                                             |
| :---------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                  <li> Comprador                                                                                   |
|  **Frequência de uso**  |                                                                                       Média                                                                                       |
|     **Requisitos**      |                                                                          Acesso à internet, conta criada                                                                          |
| **Condição de entrada** |                                                                            Pedir entrada em um grupo.                                                                             |
|   **Fluxo principal**   |                       <ol> <li> Usuário pede acesso a um grupo de compra <li> Usuário é aceito e pode adicionar itens no carrinho da compra em grupo </ol>                        |
| **Fluxos alternativos** | **Fluxo 1. Usuário tem acesso negado ao grupo** <ol> <li> Usuário pede acesso a um grupo de compra <li> Acesso é negado e usuário recebe esse feedback via notificação push </ol> |
|  **Fluxos de exceção**  |                                                                                      Não há                                                                                       |

<div style="text-align: center">
<p> Tabela 7: Especificação do caso de uso: Realizar compras em grupo. (Fonte: autores, 2023).</p>
</div>

### UC08. Criação de conta

|          UC08           |                                                                                                                                                   Criação de conta                                                                                                                                                    |
| :---------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                                    <li> Comprador                                                                                                                                                     |
|  **Frequência de uso**  |                                                                                                                                                         Alta                                                                                                                                                          |
|     **Requisitos**      |                                                                                                                          Acesso à internet, número de documento não utilizado no aplicativo                                                                                                                           |
| **Condição de entrada** |                                                                                                                                          Usuário clica no botão de cadastro.                                                                                                                                          |
|   **Fluxo principal**   |                                                                                <ol> <li> Usuário insere informações de usuário <li> Usuário faz a validação de identidade <li> Usuário é redirecionado para a home do aplicativo </ol>                                                                                |
| **Fluxos alternativos** |                                                                   **Fluxo 1. Usuário tem acesso negado ao grupo** <ol> <li> Usuário pede acesso a um grupo de compra <li> Acesso é negado e usuário recebe esse feedback via notificação push </ol>                                                                   |
|  **Fluxos de exceção**  | **Fluxo 1. Usuário usa informação usada em outro cadastro (número de documento ou email)** <ol> <li> Usuário adiciona informação que já foi usada em outro cadastro e não pode se repetir <li> Usuário recebe feedback sobre isso e é avisado que enquanto não arrumar isso não conseguirá finalizar o cadastro </ol> |

<div style="text-align: center">
<p> Tabela 8: Especificação do caso de uso: Criação de conta. (Fonte: autores, 2023).</p>
</div>

### UC09. Finalizar carrinho

|          UC09           |                                                                                                                                                                                                                                          Finalizar carrinho                                                                                                                                                                                                                                          |
| :---------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                                                                                                                            <li> Comprador                                                                                                                                                                                                                                            |
|  **Frequência de uso**  |                                                                                                                                                                                                                                                 Alta                                                                                                                                                                                                                                                 |
|     **Requisitos**      |                                                                                                                                                                                                                    Acesso à internet, conta criada, carrinho com ao menos um item                                                                                                                                                                                                                    |
| **Condição de entrada** |                                                                                                                                                                                                                             Usuário clica no botão de finalizar compra.                                                                                                                                                                                                                              |
|   **Fluxo principal**   |                                                                                          <ol> <li> Usuário clica no botão de finalizar compra. <li> Sistema valida se todos os itens do carrinho ainda estão disponíveis <li> Usuário procede para inserção de informações de pagamento <li> Usuário clica em confirmar pedido <li> Carrinho é finalizado e processo de construção do pedido iniciado </ol>                                                                                          |
| **Fluxos alternativos** |                                                         **Fluxo 1. Usuário já possui método de pagamento registrado** <ol> <li> Usuário clica no botão de finalizar compra. <li> Sistema valida se todos os itens do carrinho ainda estão disponíveis <li> Usuário seleciona método de pagamento previamente cadastrado <li> Usuário clica em confirmar pedido <li> Carrinho é finalizado e processo de construção do pedido iniciado </ol>                                                          |
|  **Fluxos de exceção**  | **Fluxo 1. Sem internet** <ol> <li> Usuário clica no botão de finalizar compra <li> Usuário é redirecionado para página explicando que ele está sem sinal e deve se reconectar para finalizar o pedido. </ol> **Fluxo 2. Itens do carrinho não estão mais disponíveis** <ol> <li> Usuário clica no botão de finalizar compra <li> Sistema verifica se todos os pedidos estão disponíveis <li> Usuário é informado que determinados itens não estão mais disponíveis e serão portanto removidos </ol> |

<div style="text-align: center">
<p> Tabela 9: Especificação do caso de uso: Finalizar carrinho. (Fonte: autores, 2023).</p>
</div>

### UC10. Acompanhar pedido

|          UC10           |                                                                                                                                                                                                         Acompanhar pedido                                                                                                                                                                                                         |
| :---------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                                                                                          <li> Comprador                                                                                                                                                                                                           |
|  **Frequência de uso**  |                                                                                                                                                                                                               Alta                                                                                                                                                                                                                |
|     **Requisitos**      |                                                                                                                                                                                       Acesso à internet, conta criada, pedido em progresso                                                                                                                                                                                        |
| **Condição de entrada** |                                                                                                                                                                                                 Usuário clica na aba dos pedidos.                                                                                                                                                                                                 |
|   **Fluxo principal**   |                                                        <ol> <li> Usuário clica no botão de finalizar compra. <li> Sistema valida se todos os itens do carrinho ainda estão disponíveis <li> Usuário procede para inserção de informações de pagamento <li> Usuário clica em confirmar pedido <li> Carrinho é finalizado e processo de construção do pedido iniciado </ol>                                                         |
| **Fluxos alternativos** | **Fluxo 1. Sem pedidos em andamento** <ol> <li> Usuário clica na aba dos pedidos. <li> Usuário não possui pedidos em progresso <li> Usuário é apresentado uma tela com histórico de pedidos já finalizados </ol> **Fluxo 2. Sem pedidos realizados** <ol> <li> Usuário clica na aba dos pedidos. <li> Usuário não possui pedidos <li> Usuário é apresentado uma tela informando usuário que ele ainda não fez nenhum pedido </ol> |
|  **Fluxos de exceção**  |                                                                                                                                                                                                              Não há                                                                                                                                                                                                               |

<div style="text-align: center">
<p> Tabela 10: Especificação do caso de uso: Acompanhar pedido. (Fonte: autores, 2023).</p>
</div>

### UC11. Cancelar Pedido

|          UC11           |                                                                                                                                Cancelar Pedido                                                                                                                                 |
| :---------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                 <li> Comprador                                                                                                                                 |
|  **Frequência de uso**  |                                                                                                                                      Alta                                                                                                                                      |
|     **Requisitos**      |                                                                                                              Acesso à internet, conta criada, pedido em progresso                                                                                                              |
| **Condição de entrada** |                                                                                                                  Usuário clica na botão de cancelar o pedido.                                                                                                                  |
|   **Fluxo principal**   |           <ol> <li> Usuário clica na botão de cancelar o pedido. <li> Usuário apresenta justificativa para cancelamento do pedido <li> Pedido é enviado ao sistema <li> Chat é aberto com suporte <li> Usuário conversa com analista o motivo do cancelamento </ol>            |
| **Fluxos alternativos** |                                                                                                                                     Não há                                                                                                                                     |
|  **Fluxos de exceção**  | **Fluxo 1. Impossibilidade de cancelar o pedido** <ol> <li> Usuário clica em cancelar pedido <li> Usuário não possui conexão com Internet <li> Usuário é apresentado uma tela que informa que não possui conexão e que portanto o pedido de cancelamento não foi enviado </ol> |

<div style="text-align: center">
<p> Tabela 11: Especificação do caso de uso: Cancelar Pedido. (Fonte: autores, 2023).</p>
</div>

### UC12. Configurar Estoque

|          UC12           |                                                                                                                                                                                  Configurar Estoque                                                                                                                                                                                   |
| :---------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                                                                    <li> Estoquista                                                                                                                                                                                    |
|  **Frequência de uso**  |                                                                                                                                                                                         Baixa                                                                                                                                                                                         |
|     **Requisitos**      |                                                                                                                                                                            Acesso à internet, conta criada                                                                                                                                                                            |
| **Condição de entrada** |                                                                                                                                                                     Usuário clica no botão de configurar máquina.                                                                                                                                                                     |
|   **Fluxo principal**   | <ol> <li> Usuário clica no botão de configurar máquina <li> Usuário faz o pareamento da máquina <li> Máquina é pareada <li> Usuário é instruído em montar a máquina nas estantes proprietárias <li> Usuário confirma que máquina está instalada <li> Sistema mapeia cubículos disponíveis <li> Mapemanto é concluído e usuário é informado que seu estoque está pronto para uso </ol> |
| **Fluxos alternativos** |                                                                                                                                                                                        Não há                                                                                                                                                                                         |
|  **Fluxos de exceção**  |                           **Fluxo 1. Impossibilidade de parear máquina** <ol> <li> Usuário clica no botão de configurar máquina <li> Usuário não consegue parear com máquina <li> Usuário é informado sobre falha no pareamento e instruído a ler a documentação para ajudá-lo <li> Usuário é redirecionado a um FAQ sobre pareamento da máquina <li> </ol>                           |

<div style="text-align: center">
<p> Tabela 12: Especificação do caso de uso: Configurar Estoque. (Fonte: autores, 2023).</p>
</div>

### UC13. Gerenciar Estoque

|          UC13           |                                                                                                                                                                                                                                                     Gerenciar Estoque                                                                                                                                                                                                                                                      |
| :---------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                                                                                                                                                      <li> Estoquista                                                                                                                                                                                                                                                       |
|  **Frequência de uso**  |                                                                                                                                                                                                                                                            Alta                                                                                                                                                                                                                                                            |
|     **Requisitos**      |                                                                                                                                                                                                                                    Acesso à internet, conta criada, estoque configurado                                                                                                                                                                                                                                    |
| **Condição de entrada** |                                                                                                                                                                                                                         Usuário clica no mapa bidimensional do estoque e escolhe um dos cubículos.                                                                                                                                                                                                                         |
|   **Fluxo principal**   |                                                                                                                                                         <ol> <li> Usuário clica no mapa bidimensional do estoque e escolhe um dos cubículos. <li> Usuário edita as informações do produto naquele cubículo <li> Usuário clica no botão de salvar alterações </ol>                                                                                                                                                          |
| **Fluxos alternativos** | **Fluxo 1. Adicionar item** <ol> <li> Usuário clica no mapa bidimensional do estoque e escolhe um dos cubículos. <li> Cubículo está vazio <li> Usuário clica em adicionar produto <li> Usuário adiciona novo produto e relaciona a essa cubículo <li> Usuário salva as informações </ol> **Fluxo 2. Remover item** <ol> <li> Usuário clica no mapa bidimensional do estoque e escolhe um dos cubículos. <li> Cubículo está populado com um item <li> Usuário clica em remover item <li> Usuário salva as informações </ol> |
|  **Fluxos de exceção**  |                                                                                                 **Fluxo 1. Impossibilidade de visualizar estoque** <ol> <li> Usuário acessa a home do aplicativo <li> Sistema tenta adquirir informação de estoque <li> Sistema não consegue carregar informação do estoque <li> Usuário é informado que houve algum erro no carregamento e o orienta a tentar novamente mais tarde </ol>                                                                                                  |

<div style="text-align: center">
<p> Tabela 13: Especificação do caso de uso: Gerenciar Estoque. (Fonte: autores, 2023).</p>
</div>

### UC14. Criação de alertas para itens que estão acabando no estoque

|          UC14           |                                                                                                     Criação de alertas para itens que estão acabando no estoque                                                                                                     |
| :---------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       **Atores**        |                                                                                                                           <li> Estoquista                                                                                                                           |
|  **Frequência de uso**  |                                                                                                                                Média                                                                                                                                |
|     **Requisitos**      |                                                                                         Acesso à internet, conta criada, estoque configurado, ao menos um cubículo com item                                                                                         |
| **Condição de entrada** |                                                                                             Usuário seleciona cubículo no mapa do estoque que possua item relacionado.                                                                                              |
|   **Fluxo principal**   | <ol> <li> Usuário seleciona cubículo no mapa do estoque que possua item relacionado <li> Usuário clica no ícone de notificações na página de detalhes do cubículo <li> Usuário configura alerta para cubículo e item relacionado <li> Usuário salva alterações</ol> |
| **Fluxos alternativos** |                                                                                                                               Não há                                                                                                                                |
|  **Fluxos de exceção**  |                                                                                                                               Não há                                                                                                                                |

<div style="text-align: center">
<p> Tabela 14: Especificação do caso de uso: Gerenciar Estoque. (Fonte: autores, 2023).</p>
</div>

# Brainstorm

O brainstorm é uma técnica utilizada para levantar requisitos e aprender sobre novas características que os usuários apreciariam em um produto. Essa técnica tem como objetivo incentivar a criatividade do usuário a partir da filosofia de que cada um é livre para opinar e apresentar suas ideias acerca do que deve ser melhorado, sem julgamentos nem cobranças. Buscando assim, levantar o máximo de opiniões em torno de um tema.

| Membros Participantes |
| :-------------------: |
|   Mauricio Machado    |

O identificador de cada requisito é formado por 'B' mais uma letra entre 'C' ou 'E' para indicar consumidor ou estoque, e mais um número, sendo 'B' uma abreviação de Brainstorm, e o tipo de requisito refere-se à classificação entre requisitos funcionais (RF) e não funcionais (RNF).

Como resultado das reuniões e pesquisas, nós obtivemos o temas de requisitos funcionais e não funcionais representados na Tabela 1.

| Identificador | Requisito                                                                                                                                                | Tipo |
| :-----------: | -------------------------------------------------------------------------------------------------------------------------------------------------------- | :--: |
|      BE1      | Usuário deve conseguir visualizar a quantidade dos produtos no estoque.                                                                                  |  RF  |
|      BE2      | Usuário deve conseguir solicitar retirada de produtos do estoque.                                                                                        |  RF  |
|      BE3      | Usuário deve ser capaz de registrar produtos no estoque.                                                                                                 |  RF  |
|      BE4      | Usuário deve ser capaz de editar produtos presentes no estoque.                                                                                          |  RF  |
|      BE5      | Usuário pode emitir um relatório de venda dos produtos.                                                                                                  |  RF  |
|      BE6      | Usuário pode customizar alertas sobre itens cujo o estoque esteja acabando.                                                                              |  RF  |
|      BE7      | Usuário deve ser capaz de registrar o estoque disponível no aplicativo.                                                                                  |  RF  |
|      BE8      | Usuário deve ser capaz de verificar a performance de vendas em períodos de tempo selecionados.                                                           |  RF  |
|      BE9      | Usuário deve ser informado sobre valor total do estoque.                                                                                                 |  RF  |
|     BE10      | Usuário deve ser informado qual seu produto mais performático em um período de tempo selecionado.                                                        |  RF  |
|     BE11      | Usuário deve logar toda adição de itens ao estoque.                                                                                                      |  RF  |
|     BE11      | Usuário pode verificar hisórico de adições no estoque.                                                                                                   |  RF  |
|     BE12      | Usuário pode verificar histórico de vendas.                                                                                                              |  RF  |
|     BE13      | Usuário pode visualizar o mapeamento dos produtos de cada prateleira.                                                                                    |  RF  |
|     BE14      | Usuário deve ter acesso ao status de operação da máquina.                                                                                                |  RF  |
|     BE15      | Usuário pode sobreescrever o status de operação da máquina.                                                                                              |  RF  |
|     BE16      | Sistema deve ter acesso a energia.                                                                                                                       | RNF  |
|     BE17      | Sistema deve ter conexão a internet.                                                                                                                     | RNF  |
|     BE18      | Sistema deve apresentar produtos populares.                                                                                                              | RNF  |
|     BE19      | Sistema deve dar feedback de interação em até 5 segundos.                                                                                                | RNF  |
|     BE20      | Sistema deve proteger as informações do usuário e as transações contra acessos não autorizados.                                                          | RNF  |
|     BE21      | Sistema deve registrar as vendas e atualizar o estoque automaticamente após cada transação.                                                              | RNF  |
|     BE23      | Sistema deve assegurar conformidade de dados com LGPD.                                                                                                   | RNF  |
|     BE24      | Aplicativo deve estar disponível em Android.                                                                                                             | RNF  |
|     BE25      | Sistema deve cessar operação quando uma pessoa estiver presente no mesmo recinto que a máquina.                                                          | RNF  |
|     BE26      | Sistema deve enfileirar pedidos em caso de indisponibilidade de pontos de entrega.                                                                       | RNF  |
|      BP1      | Usuário pode filtrar a lista de produtos.                                                                                                                |  RF  |
|      BP2      | Usuário deve poder visualizar a lista de todos os produtos.                                                                                              |  RF  |
|      BP3      | Usuário pode fazer o pagamento com cartão digital (débito).                                                                                              |  RF  |
|      BP4      | Usuário pode fazer o pagamento com cartão digital (crédito).                                                                                             |  RF  |
|      BP5      | Usuário pode fazer o pagamento via PIX.                                                                                                                  |  RF  |
|      BP6      | Usuário deve realizar cadastro.                                                                                                                          |  RF  |
|      BP7      | Usuário pode adicionar produtos ao carrinho.                                                                                                             |  RF  |
|      BP8      | Usuário deve validar identidade.                                                                                                                         |  RF  |
|      BP9      | Usuário deve validar identidade.                                                                                                                         |  RF  |
|     BP10      | Usuário pode pesquisar um produto.                                                                                                                       |  RF  |
|     BP11      | Usuário pode verificar o status do pedido.                                                                                                               |  RF  |
|     BP12      | Usuário pode iniciar um chat em tempo real.                                                                                                              |  RF  |
|     BP13      | Usuário pode acessar área FAQ e chat.                                                                                                                    |  RF  |
|     BP14      | Usuário deve ter acesso ao valor total da sua compra.                                                                                                    |  RF  |
|     BP15      | Usuário pode fazer compras em grupo.                                                                                                                     |  RF  |
|     BP16      | Usuário recebe notificações.                                                                                                                             |  RF  |
|     BP17      | Usuário pode fazer informações do produto serem lidas para ele.                                                                                          |  RF  |
|     BP18      | Sistema deve proteger as informações do usuário e as transações contra acessos não autorizados.                                                          | RNF  |
|     BP19      | Sistema deve ter conexão a internet.                                                                                                                     | RNF  |
|     BP20      | Sistema deve ter contraste adequado entre a fonte de texto e a cor de fundo de modo que usuários com distúrbios de visão possam ler as informações.      | RNF  |
|     BP21      | Sistema deve guardar informações em conformidade com a LGPD.                                                                                             | RNF  |
|     BP22      | Sistema deve ser disponível para plataformas Mobile Android.                                                                                             | RNF  |
|     BP23      | Em sua primeira compra, 65% dos usuários devem ser capazes de efetivar sem precisar de entrar em contato com o suporte.                                  | RNF  |
|     BP24      | Sistema  deve reembolsar o usuário que cancelar a compra sem justificativa em até 5 minutos.                                                             | RNF  |
|     BP25      | Sistema deve ser capaz de identificar se cpf é válido.                                                                                                   | RNF  |
|     BP26      | Sistema deve validar identidade facial do usuário e sua relação com o cpf cadastrado.                                                                    | RNF  |
|     BP27      | Sistema deve ser desenvolvido de forma responsiva, adaptando a aparência e funcionalidade do sistema às diferentes telas e tamanhos de dispositivos.     | RNF  |
|     BP28      | O aplicativo deve ser intuitivo, sendo consistente em toda a interface de usuário, garantindo que o usuário possa prever o que acontecerá em cada etapa. | RNF  |
|     BP29      | Sistema deve dar feedback de interação em até 5 segundos.                                                                                                | RNF  |

## Requisitos Elicitados

# Introspecção

## Introdução

<p style="text-align: justify; text-indent: 20px">A introspecção é uma técnica essencialmente voltada para especialistas em requisitos, que devem extrair as melhores informações por meio de uma análise profunda sobre como e quais requisitos são necessários para satisfazer os usuários e stakeholders do sistema. Embora seja uma técnica rica em detalhes e informações, pode não ser adequada quando não é um especialista da área realizando-a. No entanto, mesmo que não seja um especialista, ainda pode ser útil realizar a técnica de introspecção para extrair o máximo de suas vantagens e obter informações valiosas para o projeto. </p>
<p style="text-align: justify; text-indent: 20px">
A técnica utilizada consiste em o engenheiro de requisitos utilizar a imaginação como principal ferramenta, colocando-se no lugar do usuário do sistema e imaginando o que ele gostaria de realizar ao desempenhar determinadas atividades no sistema. Dessa forma, é possível obter informações valiosas sobre as necessidades e desejos dos usuários, contribuindo para a elaboração de requisitos mais precisos e efetivos para o projeto.
</p>

## Metodologia

<p style="text-align: justify; text-indent: 20px"> A fim de elaborar o artefato de requisitos, cada membro do grupo utilizou individualmente a técnica da introspecção para elicitar requisitos, os quais foram posteriormente compilados em um único artefato, eliminando duplicações de requisitos. Dessa forma, foi possível obter uma visão geral dos requisitos desejados pelos stakeholders do projeto, evitando redundâncias e garantindo a precisão das informações coletadas</p>

## Requisitos levantados

<p style="text-align: justify; text-indent: 20px"> 
    A partir dos dados obtidos pelo brainstorming foi possível levantar possíveis requisitos da aplicação.
</p>
<p style="text-align: justify; text-indent: 20px"> 
    Dessa forma, foram detectados os seguintes requisitos:
</p>

| ID  | Descrição                                                                                                                                                                                                                      | Tipo de Requisito |
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| I01 | O sistema deverá identificar a localização inicial do produto                                                                                                                                                                  | RF                |
| I02 | O sistema deverá indicar quais produtos estão sem estoque                                                                                                                                                               | RF                |
| I03 | O sistema deve ser capaz de integrar-se a mídias sociais, sendo elas o google ou o Facebook.  | RF                |
| I04 | O usuário poderá acompanhar o status do pedido                                                                                                                                                                | RF                |
| I05 | O sistema deve permitir que os usuários comparem produtos ou serviços com base no seu preço e  na sua qualidade.                                                                                   | RF                |
| I06 |  O sistema deve permitir que os usuários vejam o histórico de pedidos.                                                                                                                      | RF                |
| I07 | O usuário deve criar uma conta para poder verificar os produtos e realizar compras no aplicativo | RF                |
| I08 | O usuário para poder iniciar um processo de compra ele deve ter o status de validação de identidade como aprovado| RF                | 
| I09 | O usuário durante a criação da conta,  deve informar: seu email, cpf e senha| RF                |
| I10 | O sistema deve validar a identidade facial do usuário com o número de documento inserido durante o cadastro.                                                                                                                                                             | RF                |
| I11 |  O aplicativo deve fornecer um canal de suporte ao cliente para resolver quaisquer problemas ou dúvidas relacionadas ao pedido sendo necessário incluir um chat em tempo real.                                      | RF                |
| I12 |  O aplicativo deve fornecer uma sessão de FQ para que os usuarios possam ter suas perguntas respondidas.                                    | RF                |
| I13 | O usuário poderá visualizar via dashboard qual é o produto que mais vende no seu estoque num determinado período de tempo.                                                                                                                                       | RF                |
| I14 | O sistema deve permitir que os usuários concluam uma compra, inserindo informações de pagamento e endereço de entrega                                                                                                          | RF                |
| I15 | O sistema deverá informar para o Usuário quando os itens em estoque estejam acabando.                                                                                                                                        | RF                |
| I16 | O sistema deve identificar a profundidade de um produto através de um QR Code presente em cada caixa que irá conter os produtos.                                                                                                                                                 | RF                |
| I17 | O sistema deve fornecer ao estoquista os itens mais vendidos do estoque                                                                                                                                                        | RF                |
| I18 | O usuário poderá fazer o cancelamento do pedido no período de 5 minutos, após esse período o reembolso só acontecerá caso o usuário houver uma justificativa.                                                                                     | RNF               |
| I19| O sistema deve impedir o funcionamento do sistema enquanto estiver sendo feito a reposição de estoque                                                                                                                          | RNF               |
| I20 | O sistema deve ser responsivo  se adaptando  às diferentes telas e tamanhos de dispositivos.                                                                                                                                                                                                | RNF               |
| I21 | O aplicativo deve ser intuitivo, sendo consistente em toda a interface de usuário, garantindo que o usuário possa prever o que acontecerá em cada etapa                                                                                                                                                                                          | RNF               |
| I22 | O aplicativo deve fornecer feedback instantâneo sobre as ações do usuário, permitindo que o usuário saiba o que está acontecendo em tempo real                                                                                                                                                                                                | RNF               |
| I23 | O sistema deve impedir o funcionamento enquanto o usuário estiver pegando seu produto.                                                                                                                                         | RNF               |
| I24 | O Sistema deve ter um manual de operação/usuário.                                                                                                                               | RNF               |
| I25 |O sistema deve possuir uma  cobertura de teste de pelo menos 75% a fim de ajudar na manutenção do código.                                                                                                                               | RNF               |

<h6 align = "center">Tabela 1: Tabela contendo os requisitos levantados pela introspecção</h6>
<h6 align = "center">Fonte: Autor</h6>

<center>

| Legenda |        Descrição        |
| :-----: | :---------------------: |
|    I    |      Introspecção       |
|   RF    |   Requisito Funcional   |
|   RNF   | Requisito Não Funcional |

<h6>Tabela 2: Legenda dos acrônimos contidos na Tabela 1</h6>
<h6>Fonte: Autor</h6>

</center>

# Referências

[1] DevMedia. O que é UML e Diagramas de Caso de Uso: Introdução Prática à UML. 2012. DevMedia. Disponível em: <https://www.devmedia.com.br/o-que-e-uml-e-diagramas-de-caso-de-uso-introducao-pratica-a-uml/23408>. Acessado em 07 de dez. de 2022.

[2] IBM. Diagramas de Caso de Uso. IBM. Disponível em: <https://www.ibm.com/docs/pt-br/rsm/7.5.0?topic=diagrams-use-case>. Acessado em 07 de dez. de 2022

[3] Ferramenta Lucidchart, disponível no [link](https://www.lucidchart.com/pages/pt). Acessado em 07 de dez. de 2022.

[4] DevMedia. Especificação de Casos de Uso na Prática. 2010. DevMedia. Disponível em no [link](https://www.devmedia.com.br/especificacao-de-casos-de-uso-na-pratica/18427). Acessado em 09 de dez. de 2022.

[5] - SERRANO, Maurício; SERRANO, Milene. Disponível em: Requisitos - Aula 07. 1º/2019. 50 slides. Material apresentado para a disciplina de Requisitos de Software no curso de Engenharia de Software da UnB, FGA.

[6] - ANDRADE DE MORAIS, E. Utilização de uma estratégia para Identificação de fontes de informação na fase de Elicitação. Doutorado—[s.l.] Pontifícia Universidade Católica Do Rio De Janeiro, 2021.
| 1.4     | 10/05/2023 | Melhoramento e adequação da introspecção de acordo com o novo escopo | Davi Matheus, Natanael                        |

## Histórico de Versão<br>

| Versão | Data       | Descrição                                           | Autor(es)                                                |
| ------ | ---------- | --------------------------------------------------- | -------------------------------------------------------- |
| 1.0    | 23/04/2023 | Criação do documento                                | Mauricio Machado                                         |
| 1.1    | 23/04/2023 | Adição do diagrama de casos de uso e sua explicação | Mauricio Machado                                         |
| 1.2    | 26/04/2023 | Adição dos requisitos via brainstorm                | Mauricio Machado, Davi Matheus, Filipe Machado, Natanael |
| 1.3    | 27/04/2023 | Adição dos requisitos via introspecção              | Davi Matheus                                             |
| 1.4    | 10/05/2023 | Melhoramento e adequação da introspecção de acordo com o novo escopo | Davi Matheus, Natanael                  |
| 1.5    | 12/05/2023 | Refatoração requisitos de brainstorm                | Mauricio Machado, Davi Matheus, Natanael, Pedro Henrique |
| 1.6    | 17/05/2023 | Refatoração requisitos casos de uso                 | Mauricio Machado                                         |

