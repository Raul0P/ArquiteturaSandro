# Usano markdown, que é isso aqui kappa.

*guiazinho do markdown e suas features: https://code.visualstudio.com/docs/languages/markdown*

**Sintaxe básica:**



importancia do readme em seu projeto/repo, pra entender todo o contexto dessa aplicação.

## Estilos Aquiteturais https://www.canva.com/design/DAGLliICAKQ/yMvfg3Vkbr4K_0FTKyfyBg/edit

- São abordagens de desing amplas que definem a estrutura e a organização de sistemas de software. Fornecem uma visão geral da estrutura de um sistema e como seus componentes interagem.
- Eles descrevem umas estrutura de alto nível para organizar os componentres de um sistema, suas interações e as restrições que guiam o desenvolvimento e a evolução do sistema 


Quais os benefícios:

- Reutilização: permitem a reutilização de soluções testadas e comprovadas para problemas recorrentes, aumentando a eficiencia do desenvolvimento;
- Compreensão e Comunicação.
- Flexibilidade e Escabilidade: Fácil a evolução do código.
- Padronização.
- Facilidade de Manutenção: facil acesso aos componentes do sistema.

Component-based:
 - Fowler descreve Component-Based Architecture como uma abordagem para
organizar sistemas de software em componentes reutilizáveis, que podem ser
desenvolvidos e implantados de forma independente. modularização.

- Principais beneficios: 
    - Reutilização & Facilidade de Manutenção

Exemplos de Component-based

- Sistema de gestão empresarial (ERP) - Monólito modular
- Plataforma de comércio eletrônico - Magento, Shopify.
- Sistema de gerenciamento de conteúdo(CMS) - WordPress, Drupal.
- Componentes em aplicações web
- E Microserviços? 
      - No livro "Building Microservices: Designing Fine-Grained Systems", Sam
Newman argumenta que os microsserviços são uma extensão natural dos
princípios de Component-Based Architecture, aplicada ao
desenvolvimento de sistemas distribuídos modernos.

    - Recomendação de Artigo: https://www.thoughtworks.com/en-us/insights/blog/microservices/modular-monolith-better-way-build-software

    - Citação: "Microservices are a form of component-based architecture
where the components are services that are independently deployable
and scalable."

**Layered & N-tiers**

*Layered, divisão lógica*

- É uma abordagem onde o sistema é organizado em camadas, cada uma com
responsabilidades específicas e interações bem definidas. Este estilo promove a separação
de preocupações, facilitando o desenvolvimento, a manutenção e a evolução do software.

- Fowler descreve a arquitetura em camadas como um padrão
estrutural comum em aplicações empresariais, dividindo a
aplicação em camadas como apresentação, aplicação, domínio
e infraestrutura. Ele defende padrões específicos que se encaixam
na arquitetura em camadas, como "Presentation Layer," "Domain
Layer" e "Data Source Layer".

- Em resumo, vai possuir uma interação com o usuário, seja ela
qual for, vai possuir um domínio e vai ter uma camada de acesso
a dados. 

*N-tiers, divisão física*

- Refere-se à separação física das diferentes camadas da aplicação, onde cada
nível pode ser distribuído em diferentes máquinas ou servidores. Esse estilo é
focado na distribuição e escalabilidade do sistema.

- A separação física permite que cada
nível seja escalado de forma
independente, aumentando a
capacidade do sistema de lidar com
uma maior carga de trabalho.

Em discussões de arquitetura de três camadas(tier), o nível é frequentemente usado de forma intercambiável e equivocadamente pela camada, como um 'nível de apresentação' ou 'nível lógico de negócios'. Não são o mesmo!

    - TIER (NÍVEL): Refere-se normalmente a uma divisão física do software executada em infraestrutura separada das outras divisões.
    
    - LAYER (CAMADA): Se refere a uma divisão lógica da sua aplicação, sendo normalmente executada em uma única infra e processos distintos. 

Exemplo:

