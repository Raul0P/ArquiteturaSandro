## PADRÕES DE PROJETO - Padrões Comportamentais

#### Definição

Os padrões comportamentais são focados em definir
como os objetos interagem e se comunicam entre si
dentro de um sistema.

Eles abordam a atribuição de responsabilidades e a
maneira como as classes colaboram, permitindo que o
comportamento do sistema seja flexível e dinâmico
sem a necessidade de modificações profundas no
código.

Segundo o livro "Design Patterns: Elements of Reusable Object-
Oriented Software" (GoF), os padrões comportamentais "*se
preocupam com algoritmos e a atribuição de responsabilidades
entre objetos... não descrevem apenas padrões de objetos ou
classes, mas também o padrão de comunicação entre eles.*"
(GoF, p. 211).

Esses padrões auxiliam a separar a lógica de controle do
comportamento real dos objetos, facilitando a extensão e
manutenção do código.

---

#### CHAIN OF RESPONSIBILITY

Permite que um pedido passe por
uma cadeia de objetos potenciais,
onde cada objeto tem a chance de
tratar o pedido ou passá-lo adiante. 

Isso promove um desacoplamento
entre o remetente e os receptores,
permitindo que vários objetos
possam processar o pedido de forma
ordenada e flexível.

![exemplo](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2F-ZHa0%2FMAGSQG-ZHa0%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAALX03s2Ag-lejmD1ryHMIpXvSp36bMrVGqhyWKc8cUWl&exp=1727753304&osig=AAAAAAAAAAAAAAAAAAAAAIbYMg7UzCWImiVsYElWEPwr2jULTIe1umtyFG6gGpxl&signer=media-rpc&x-canva-quality=screen
)

---

#### COMMAND

Transforma uma solicitação em um objeto
autônomo, que encapsula toda a informação
necessária para executar uma ação. Isso inclui
o próprio pedido, o receptor que o processará
e, eventualmente, os parâmetros necessários.

O padrão permite que comandos sejam
armazenados, enfileirados, desfeitos ou
refeitos sem a necessidade de conhecer os
detalhes sobre quem ou como a solicitação
será processada.

Esse padrão promove o desacoplamento entre
o objeto que faz a solicitação e os objetos
que realizam a ação.

![EXEMPLO](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2FuCrVk%2FMAGSQBuCrVk%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAAJubhlLQdmH6UFnP9CEIZLkmbvJuzqp-DoX829g-piPa&exp=1727751181&osig=AAAAAAAAAAAAAAAAAAAAAKYWuBZwCfBQGH-sdyQVYPY7BEe5kf1g3SMQBQ0OX1J6&signer=media-rpc&x-canva-quality=screen)

---

#### INTERPRETER

Define uma forma de interpretar ou avaliar a
gramática de uma linguagem, representando-a
por meio de uma estrutura de classes.

Ele é útil quando você precisa interpretar ou
analisar sentenças ou expressões escritas em
uma linguagem particular, e cada símbolo ou
expressão tem uma regra gramatical
associada.

Este padrão é normalmente usado em
cenários onde uma linguagem específica, um
script ou expressões complexas precisam ser
processados repetidamente.

