# Estilos Arquiteturais

Estilos Arquiteturais definem a estrutura e organização de sistemas de software, descrevendo como seus componentes interagem e as restrições que guiam o desenvolvimento. A aplicação de estilos arquiteturais traz benefícios como:

- **Reutilização** de soluções testadas para problemas recorrentes.
- **Compreensão e Comunicação** mais claras entre equipes.
- **Flexibilidade e Escalabilidade** ao facilitar a modificação e o crescimento do sistema.
- **Padronização** no desenvolvimento, promovendo consistência.
- **Facilidade de Manutenção** com uma estrutura clara e organizada.

## Principais Estilos Arquiteturais

### Client-Server
- Distribui responsabilidades entre servidores, que fornecem serviços, e clientes, que os consomem.
- Em **thin client**, o servidor faz a maior parte do processamento, enquanto em **fat client** o cliente executa mais lógica de aplicação.
- Comum em aplicações web e sistemas de banco de dados, esse estilo é frequentemente combinado com outros, como **Component-based** e **Layered**.

### Component-based
- Focado na reutilização de componentes, essa arquitetura permite que sistemas sejam desenvolvidos e implantados de forma modular.
- Componentes podem ser atualizados sem afetar o restante do sistema, facilitando a manutenção.
- Um exemplo é o uso de **microserviços**, que seguem princípios semelhantes ao component-based, mas são mais independentes.

### Layered
- Organiza o sistema em camadas com responsabilidades específicas (apresentação, aplicação, domínio, infraestrutura), facilitando a separação de preocupações.
- A **arquitetura N-tiers** é uma variante física, onde camadas são distribuídas entre diferentes servidores, aumentando a escalabilidade e distribuindo a carga de trabalho.

### Event-driven Architecture (EDA)
- Componentes do sistema se comunicam por meio de eventos.
- Existem **Event producers** (publicadores) que geram eventos e **Event consumers** (assinantes) que os processam.
- Um **event channel** gerencia a distribuição, enquanto **event processors** tratam os eventos e podem gerar novos.

### Microkernel
- Foca em um núcleo mínimo e modularidade, onde funcionalidades adicionais são acopladas como serviços externos.
- Muito usado em sistemas operacionais como **Minix** e frameworks como **Eclipse IDE**.

### Microservices
- Esse estilo divide a aplicação em pequenos serviços independentes, com comunicação via APIs.
- Cada microserviço é implantado e escalado de forma separada, oferecendo flexibilidade e agilidade.
- Entre as características estão a **descentralização**, **desenvolvimento poliglota** e **escala independente**.

### Pipes and Filters
- Sistemas são organizados como filtros que processam dados e pipes que os transportam entre filtros.
- Muito usado em pipelines de dados, como no shell do Linux.

### Representational State Transfer (REST)
- Usa HTTP para operar sobre recursos e representações.
- Recursos são identificados por URLs e manipulados via métodos HTTP.

### Service-Oriented Architecture (SOA)
- Organiza o sistema como um conjunto de serviços independentes que se comunicam por interfaces definidas, com foco em compartilhamento de funcionalidade.

### Clean Architecture e Hexagonal
- A **Arquitetura Limpa** enfatiza a independência de frameworks, bancos de dados e interfaces, isolando regras de negócio no centro do sistema.
- Ela é considerada uma evolução da **Arquitetura Hexagonal**, que também prioriza a lógica de negócios, desacoplando as interfaces de entrada e saída.
- Ambos os estilos facilitam testes e evolução.

### Serverless
- Os provedores de nuvem gerenciam a execução do código, escalando automaticamente os recursos necessários.
- Exemplos incluem **AWS Lambda** e **Firebase**.

## Padrões Arquiteturais
Mais específicos que os estilos, **padrões arquiteturais** fornecem soluções recorrentes para problemas de design em contextos específicos.

### Model-View-Controller (MVC)
- Separa a aplicação em três partes: **Model** (dados e lógica), **View** (interface) e **Controller** (gerenciamento da entrada do usuário).
- Essa separação facilita a reutilização de código e a manutenção.