![EXEMPLO](https://media.canva.com/v2/image-resize/format:JPG/height:473/quality:92/uri:s3%3A%2F%2Fmedia-private.canva.com%2FhB8TM%2FMAGLnahB8TM%2F1%2Fp.jpg/watermark:F/width:625?csig=AAAAAAAAAAAAAAAAAAAAAGHSX1nBt2WlSP3P2nPpdR37nBp_ULuX2_uNvlruJZq2&exp=1722912379&osig=AAAAAAAAAAAAAAAAAAAAABuxvVIUcMPzZeMEGHR5jgJ4c2tj0sy5mcB9u4xdOSKS&signer=media-rpc&x-canva-quality=screen)



**Event-driven architeture**

É um estilo arquitetural em que os componentes do sistema se comunicam
através da geração e manipulação de eventos. Um evento é uma mudança
significativa de estado ou uma ocorrência que pode ser capturada e respondida
por outros componentes do sistema.

- Event producers (Publicadores): Geram e emitem eventos.
- Event consumers (Assinantes): Recebem e processam eventos.
- Event channel (Broker de Mensagens): Middleware que gerencia a
distribuição de eventos dos publicadores para os assinantes.
- Event processors: Componentes que processam eventos e podem
gerar novos eventos

artigo: https://nexocode.com/blog/posts/event-driven-architecture-examples-in-logistics-apache-kafka-to-handle-supply-chain-network/


**Microkernel**

Estilo arquitetural que busca manter o núcleo do sistema o mais simples e reduzido possível, delegando a maioria das funcionalidades para módulos ou serviços externos adicionados ao núcleo.



- Características:

    - Núcleo Mínimo: Apenas as funcionalidades essenciais
    - Serviços e Módulos: Funcionalidades adicionais
    - Comunicação: Normalmente feita por meio de chamadas de sistema ou mensagens


- Exemplos:

    - Sistemas Operacionais: Minix, QNX.

    - Frameworks: Eclipse IDE.

*Citação*

*"The microkernel architecture style involves designing a
minimal core system with additional features provided
by separate modules or services. This approach is
considered a style because it defines a high-level
organization of components and their interactions,
rather than a specific implementation pattern."*

*(Software Architecture in Practice, p. 207)*


**Microservices**

É um estilo arquitetural que estrutura uma aplicação como um conjunto de pequenos
serviços independentes, cada um executando um processo único e comunicando-se
por meio de APIs bem definidas. Cada microserviço é desenvolvido, implantado e
escalado de forma independente, permitindo uma maior flexibilidade e agilidade no
desenvolvimento e na manutenção de software.



Características (Prova):

- Desenvolvimento independente;
- Desenvolvimento poliglota;
- Desempenho e escalabilidade;
- Descentralização;

*Trade-offs*

- Complexidade do gerenciamento;
- Latência na comunicação entre microserviços;
- Consistência de dados;
- Custos operacionais e segurança;

Repositório utilizando Microservices: https://github.com/Sandrolaxx/dfmicroservices

Artigo de uso de microservices na Amazon, Netflix e etc: https://blog.dreamfactory.com/microservices-examples

- *Pipes and Filters:* 

Organiza o sistema como uma
série de filtros conectados por pipes (tubos). Cada
filtro é responsável por processar dados, enquanto
os pipes transportam os dados entre os filtros. Este
estilo é ideal para sistemas que processam dados
em etapas sequenciais, como pipelines de
processamento de dados. Exemplo clássico é o
shell do linux:

$ ls | grep b | sort -r | tee arquivo.out | wc -l


- *Representational State Transfer (REST):*

É um estilo arquitetural para sistemas
distribuídos que utiliza o protocolo HTTP e
opera sobre os conceitos de recursos e
representações. 

Em REST, os recursos são identificados
por URLs e manipulados usando
métodos HTTP.

- *Service-Oriented Architecture (SOA):*

Estilo arquitetural que organiza o sistema
como um conjunto de serviços independentes que se comunicam entre si por
meio de interfaces bem definidas. Cada serviço é responsável por uma parte
específica da funcionalidade do sistema e pode ser acessado remotamente
por outros serviços ou aplicações. Possuem o mesmo banco e são uma parte
completa do domínio.

**Clean Arch & Hexagonal**

- *Arquitetura Limpa*

Este estilo de arquitetura enfatiza a separação de preocupações
e a independência dos frameworks, interfaces de usuário, bancos
de dados e outros detalhes externos. Podemos considerar como
um avanço da onion architeture.



*"The Clean Architecture is an architectural style that can be
applied to a wide range of applications. It emphasizes the
separation of concerns, making sure that the business rules are
isolated from frameworks, user interfaces, and external agencies."*
(Clean Architecture: A Craftsman's Guide to Software Structure
and Design, p. 18).


- *Hexagonal-Ports and Adapters*

Foi proposta por Alistair Cockburn, visa criar sistemas de software que sejam altamente desacoplados e testáveis, permitindo que as partes centrais da aplicação permaneçam independentes de suas interfaces de entrada e saída.

![exemplo](https://media.canva.com/v2/image-resize/format:PNG/height:450/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2FqGs6Y%2FMAGLqjqGs6Y%2F1%2Fp.png/watermark:F/width:800?csig=AAAAAAAAAAAAAAAAAAAAAH3TYO2nqF3tau-ZOjHCP1ar0a24HekiRS53MoFmGi-8&exp=1724123059&osig=AAAAAAAAAAAAAAAAAAAAAOnQzLPns9qShDnuV6r4C8ZZUXWIGt4D0zBh6eDcFDYR&signer=media-rpc&x-canva-quality=screen)


**Comparação entre estilos**

- **Clean Arch x Hexagonal x Onion:**

Layered é criticada por focar no banco de dados, causando dependências transitivas, limites
confusos e dificuldades na manutenção e testes. Já a arquitetura hexagonal prioriza a lógica de
negócios, desenvolvendo-a antes da persistência dos dados. Ela se adapta melhor a aplicativos
complexos com componentes adicionais, como APIs REST, evitando dependências excessivas e
duplicação da lógica de negócios.

A Arquitetura Limpa coloca a lógica de negócios no centro, com adaptadores de interface ao redor
conectando a interface do usuário, banco de dados e outros componentes externos. Todas as
dependências do código apontam para o núcleo, seguindo o Princípio de Inversão de Dependência.

Arquitetura Hexagonal mapeia-se quase diretamente para a Arquitetura Limpa.

Arquitetura Limpa pode ser vista como
uma evolução da Arquitetura Onion e
Hexagonal, devido à sua abordagem
mais detalhada e abrangente para a
organização de sistemas de software.

A Arquitetura Limpa refina e expande os
conceitos da Arquitetura Hexagonal,
oferecendo uma estrutura clara e
sistemática para a construção de
aplicações desacopladas, modulares e
testáveis.

**Serverless**

Arquitetura serverless é um modelo de computação em nuvem onde os provedores
de nuvem gerenciam a execução do código, alocando dinamicamente os recursos
necessários. 



Esse modelo permite que os desenvolvedores se concentrem mais na lógica de
negócios e menos na infraestrutura, uma vez que tudo isso é responsabilidade do
provedor de serviços de nuvem.

- Características:

    - Execução sob demanda, escalabilidade automática;
    - Custo-eficiência, gerenciamento simplificado;
- Funções como Serviço (FaaS)

    - AWS Lambda, Google Cloud Functions, e Azure Functions
- Backend como Serviço (BaaS)

    - Firebase Authentication, Firestore e Amazon S3


Podemos encontrar muitos dos conceitos no artigo de Mike Roberts.
https://www.canva.com/design/DAGLliICAKQ/yMvfg3Vkbr4K_0FTKyfyBg/edit#:~:text=Podemos%20encontrar%20muitos%20dos%20conceitos%20no%20artigo%20de%20Mike%20Roberts.

**Qual o estilo
arquitetural correto?**

Depende....

Temos de levar em conta o problema que queremos resolver,
budget do projeto, senioridade do time, isso também vale para
quando buscamos alterar o estilo atual.

### Padrões Arquiteturais

São soluções recorrentes para problemas específicos de design em um contexto
arquitetural. Eles são mais específicos que estilos arquiteturais e fornecem detalhes
sobre a implementação.
    
- Solucionam problemas específicos
- Guias de implementação
- Reutilização de soluções

**MVC - Model, View e Controller**

É um padrão de design de software que separa uma aplicação em três
partes principais:

- Model (Modelo):
    - Representa os dados e a lógica de negócios.
    - Gerencia o comportamento e os dados da aplicação.
- View (Visão):
    - Apresenta os dados ao usuário.
    - Atualiza a interface do usuário quando o modelo muda.
- Controller (Controlador):
    - Recebe a entrada do usuário.
    -   Interage com o modelo e seleciona a visão para apresentar a saída.


Benefícios:

Separação de preocupações: Facilita a manutenção e a escalabilidade.
Reutilização de código: Componentes podem ser reutilizados em
diferentes partes da aplicação.

**Plug-ins**

Núcleo e plug-ins ou extensões que adicionam funcionalidades. O núcleo fornece a
base e a infraestrutura, enquanto os plug-ins fornecem funcionalidades específicas.



Alguns locais citam como estilo arquitetural, porém partilho da visão de que ela
como solução não possui "tamanho" suficiente para ser um estilo completo, se
enquadrando como padrão que pode ser composto em estilos arquiteturais como
o Layered e Componend-based.



Exemplos: Navegadores, IDE’s como Eclipse.

Artigoo: https://medium.com/omarelgabrys-blog/plug-in-architecture-dec207291800

**Three-tier**

A arquitetura de três camadas é um modelo de arquitetura de software que separa
uma aplicação em três camadas físicas distintas: a camada de apresentação
(Presentation Tier), a camada de lógica de negócios (Business Logic Tier), e a
camada de dados (Data Tier). 



Essas camadas são distribuídas em diferentes servidores ou máquinas para
melhorar a escalabilidade, a segurança e a manutenibilidade do sistema.



- Benefícios

    - Escalabilidade
    - Segurança
    - Manutenibilidade
    - Flexibilidade e reutilização









