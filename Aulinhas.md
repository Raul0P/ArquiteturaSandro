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



# Design Patterns - Padrões Criacionais

#### Tópicos

- Visão geral
- Benefícios
- Três categorias
- Padrões criacionais
- Singleton
- Abstract Fatory
- Factory Method
- Prototype
- Builder


#### Visão Geral

**Design Patterns (ou padrões de projeto) são soluções típicas para
problemas recorrentes no desenvolvimento de software**. Eles
representam boas práticas adotadas por desenvolvedores
experientes e foram criados para facilitar a manutenção,
escalabilidade e a clareza do código.

*"Design Patterns are descriptions of communicating
objects and classes that are customized to solve a
general design problem in a particular context."* 
 Gamma et al., 1995, p. 3

Segundo Christoper Alexander “cada padrão descreve um problema do nosso
ambiente e o cerne da sua solução, de tal forma que você possa usar essa solução
mais de um milhão de vezes, sem nunca fazê-lo da mesma maneira” [AIS+77, pág. x].



Arquiteto britânico, o qual foi o primeiro a mapear, o que ele nomeou dê a linguagem
de padrões. Nos termos de Alexander, um padrão é uma regra de três partes, que
expressa uma relação entre um determinado contexto, um problema e uma solução

De posse desses conhecimentos em 1995 Erich Gamma, John Vlissides,
Ralph Johnson e Richard Helm publicaram “Design Patterns: Elements of
Reusable Object-Oriented Software”, onde foram descritos 23 padrões que
resolviam vários problemas de design orientado a objetos e se tornou um
best-seller muito rapidamente. Devido ao seu nome ser muito extenso o livro
foi batizado de GoF (Gang of Four).

##### Quais o benefícios?

- Reutilização de
código

     - Design patterns promovem a
    reutilização de soluções
    testadas, evitando a
    necessidade de "reinventar a
    roda" e economizando tempo
    durante o desenvolvimento.

- Manutenção 

    - O uso de padrões facilita a
    manutenção do código, pois as
    soluções são reconhecíveis e
    compreendidas por
    desenvolvedores familiarizados
    com os padrões.

- Comunicação

    - Ao usar design patterns,
    desenvolvedores podem se
    comunicar de maneira mais
    eficiente, referindo-se a uma
    solução complexa com um
    nome simples e amplamente
    compreendido, como "Factory
    Method" ou "Observer".

- Escalabilidade e
flexibilidade

    - Ajudam a criar sistemas
    facilmente estendidos ou
    modificados à medida que
    novos requisitos surgem

##### Onde não utilizar?

Mesmo sendo ferramentas poderosas, eles não devem ser aplicados de maneira indiscriminada:

- Complexidade desnecessária: Aplicar um pattern em um problema que pode ser resolvido com uma solução mais simples pode adicionar complexidade desnecessária ao código.

- Problemas mal definidos: Não tente forçar um padrão em um problema que não é claramente compreendido. Primeiro, compreenda completamente o problema antes de buscar uma solução padrão.

- Overengineering **microservices**: Evite overengineering, que é a tendência de criar uma solução mais complexa do que o necessário, por aplicar padrões de design onde não são necessários.

#### Três categorias de Patterns

- Criacionais
    - Tratam do processo de
criação de objetos,
promovendo a flexibilidade e
a reutilização de código.

- Estruturais
    - Lidam com a composição
de classes ou objetos,
formando estruturas
maiores de forma
eficiente.

- Comportamentais
    - Lidam com a
comunicação entre os
objetos e com a maneira
como eles interagem e
suas responsabilidades.

#### Singleton

É um padrão de design criacional que garante que uma classe tenha apenas uma única
instância e fornece um ponto global de acesso a essa instância. 



Ele é útil em situações onde é importante que apenas um objeto de uma classe seja criado,
como em gerenciadores de recursos, conexões de banco de dados ou configurações globais
de uma aplicação.

Características:

- Única instância: Apenas uma instância da classe é
criada durante o ciclo de vida da aplicação.
- Controle de acesso: A classe controla como e
quando sua única instância é criada.
- Ponto de acesso global: Fornece uma forma global
de acessar essa instância única.


#### Abstract Factory

Padrão que permite criar famílias de objetos relacionados ou dependentes sem especificar
suas classes concretas. 

Ele define uma interface para criar diferentes tipos de objetos (como botões e checkboxes),
permitindo que o cliente trabalhe com essas famílias de objetos de forma independente de
suas implementações específicas.

Características:

- Criação de famílias de objetos: Permite criar grupos de
objetos relacionados que devem ser usados juntos.
- Independência de implementação: O cliente usa
interfaces abstratas, sem saber quais classes
concretas estão sendo instanciadas.
- Flexibilidade: Facilita a troca entre diferentes famílias
de objetos, como mudar a interface do usuário de
Windows para macOS sem alterar o código cliente.

#### Factory Method

Define um método para criar objetos em uma classe, permitindo que as subclasses decidam
qual classe concreta será instanciada.