### Plug-ins
- Adiciona funcionalidades extras ao núcleo de um sistema.
- Comumente visto em navegadores e IDEs como **Eclipse**, esse padrão pode se combinar com estilos como **Layered** e **Component-based**.

### Three-tier
- A arquitetura de três camadas divide a aplicação em: **Apresentação**, **Lógica de Negócios** e **Dados**, distribuídas fisicamente em servidores.
- Oferece escalabilidade e flexibilidade.

### Publisher-Subscriber
- Desacopla publicadores e assinantes, permitindo que componentes evoluam independentemente.
- É um padrão amplamente usado em sistemas distribuídos e orientados a eventos.

## Considerações Finais
A escolha do estilo ou padrão arquitetural ideal depende de fatores como o tipo de aplicação, orçamento e senioridade da equipe. É importante alinhar a arquitetura com os requisitos e limitações do projeto para garantir sucesso na implementação e manutenção.




# Padrões de Projeto - Padrões Criacionais

## Design Patterns

### Visão Geral

Design Patterns (ou padrões de projeto) são soluções típicas para problemas recorrentes no desenvolvimento de software. Eles representam boas práticas adotadas por desenvolvedores experientes e foram criados para facilitar a manutenção, escalabilidade e a clareza do código.

> "Design Patterns are descriptions of communicating objects and classes that are customized to solve a general design problem in a particular context."  
> — Gamma et al., 1995, p. 18-19

De acordo com Christoper Alexander, “cada padrão descreve um problema do nosso ambiente e o cerne da sua solução, de tal forma que você possa usar essa solução mais de um milhão de vezes, sem nunca fazê-lo da mesma maneira” [AIS+77, pág. x].

Em 1995, Erich Gamma, John Vlissides, Ralph Johnson e Richard Helm publicaram o livro *Design Patterns: Elements of Reusable Object-Oriented Software*, onde descreveram 23 padrões que resolvem problemas de design orientado a objetos. O livro ficou conhecido como *GoF* (Gang of Four).

---

### Quais são os benefícios?

- **Reutilização de código**: Promovem a reutilização de soluções testadas, evitando a "reinvenção da roda".
- **Manutenção**: Facilita a manutenção, pois as soluções são reconhecíveis e compreendidas por desenvolvedores familiarizados com os padrões.
- **Comunicação**: Melhora a comunicação entre desenvolvedores, referindo-se a soluções complexas com nomes simples e amplamente reconhecidos.
- **Escalabilidade e Flexibilidade**: Ajuda a criar sistemas extensíveis ou modificáveis conforme surgem novos requisitos.

### Onde não utilizar?

- **Complexidade desnecessária**: Não aplicar em problemas simples, evitando adicionar complexidade ao código.
- **Problemas mal definidos**: Não aplicar sem entender completamente o problema.
- **Overengineering**: Evitar criar soluções mais complexas do que o necessário.

---

## Três Categorias de Patterns

- **Criacionais**: Tratam da criação de objetos, promovendo flexibilidade e reutilização de código.
- **Estruturais**: Lidam com a composição de classes ou objetos, formando estruturas maiores de forma eficiente.
- **Comportamentais**: Lidam com a comunicação entre os objetos e suas responsabilidades.

---

## Padrões Criacionais

### Singleton

Garante que uma classe tenha apenas uma única instância e fornece um ponto global de acesso a essa instância. É útil em situações onde é importante que apenas um objeto seja criado, como em gerenciadores de recursos ou conexões de banco de dados.

**Características:**
- Única instância.
- Controle de acesso.
- Ponto de acesso global.

---

### Abstract Factory

Permite criar famílias de objetos relacionados sem especificar suas classes concretas. Define uma interface para criar diferentes tipos de objetos, permitindo que o cliente trabalhe de forma independente das implementações.

**Características:**
- Criação de famílias de objetos.
- Independência de implementação.
- Flexibilidade.

---

### Factory Method