![EXEMPLO](https://media.canva.com/v2/image-resize/format:PNG/height:500/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2FFGyNk%2FMAGSQMFGyNk%2F1%2Fp.png/watermark:F/width:500?csig=AAAAAAAAAAAAAAAAAAAAAE4gcdrTigYKY4ref13K2HZhUVs2TJCg8orkt7soU1TR&exp=1727752502&osig=AAAAAAAAAAAAAAAAAAAAAHaUCcAfjCge5y2bc4UQEqodRuGRU1o6GOex3cgteen1&signer=media-rpc&x-canva-quality=screen)

---


### PROBLEMAS (interpreter, command, chain of responsibility)

#### 1º problema (Command)

Desenvolver um sistema de automação
residencial que permite aos usuários controlar
dispositivos, como lâmpadas, cortinas e
sistemas de som, por meio de comandos
emitidos por um controle remoto. 

O sistema precisa ser flexível o suficiente
para permitir que novos dispositivos sejam
adicionados no futuro, sem que o controle
remoto precise ser alterado. Além disso, os
usuários querem ter a capacidade de desfazer
uma ação, como desligar a lâmpada após tê-la
ligado acidentalmente.

link repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/behavioral/command/doc.md

---

#### 2º problema (Chain of responsibility)

Imagine que estamos desenvolvendo um sistema de
suporte técnico para uma empresa que oferece vários níveis
de atendimento.

Os clientes podem ter problemas de diferentes níveis de
complexidade: simples, intermediários e complexos.

Dependendo da complexidade do problema, ele pode ser
resolvido por um atendente, um técnico de nível 1, 2 ou 3.

link repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/behavioral/chainofresponsibility/doc.md

---

#### 3º problema (Interpreter)

Estamos desenvolvendo uma planilha, ela deve
suportar uma gama de expressões matemáticas pré-
definidas, como (somar, subtrair, multiplicar e dividir). 

Os usuários podem inserir expressões matemáticas
no formato de texto, como SOMA(3, 5), e a
calculadora deve interpretar e avaliar a expressão
corretamente.

link repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/behavioral/interpreter/doc.md

---

#### ITERATOR

Permite percorrer uma coleção de objetos (como
listas, arrays ou árvores) de forma sequencial, sem
expor sua estrutura interna. O padrão separa a lógica
de iteração da coleção, fornecendo uma interface
comum para acessar os elementos um por um,
independentemente da implementação da coleção.

O objetivo do Iterator é garantir que diferentes tipos
de coleções possam ser percorridos de forma
uniforme, oferecendo métodos como next(),
hasNext(), e currentItem() para controlar o fluxo de
acesso aos elementos.

![EXEMPLO](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2F6vGIQ%2FMAGSRa6vGIQ%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAAMuVh6HTPWaYJxymdvN2CSGZDHW28QBSEDT15yNJUsXM&exp=1727752864&osig=AAAAAAAAAAAAAAAAAAAAAGQIUMKZc2G_5OB-1v_Wuo4Bbo66Y6a9ui83OC8abv0G&signer=media-rpc&x-canva-quality=screen)

---

#### MEDIATOR

Centraliza a comunicação entre objetos,
evitando que eles se comuniquem
diretamente uns com os outros. 

Isso promove o desacoplamento entre os
objetos, pois, ao invés de se comunicarem
diretamente, eles passam a interagir
mediante um intermediário, o Mediator. 

Esse padrão é útil quando há inúmeras
interações complexas entre os objetos, o
que poderia tornar o sistema difícil de
manter e modificar.

![EXEMPLO](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2FzHB3s%2FMAGSRfzHB3s%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAAJjMrL1vfoEUPXcvN2ihn-Cov9uskzo-CWX464tXxzhr&exp=1727752501&osig=AAAAAAAAAAAAAAAAAAAAAGbcjVhyAYAIyOkTLFPzc0knvtsxoVNREMWEjfzmJRan&signer=media-rpc&x-canva-quality=screen)

---

#### MEMENTO

Permite capturar e armazenar o estado interno de um objeto em um determinado momento, sem expor os detalhes de sua implementação.

Posteriormente, esse estado pode ser restaurado, permitindo que o objeto volte a uma configuração anterior. 

A principal vantagem do Memento é que ele mantém a integridade do encapsulamento do objeto original, pois o estado armazenado não é exposto diretamente para o cliente ou outros objetos.

![ex](https://media.canva.com/v2/image-resize/format:PNG/height:400/quality:100/uri:s3%3A%2F%2Fmedia-private.canva.com%2FoDWl8%2FMAGSRYoDWl8%2F1%2Fp.png/watermark:F/width:640?csig=AAAAAAAAAAAAAAAAAAAAAI9meD3wf6FwzzQ8ObDhGFEnUGzLK74xcMNwIubEGOOv&exp=1727752448&osig=AAAAAAAAAAAAAAAAAAAAAD_ScICfHgTKtegSx8CP9_7fzYaEgkXUWge8WIrRKL4P&signer=media-rpc&x-canva-quality=screen)

---

### PROBLEMAS (Memento, Mediator, Iterator)

#### 1º problema (Mediator)

Imagine que você está desenvolvendo um sistema de chat
para o discord2. Nesse sistema, os usuários podem enviar
mensagens uns para os outros em grupos de chat. Cada
usuário pode estar em vários grupos, e a comunicação
entre os usuários deve ser gerenciada de forma eficiente. 

Se cada usuário fosse responsável por enviar mensagens
diretamente para todos os outros usuários do grupo, o
código rapidamente se tornaria caótico e difícil de manter,
pois cada usuário precisaria conhecer todos os outros.

link repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/behavioral/mediator/doc.md

---

#### 2º problema (Memento)

Imagine que você está desenvolvendo um editor de texto com
uma funcionalidade de "desfazer" (undo) e "refazer" (redo). No
editor, os usuários podem fazer alterações no documento e, caso
algo saia errado, eles podem desfazer essas alterações e retornar
a um estado anterior do documento. 

Se o editor armazenar diretamente cada estado em variáveis ou
gerenciar essas mudanças dentro do objeto principal do
documento, o código pode ficar muito acoplado e difícil de
manter, especialmente conforme a complexidade do
documento aumenta.

link repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/behavioral/memento/doc.md

---

#### 3º problema (Iterator)

Imagine que você está desenvolvendo uma plataforma de
streaming de vídeo. Nessa plataforma, os usuários podem
criar listas de reprodução (playlists) com filmes e séries. Cada
playlist pode conter diferentes tipos de conteúdo, como
episódios de séries ou filmes completos.

O problema surge quando você precisa implementar a
navegação por essas listas de reprodução. É necessário
permitir que os usuários percorram suas playlists de maneira
eficiente e consistente, independentemente do tipo de
conteúdo (filmes ou séries).

link repo: https://github.com/Sandrolaxx/design-pattern-sample/blob/master/behavioral/iterator/doc.md