Em vez de instanciar objetos diretamente com new, o Factory Method delega essa
responsabilidade para métodos especializados, oferecendo flexibilidade para criar diferentes
tipos de objetos.

Características:

- Delegação da criação: Define um método para criar
objetos, delegando às subclasses a decisão de qual
classe concreta instanciar.
- Desacoplamento: Desacopla a criação de objetos da sua
utilização, facilitando a adição de novas classes sem
modificar o código existente.
- Flexibilidade: Permite que uma classe defina a interface
de criação, enquanto subclasses concretas implementam
a lógica específica para diferentes tipos de produtos

#### Prototype

Permite criar novos objetos copiando instâncias existentes (protótipos), ao invés de
instanciar novos objetos do zero. 

Ele é útil quando a criação direta de um objeto é cara (em termos de tempo ou recursos) ou
quando você deseja evitar subclasses para criar diferentes instâncias.

Características:

- Clonagem de objetos: Cria novos objetos copiando
(clonando) instâncias existentes, sem depender de
classes concretas.
- Flexibilidade: Permite criar objetos complexos com uma
configuração inicial específica, evitando a repetição de
código ou configurações.
- Independência de implementação: Você pode criar
novos objetos sem depender de suas classes concretas,
utilizando cópias de protótipos existentes.

#### Builder

Permite a construção de objetos complexos passo a passo. Ele separa o processo de
construção do objeto da sua representação, permitindo criar diferentes representações do
mesmo objeto.

Características:

- Construção passo a passo: Permite criar objetos
complexos em etapas, adicionando um nível de
controle sobre o processo de construção.
- Separação de preocupações: Separa a lógica de
construção do objeto (Builder) de sua representação
final, permitindo que o mesmo processo construa
diferentes tipos de objetos.
- Flexibilidade: Facilita a criação de objetos com
configurações variadas sem precisar de múltiplos
construtores ou parâmetros opcionais.

# Design Patterns - Padrões Estruturais


Overview:

- Padrões estruturais
- Adapter
- Bridge
- Composite
- Decorator
- Facade
- Flyweight
- Proxy

#### Padrão estrutural

São descritas como soluções para problemas
relacionados à composição de classes e objetos
para formar estruturas maiores e mais flexíveis. 

Esses padrões ajudam a organizar e otimizar o
design de sistemas de software, facilitando como
os componentes interagem e se conectam.

Principais benefícios:

- Flexibilidade na composição de objetos
- Desacoplamento
- Manutenção e extensão
- Simplificação de complexidade

*"Structural patterns deal with object composition, creating relationships between objects to form larger structures. These patterns help ensure that if one part of a system changes, the entire system does not need to change. They simplify the design by decoupling components, making the system more flexible and easier to maintain." - Gamma et al., 1995, p. 25-26*

#### Adapter

Permite que interfaces incompatíveis
trabalhem juntas. Ele converte a interface de
uma classe em outra interface esperada
pelos clientes. 

Assim, o Adapter atua como um
intermediário que traduz as chamadas feitas
pelo cliente para a interface da classe que
não é compatível.

Usado quando é necessário integrar
sistemas legados com novos sistemas ou
quando se deseja adaptar uma API para uma
nova interface.

![exemplo](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2FWDywQ%2FMAGQ38WDywQ%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAAET5BnH2j5StfJ9ShMES_7q2L_zs9hCbr5xPZwCcdMhR&exp=1726543145&osig=AAAAAAAAAAAAAAAAAAAAAKKDBdEcTBUvisu9w9gDUXMv8uWKMInQeDuDaX_qwUw9&signer=media-rpc&x-canva-quality=screen)

#### Bridge

Desacopla uma abstração da sua
implementação, permitindo que ambas
evoluam independentemente. 

É usado quando você quer separar uma
abstração (a ideia principal ou conceito) de
sua implementação concreta (a forma como
o conceito é realizado). Isso é útil para evitar
que mudanças em uma parte da estrutura
(como uma classe) causem impacto na outra
parte.

![exemplo](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2FMLFm0%2FMAGQ36MLFm0%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAABMz9iYK9F9_xQyMBRESGGR0oilCXCjSwM3rA-wM_53Y&exp=1726543349&osig=AAAAAAAAAAAAAAAAAAAAAPUceGeTIh8PPHcgnaPcFke7j8BpAo66vM_8HaNecM8E&signer=media-rpc&x-canva-quality=screen)


#### Composite

Permite que você trate objetos individuais e
composições de objetos de forma uniforme.

Isso é útil quando você tem uma estrutura
hierárquica de objetos, como uma árvore, onde
cada nó pode ser um objeto simples ou um
grupo de objetos.

**Usado quando** precisar representar hierarquias
de objetos, como estruturas de diretórios de
arquivos ou interfaces gráficas complexas.

![exemplo](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2FKVy9U%2FMAGQ33KVy9U%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAAJ4o_AC-oqrnTGzo6ugUt9hIwsoxdryTFhnRnPYXZuN-&exp=1726540620&osig=AAAAAAAAAAAAAAAAAAAAAOvH6JELgz6ZQ8VMRTk5dRrHoB3Zxm9MNoCXyQr0jC86&signer=media-rpc&x-canva-quality=screen)


