# Links Notion

- 1 bimestre: https://maze-leaf-ed4.notion.site/Arch-Desing-Primeiro-BI-9af863bbd87b4e8580d7926ca5910a2a

- 2 bimestre: https://maze-leaf-ed4.notion.site/Arch-Desing-Segundo-BI-f61ea951cbbd4ace821efc07e7aeddeb







## Design Patterns attivdades

---

**1. Qual das afirmativas abaixo descreve corretamente as principais características e benefícios dos Design Patterns?**

- **Resposta correta: c)**
  - **São boas práticas utilizadas por desenvolvedores experientes para resolver problemas recorrentes e promovem a clareza, manutenção e escalabilidade do código.**

---

**2. Quanto aos benefícios de manutenção e comunicação, como isso é alcançado na prática?**

- **Resposta correta: d)**
  - **Manutenção é aprimorada, pois evita a necessidade de "reinventar a roda", comunicação aprimorada, pois conceitos complexos são identificados por nomes simples.**

---

**3. Com base no padrão Builder, analise as afirmativas abaixo e escolha a opção correta:**

- **Resposta correta: d)**
  - **Apenas II, III e V estão corretas.**
  - **II. Ele permite que um mesmo processo de construção crie diferentes representações de um objeto.**
  - **III. O Builder separa a construção de um objeto da sua representação, facilitando a criação de objetos complexos com etapas definidas.**
  - **V. Ele é útil quando o processo de criação envolve muitos parâmetros opcionais ou etapas de construção complexas.**

---

**4. Qual padrão de projeto seria o mais adequado para garantir que apenas uma única instância do arquivo de configuração seja criada e compartilhada por todo o sistema?**

- **Resposta correta: e)**
  - **Padrão Singleton, para garantir que apenas uma instância do arquivo de configuração seja criada e compartilhada por todo o sistema.**

---

**5. Selecione a alternativa que possui mais benefícios relacionados a padrões estruturais.**

- **Resposta correta: c)**
  - **Flexibilidade na composição, manutenção/extensão, simplificação de complexidade.**

---

**6. Quanto à categoria de padrões estruturais, analise as seguintes proposições abaixo e escolha a opção correta:**

- **Resposta correta: d)**
  - **I, II e IV estão corretas.**
  - **I. O uso de padrões estruturais melhora a manutenção e a evolução dos sistemas de software.**
  - **II. Padrões estruturais são descritos como soluções para problemas relacionados à composição de classes e objetos para formar estruturas maiores e mais flexíveis.**
  - **IV. Existe um padrão estrutural que pode aprimorar o desempenho da aplicação, diminuindo o consumo de memória RAM.**

---

**7. O padrão Facade:**

- **Resposta correta: b)**
  - **Age como uma fachada que oculta a complexidade de um sistema, fornecendo uma interface mais simples e direta para interação.**

---

**8. Sobre o uso e propósito do padrão Adapter, assinale a alternativa correta:**

- **Resposta correta: d)**
  - **Apenas I e IV estão corretas.**
  - **I. Converte a interface de uma classe em outra interface esperada pelos clientes, facilitando a integração de sistemas legados com novos sistemas.**
  - **IV. Atua como um intermediário que traduz chamadas feitas pelos clientes para uma interface que não seria compatível diretamente.**



## Arquitetura de software atts


**1. Quanto à definição de estilos arquiteturais e padrões arquiteturais:**
Pergunta:
Estilos arquiteturais são padrões utilizados durante o desenvolvimento, enquanto padrões são mais amplos.

Resposta correta:
c) Estilo arquitetural é uma estrutura global de escopo amplo, padrões são soluções específicas e guias de implementação.

---

**2. Em relação às implicações de uma abordagem thin client:**

Pergunta:
Uma empresa está desenvolvendo um sistema e precisa escolher entre uma abordagem thin client ou fat client em sua camada de visualização. Qual das seguintes afirmações é correta?

Resposta correta:
c) Thin client depende fortemente da rede para comunicação constante com o servidor, o que pode ser uma desvantagem em ambientes com conectividade instável.

**3. Sobre a abordagem de Martin Fowler em relação à arquitetura baseada em componentes:**

**Pergunta:**
Quais das seguintes proposições são verdadeiras sobre a abordagem de Martin Fowler?
I. A reutilização de componentes é uma das principais vantagens desse estilo arquitetural, facilitando a manutenção do sistema.
II. Fowler sugere que a alta modularidade dos componentes torna o sistema mais difícil de compreender e manter.
III. A definição clara de interfaces entre componentes é vista por Fowler como essencial para a integração eficiente do sistema.

**Resposta correta:** d) Apenas a I e a III são verdadeiras.

**4. Em relação à arquitetura em camadas:**
Pergunta:
Em uma aplicação corporativa que utiliza o estilo arquitetural em camadas (layered), a camada de apresentação está diretamente ligada à camada de dados para melhorar o desempenho. Avalie se essa prática está conforme os princípios da arquitetura em camadas.

Resposta correta:
e) De acordo com os princípios da arquitetura em camadas, a camada de apresentação deve interagir apenas com a camada de lógica de negócios e não deve ter acesso direto à camada de dados.

**5. Sobre a arquitetura orientada a eventos (EDA):**
Pergunta:
Os eventos são usados para comunicar mudanças de estado entre diferentes componentes do sistema. Qual das seguintes afirmações é verdadeira sobre essa abordagem?

Resposta correta:
d) Eventos são usados para disparar ações reativas em componentes do sistema, permitindo que eles respondam a mudanças de estado de forma assíncrona.

**6. Sobre os benefícios da utilização de microserviços segundo Sam Newman:**
Pergunta:
Quais são os dois principais benefícios da utilização do estilo arquitetural de microserviços?

Resposta correta:
a) Independência dos times e escalabilidade.

**7. Sobre a arquitetura serverless:**
Pergunta:
Quais das seguintes proposições sobre a arquitetura serverless são verdadeiras?
I. A arquitetura serverless elimina completamente a necessidade de servidores físicos, sendo todo o processamento realizado em dispositivos do cliente.
II. Funções serverless são executadas sob demanda, permitindo que recursos sejam alocados apenas quando necessário.
III. A arquitetura serverless permite escalabilidade automática, adaptando-se à carga de trabalho sem intervenção manual.
IV. Em uma arquitetura serverless, os desenvolvedores têm controle direto sobre a infraestrutura subjacente.
V. A arquitetura serverless geralmente resulta em um modelo de pagamento baseado no uso, reduzindo custos em comparação a arquiteturas tradicionais.

Resposta correta:
c) Apenas II, III e V.

**8. Sobre o padrão arquitetural de plugins:**
Pergunta:
Em sistemas que necessitam de extensibilidade, permitindo a adição de novas funcionalidades sem modificar o núcleo do sistema, o padrão arquitetural de plugins é frequentemente adotado. Qual das afirmações abaixo descreve corretamente esse padrão?

Resposta correta:
b) O padrão de plugins permite que funcionalidades sejam adicionadas ao sistema através de módulos externos, que podem ser carregados dinamicamente.