Define um método para criar objetos em uma classe, permitindo que as subclasses decidam qual classe concreta será instanciada. Oferece flexibilidade para criar diferentes tipos de objetos sem acoplamento direto.

**Características:**
- Delegação da criação.
- Desacoplamento.
- Flexibilidade.

---

### Prototype

Permite criar novos objetos copiando instâncias existentes, útil quando a criação direta de um objeto é cara ou para evitar subclasses.

**Características:**
- Clonagem de objetos.
- Flexibilidade.
- Independência de implementação.

---

### Builder

Permite a construção de objetos complexos passo a passo, separando o processo de construção da sua representação.

**Características:**
- Construção passo a passo.
- Separação de preocupações.
- Flexibilidade.




# Padrões Estruturais - Design Patterns

## Definição
Os padrões estruturais são soluções para problemas relacionados à **composição de classes e objetos** em estruturas maiores e mais flexíveis. Eles ajudam a organizar o design do software, otimizando a interação entre os componentes.

### Benefícios principais:
- **Flexibilidade:** Facilita a composição de objetos.
- **Desacoplamento:** Reduz dependências diretas entre componentes.
- **Manutenção:** Torna o código mais fácil de manter e estender.
- **Simplicidade:** Simplifica sistemas complexos.

---

## Padrões Estruturais mais comuns:

### 1. Adapter
- **Propósito:** Converte a interface de uma classe em outra interface esperada pelo cliente, permitindo que interfaces incompatíveis funcionem juntas.
- **Exemplo:** Usar um adaptador para conectar um carregador com padrão de tomada diferente em outro país.

### 2. Bridge
- **Propósito:** Desacopla uma abstração de sua implementação, permitindo que ambas evoluam independentemente.
- **Exemplo:** Controlar dispositivos como TVs e rádios sem precisar criar novas classes para cada combinação de controle e dispositivo.

### 3. Composite
- **Propósito:** Permite tratar objetos individuais e composições de objetos de forma uniforme.
- **Exemplo:** Um sistema de arquivos onde pastas e arquivos são tratados como componentes do sistema, seja para exibir o conteúdo ou calcular o tamanho.

### 4. Decorator
- **Propósito:** Adiciona funcionalidades a um objeto dinamicamente, sem modificar sua classe original.
- **Exemplo:** Um sistema de notificação onde, além de e-mail, você deseja enviar notificações por SMS e registrar logs.

### 5. Facade
- **Propósito:** Fornece uma interface simplificada para um sistema complexo.
- **Exemplo:** Simplificar o processo de reserva de cinema, onde várias etapas (escolha de filme, assento, pagamento, etc.) são ocultadas por uma interface mais direta.

### 6. Flyweight
- **Propósito:** Reduz o uso de memória compartilhando objetos semelhantes em vez de criar novas instâncias para cada objeto.
- **Exemplo:** Um jogo com muitos personagens semelhantes, como arqueiros, onde os atributos comuns são compartilhados para economizar memória.

### 7. Proxy
- **Propósito:** Atua como um substituto ou intermediário de outro objeto, controlando o acesso a ele.
- **Exemplo:** Um sistema de gerenciamento de imagens que utiliza proxy para carregar imagens de alta resolução apenas quando necessário, economizando recursos.

---

## Problemas Exemplificados:
1. **Adapter:** Usar um adaptador para conectar um carregador brasileiro em uma tomada no Reino Unido.
2. **Bridge:** Criar controles remotos diferentes para TVs e rádios sem precisar criar uma classe específica para cada dispositivo.
3. **Composite:** Representar uma estrutura de pastas e arquivos de forma hierárquica e uniforme.
4. **Decorator:** Adicionar novas funcionalidades de notificação a um sistema sem modificar a classe original.
5. **Proxy:** Controlar a exibição de imagens de alta resolução em um sistema de gerenciamento de mídia.
6. **Flyweight:** Economizar memória em um jogo como Age of Empires, compartilhando atributos comuns entre personagens.
7. **Facade:** Simplificar o processo de reserva de ingressos de cinema, ocultando a complexidade do sistema.
"""