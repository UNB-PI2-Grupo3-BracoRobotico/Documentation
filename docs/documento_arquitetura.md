# Introdução

<!-- Adicionar explicação do que é o documento de arquitetura e sua finalidade -->

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

# Diagrama de implementação

O Diagrama de Implementação é uma representação visual que mostra a estrutura física da arquitetura de um sistema de software. Ele se concentra na organização do ambiente físico em que o software será implantado e executado, incluindo o hardware necessário, como computadores pessoais e servidores que suportarão o sistema. O diagrama é a visão mais tangível da UML e ajuda a entender como os diferentes componentes do sistema se relacionam entre si em termos físicos.

O Diagrama de Implementação será usado para descrever a conexão das máquinas e os protocolos de comunicação utilizados para transferir informações. O objetivo é obter uma visão clara da implementação do software, o que facilita o processo de desenvolvimento, uma vez que a modelagem é focada em um nível arquitetural mais específico em relação ao hardware. Com o Diagrama de Implementação, é possível entender como os componentes do sistema se interconectam fisicamente e quais recursos de hardware são necessários para executar o software. Dessa forma, é possível identificar e resolver problemas de desempenho ou escalabilidade antes de implementar o sistema, o que pode economizar tempo e recursos. O diagrama também ajuda a comunicar a arquitetura do sistema para as partes interessadas de forma clara e eficaz.

## v1.0

![Versão v1.0 do 5W2H](./assets/documento_arquitetura/diagrama_implementacao.png)

A primeira versão desse diagrama se concentrou em um nível de desenvolvimento e tangibilizou uma implantação mais simples. Partindo dessa perspectiva, temos o servidor da aplicação englobando o ambiente do Front End, Back End e o Banco de Dados rodando localmente. 

## v2.0

![Versão v1.0 do 5W2H](./assets/documento_arquitetura/diagrama_implementacaoV2.png)

A segunda versão desse diagrama apresenta todos os ambientes estão dentro do container do Docker. O acesso é feito pelo protocolo HTTP a partir de navegadores e do protocolo TCP/IP para comunicação com o Banco de Dados.


# Referências

- [1] - Clean architecture in flutter part 1. Disponível em: <https://devmuaz.medium.com/flutter-clean-architecture-series-part-1-d2d4c2e75c47>. Acesso em 23 de Abril de 2023.
- [2] - Designing Software Using Clean Architecture: Domain-Driven Design. Disponível em: <https://betterprogramming.pub/how-to-design-in-clean-architecture-way-part-2-8524e76f2720>. Acesso em 23 de Abril de 2023.
- [3] -Diagramas de Implementação. Disponível em: https://www.ibm.com/docs/pt-br/rsas/7.5.0?topic=topologies-deployment-diagrams. Acesso em: 26 de abr.  2022
- [4] - Diagrama de Implantação .Disponível em: https://creately.com/blog/pt/diagrama/tutorial-do-diagrama-de-implantacao/. Acesso em: 26 de abr.  2022
- [5] - VISUAL PARADIGM. UML Deployment Diagram. Disponível em: https://www.visual-paradigm.com/guide/uml-unified-modeling-language/uml-deployment-diagram/. Acesso em: 27 abr. 2023.

## Histórico de Versão<br>
|    Data    | Versão | Descrição            | Autor(es)       |
| :- | :- | :- | :- |
| 27.04.2022 |  0.1   | Criação do diagrama de implementação | [Sávio Cunha](https://github.com/savioc2) |