#### Decorator

Permite adicionar responsabilidades a um objeto dinamicamente, sem alterar o código da classe
original. Ele usa um conjunto de classes de decoração que envolvem o objeto original, adicionando
funcionalidades adicionais. **Utilizado** para adicionar funcionalidades a objetos de maneira flexível e
extensível, como adicionar estilos de janela em um sistema de GUI.

![exeplo](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2Fq-AaM%2FMAGQ4Gq-AaM%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAAD-0v-XwA4Aczv81FRhXHNP6MwG45UdtAAFdkaPdv3XM&exp=1726540027&osig=AAAAAAAAAAAAAAAAAAAAAO91EfnGz2YPlHpE3U8Im-LGmV5IgGLTQm-9oyEJlc28&signer=media-rpc&x-canva-quality=screen)

================================================



### 1º problema

Desejamos criar um sistema que precisa lidar com a estrutura
de um sistema de arquivos, onde há pastas que podem conter
arquivos e outras pastas. 



Cada pasta pode ter um número arbitrário de subpastas e
arquivos, mas tanto os arquivos quanto as pastas podem ser
tratados como "componentes" do sistema de arquivos,
permitindo operações como exibir o conteúdo ou calcular o
tamanho total.

**COMPOSITE**

repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/structural/composite/doc.md

================================================


### 2º Problema

Imagine que você está fazendo um intercambio
para o Reino Unido, chegando lá com seu laptop,
você descobre que o padrão de tomada é
diferente. 

Seu carregador foi projetado para funcionar com
uma tomada de dois pinos (padrão BR), mas lá são
utilizadas tomadas de três pinos (padrão UK). 

Para resolver esse problema sem a necessidade de
modificar o design do carregador ou da tomada,
você pode usar um adaptador de tomada que faz a
conversão entre esses dois padrões.

**ADAPTER**

repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/structural/adapter/doc.md

================================================


#### 3º Problema

Imagine que você está desenvolvendo um sistema que
controla dispositivos eletrônicos como TVs e rádios. 

Você precisa criar diferentes tipos de controles remotos
(por exemplo, controles básicos e avançados) para esses
dispositivos.

Uma abordagem simples seria criar algo específico para
cada tipo de controle e dispositivo (por exemplo,
Controle Remoto TV, Controle Remoto Rádio), mas isso
levaria a uma explosão de implementações conforme
novos dispositivos e novos tipos de controles surgem.

**BRIDGE**

repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/structural/bridge/doc.md

================================================

#### 4º Problema

Imagine que você tem um sistema de notificações,
a notificação básica envia mensagens via e-mail. 

No entanto, você deseja adicionar a capacidade de
enviar mensagens via SMS e registrar as
notificações em um log.

**DECORATOR**

repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/structural/decorator/doc.md

================================================

#### Facade
Fornece uma interface simplificada para um conjunto de interfaces
em um subsistema complexo. Em outras palavras, o Facade **atua
como** uma "fachada" que oculta a complexidade de um sistema,
oferecendo uma maneira mais fácil e direta para os clientes
interagirem com ele.

#### Flyweight
Visa reduzir o uso de memória e
melhorar o desempenho ao
compartilhar objetos semelhantes em
vez de criar novos objetos para cada
instância.

Ele é especialmente útil quando você
precisa lidar com excesso de objetos
que possuem características
semelhantes.

#### Proxy

Fornece um substituto ou intermediário para outro objeto. Ele age como um "representante" do objeto real, controlando o acesso a ele e podendo adicionar funcionalidades extras, como controle de acesso, atraso na criação ou manipulação adicional.

**Usado para** adicionar funcionalidades como controle de acesso, cache, ou outras operações intermediárias.

================================================

#### 5º problema

Imagine que você está desenvolvendo um sistema
de gerenciamento de imagens que precisa exibir
várias imagens de alta resolução. 

Carregar todas as imagens de uma vez pode
consumir muita memória e causar lentidão.

repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/structural/proxy/doc.md

**PROXY**

================================================

#### 6º problema

Imagine que você está criando um Age of Empiers
com inúmeros personagens no campo de batalha. 

Cada personagem tem um tipo (por exemplo, arqueiro,
cavaleiro, monge) e atributos específicos (força,
velocidade, etc.). 

No entanto, muitos personagens compartilham o mesmo tipo, logo, criar uma nova instância de cada tipo para cada personagem resultaria em desperdício de memória. 

repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/structural/flyweight/doc.md

================================================

#### 7º problema

Imagine que estamos desenvolvendo um sistema de gerenciamento de cinema.

O processo de reserva de um ingresso envolve múltiplos passos, como escolher
o filme, selecionar assentos, fazer o pagamento e enviar um e-mail de confirmação. 

Caso o cliente tenha de lidar com cada uma dessas operações, iremos
aumentar a complexidade do código e abrir margem para erros.

**FACADE**

repo: 

