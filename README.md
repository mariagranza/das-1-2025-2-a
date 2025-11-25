Artigo: Pensamento Arquitetônico - Fundamentos da Arquitetura de Software

1- Resuma a diferença entre: Arquitetura e Design

Arquitetura de Software: foca nas decisões de alto nível do sistema que são difíceis de mudar, define estruturas principais, componentes, comunicação entre eles e princípios que ajudarão a guiar o desenvolvimento.

Design de Software: está mais próximo da implementação de baixo nível, detalhando como cada componente ou módulo será construído. Define classes, métodos, interfaces, padrões de design e outros aspectos internos que podem ser alterados com menor impacto.

Arquitetura = visão macro, estratégica, de longo prazo. Design = visão micro, tática, de curto prazo.

2- Como é a formação do conhecimento de um arquiteto modelo T?

Ele combina amplitude e profundidade. Barra horizontal do T: representa a amplitude de conhecimentos onde o arquiteto precisa entender um pouco de várias áreas como bancos de dados, redes, cloud, segurança, metodologias ágeis, conseguindo dialogar com diferentes especialistas.

Barra vertical do T:representa a profundidade em uma área específica onde o arquiteto deve ter especialização sólida em algum domínio técnico como por exemplo, integração de sistemas, microsserviços, IA...

1- O que é abstração?

Abstração significa não considerar ou ignorar algo propositalmente, o que é chamado de “abstrato” é tudo aquilo que não se refere ao mundo físico de forma direta.

2- O que é ocultamento de informações?

É uma técnica da que envolve a incorporação de mensagens secretas em informações públicas para ocultar sua existência, fornecendo uma camada extra de segurança ao tornar as mensagens secretas invisíveis para partes não autorizadas.

3- O que é um código com coesão?

Coesão se refere ao grau em que os elementos dentro de um módulo pertencem um ao outro, é uma medida da força do relacionamento entre os métodos e dados de uma classe e algum propósito ou conceito unificador servido por essa classe.

4- O que é acoplamento?

É o grau de interdependência entre dois componentes de um software, quando há baixo acoplamento o componente consegue operar de forma mais independente do outro, já o alto acoplamento implica em uma conexão forte entre os dois, o que pode torná-los até indistinguíveis.

Robert Martin - referência código limpo

SOLID: Usar a orientação a objetos do jeito mais correto possível.

S - Single responsability principle (Princípio da responsabilidade única)

Relação direta com a coesão Separar as coisas MVC (dados, html, controla a tela) Responsabilidade única na hora de construir uma interface gráfica

É um conceito na programação orientada a objetos que estabelece que uma classe deve ter apenas uma única razão para mudar, que deve ser responsável por uma única funcionalidade ou tarefa específica, ou seja, uma classe não deve ser sobrecarregada com múltiplas responsabilidades que não estão relacionadas entre si.

O - Open-Closed Principle (Princípio Aberto-Fechado)

As entidades de software (classes, módulos, funções, etc.) devem ser abertas para extensão, mas fechadas para modificação. O comportamento de um módulo pode ser estendido sem alterar seu código-fonte.

L - Liskov Substitution Principle (Princípio da substituição de Liskov)

Os objetos de uma classe base devem poder ser substituídos por objetos de suas subclasses sem que o comportamento do programa seja alterado. Se uma classe A é subtipo de uma classe B, então objetos de tipo A devem poder ser usados em qualquer lugar onde objetos de tipo B são esperados, sem causar erros ou comportamentos inesperados.

I - Interface Segregation Principle (Princípio da Segregação da Interface)

Interface que seja bem escrita e que defina como vai ser a comunicação entre essas duas classes Cada interface tem sua responsabilidade

D - Dependency Inversion Principle (Princípio da inversão da dependência)

Uma classe deve depender diretamente de uma abstração e não de uma impleentação concreta É um princípio que afirma que módulos de alto nível não devem depender de módulos de baixo nível, e que ambos devem depender de abstrações.

Conceitos Fundamentais
-Abstração

Processo de transformar problemas do mundo real em soluções de software, destacando apenas os aspectos essenciais.

Permite focar no o que um objeto faz e não como ele faz.

Facilita a modelagem de sistemas complexos e melhora o entendimento do problema.

-Ocultamento de Informação (Encapsulamento)

Esconde os detalhes internos da implementação, expondo apenas o necessário para uso externo.

Garante integridade dos dados, organiza o código e evita interferências externas.

Exemplo: atributos privados acessados apenas por getters e setters.

-Débito Técnico

Resultado de escolhas rápidas ou soluções fáceis que podem gerar problemas no futuro.

Consequências: aumento de erros, dificuldade de manutenção, necessidade de reescrever código.

Pode ocorrer por prazos curtos, falta de conhecimento ou má implementação.

-Coesão

Cada classe ou módulo deve ter uma única responsabilidade.

Código coeso é mais fácil de entender, testar e manter.

Exemplo: uma classe Cliente deve lidar apenas com dados e comportamentos relacionados ao cliente.

-Acoplamento

Mede a dependência entre classes ou módulos.

Baixo acoplamento: comunicação via interfaces; alterações em uma classe não afetam a outra.

Alto acoplamento: dependência direta de código interno ou de variáveis globais; mudanças podem quebrar o sistema.

UML e Padrões de Arquitetura
-UML (Unified Modeling Language)

Linguagem de modelagem que representa visualmente classes, objetos e suas relações.

Herança: seta vazada → uma classe herda atributos/métodos de outra.

Associação: seta cheia → relação entre classes.

Implementação: seta pontilhada e vazada → classe implementa interface.

-MVC (Model-View-Controller)

Model: gerencia dados e lógica de negócio.

View: apresenta informações ao usuário.

Controller: controla fluxo e regras do sistema.

Princípios de Código SOLID
S – Single Responsibility Principle: uma classe deve ter apenas um motivo para mudar.

O – Open/Closed Principle: classes devem estar abertas para extensão, mas fechadas para modificação.

L – Liskov Substitution Principle: subclasses devem substituir superclasses sem alterar o comportamento esperado.

I – Interface Segregation Principle: interfaces devem ser pequenas, coesas e específicas; evite obrigar classes a implementar métodos desnecessários.

D – Dependency Inversion Principle: classes de alto nível devem depender de abstrações e não de implementações concretas.

-Composição x Herança

Prefira composição sempre que possível; herança só quando subclasses não puderem exercer o mesmo papel que a classe base.

Exemplo: Cachorro e Gato herdam de Animal, mas um não pode ser o outro.

-Princípio de Demeter (Lei do Menor Conhecimento)

Uma classe/método deve conhecer apenas o necessário para executar sua função.

Acesso permitido apenas a:

métodos da própria classe

objetos passados como parâmetro

objetos criados dentro do método

atributos da própria classe

Evita cadeias longas de chamadas (ex.: pedido.getCliente().getEndereco().getCidade() → ruim; pedido.getCidadeCliente() → bom).

Arquitetura de Software Características Arquiteturais
Requisitos não funcionais que definem qualidade do sistema.

Exemplos: desempenho, escalabilidade, segurança, confiabilidade, manutenibilidade.

Nenhum sistema consegue atender todos os requisitos não funcionais simultaneamente.

-Decisões Arquiteturais

Definem como o sistema será construído, escolhendo tecnologias, padrões e limites.

Exemplo: camada de apresentação não acessa diretamente o banco de dados, microsserviços vs. monólito.

-Princípios de Design

Orientações para criação do sistema, mas não regras obrigatórias.

Exemplo: comunicação assíncrona entre microsserviços para melhorar escalabilidade.

-Trade-offs

Toda decisão arquitetural envolve vantagens e desvantagens.

É necessário equilibrar atributos conflitantes, como desempenho, segurança e manutenibilidade.

Estilos de Comunicação Publish/Subscribe (Tópicos)
Comunicação assíncrona, um-para-muitos.

Publisher envia evento para canal; canal distribui para múltiplos subscribers.

Benefício: desacoplamento e facilidade de escalar o sistema.

Protocolos: MQTT, AMQP, WebSocket.

Exemplos: RabbitMQ, HiveMQ, SNS.

Fan-out: uma mensagem enviada é recebida por vários consumidores simultaneamente.

-Fila (Queue – FIFO)

Comunicação um-para-um.

Mensagens são processadas na ordem de chegada (First In, First Out).

Conceitos: ENQUEUE (adicionar), DEQUEUE (retirar), Sender/Receiver, Buffer, Pooling.

Implementações: RabbitMQ, AWS SQS, Azure ServiceBus.

Melhor para confiabilidade e processamento garantido.

Papel do Arquiteto
Tomar decisões: define tecnologias, padrões e limites do sistema.

Analisar continuamente: revisar e melhorar a arquitetura ao longo do tempo.

Manter-se atualizado: acompanhar tendências e melhores práticas.

Assegurar conformidade: garantir que padrões e decisões sejam respeitados.

Experiência diversificada: conhecer diversas tecnologias e ambientes.

Conhecimento do domínio: entender regras de negócio e apoiar decisões técnicas.

Habilidades interpessoais: liderança, comunicação, motivação e negociação.

Gestão política: lidar com hierarquia, negociar prazos e influenciar decisões.

-Arquiteto Modelo T

Horizontal: conhecimento amplo em várias tecnologias e ambientes.

Vertical: especialização profunda em uma área específica.

Práticas Modernas DevOps
Integra desenvolvimento e operações para entregar valor contínuo ao cliente.

Ciclo: Planejamento → Criação → Integração Contínua → Implantação → Monitoramento → Feedback.

Cultura DevOps: colaboração entre todas as equipes, não apenas desenvolvedores ou infraestrutura.

-Twelve-Factor App

Boas práticas para aplicações SaaS modernas: portabilidade, automação, escalabilidade, implantação simples, independente da linguagem ou serviços utilizados.

----------------------------------------------------------------------------------------

2°BIMESTRE

https://learn.microsoft.com/pt-br/azure/architecture/patterns/circuit-breaker?wt.mc_id=AZ-MVP-5003638

Circuit breaker: O Circuit Breaker é um padrão criado para evitar que uma aplicação continue enviando requisições para serviços que estão falhando ou demorando demais para responder — situação bastante comum em sistemas distribuídos. Sua função é impedir que erros transitórios se tornem problemas maiores, protegendo todo o ecossistema de chamadas remotas repetidas e inúteis.

Esse mecanismo funciona alternando entre três estados:

• Fechado (Closed)
As requisições são processadas normalmente. Caso o volume de falhas ultrapasse um limite definido, o mecanismo “abre” e interrompe as chamadas.

• Aberto (Open)
As requisições deixam de ser encaminhadas para o serviço que está apresentando problemas. Após um período de espera determinado, o estado muda para o modo de teste.

• Meio Aberto (Half-Open)
Nesse estágio intermediário, apenas algumas requisições são permitidas para verificar se o serviço já se recuperou. Se der tudo certo, o circuito “fecha” novamente; caso contrário, volta a permanecer “aberto”.

Características Arquiteturais

As características arquiteturais representam qualidades essenciais de um software. Elas orientam decisões importantes de projeto e influenciam diretamente na eficiência e no comportamento do sistema. Para serem consideradas relevantes, precisam:

Tratar de aspectos fora do domínio de negócio;

Impactar a estrutura da solução;

Ser fundamentais para o sucesso da aplicação.

Essas características podem ser agrupadas em três categorias:

1. Características Operacionais

Relacionadas a como o sistema se comporta em execução.

Termo	Descrição
Disponibilidade	Período em que o sistema deve permanecer funcional.
Continuidade	Capacidade de recuperação após eventos críticos.
Desempenho	Rapidez e capacidade de resposta.
Recuperabilidade	Tempo necessário para restaurar o sistema depois de falhas.
Confiabilidade / Segurança	Resistência a falhas e importância operacional.
Robustez	Resistência a erros internos e externos.
Escalabilidade	Habilidade de crescer conforme o uso aumenta.
2. Características Estruturais

Relacionadas ao design interno e qualidade técnica do software.

Termo	Descrição
Configuração	Facilidade de ajustar parâmetros conforme necessidade.
Extensão	Facilidade para incluir funcionalidades novas.
Instalabilidade	Simplicidade de instalação em diferentes ambientes.
Reutilização	Uso de módulos e componentes em soluções distintas.
Localização	Suporte a idiomas e formatos regionais.
Manutenção	Agilidade para modificar ou corrigir o sistema.
Portabilidade	Capacidade de rodar em diferentes plataformas.
Suporte	Ferramentas e mecanismos para diagnóstico de problemas.
Atualização	Facilidade de substituir versões antigas por novas.
3. Características Transversais

Atravessam várias áreas do sistema e não se encaixam perfeitamente em categorias únicas.

Termo	Descrição
Acessibilidade	Uso por pessoas com necessidades diversas.
Armazenamento	Regras para retenção ou descarte de dados.
Autenticação	Garantia da identidade do usuário.
Autorização	Controle sobre o que cada usuário pode acessar.
Legalidade	Conformidade com leis e normas aplicáveis.
Privacidade	Proteção das informações contra acessos indevidos.
Segurança	Criptografia e proteção contra ataques.
Suporte	Recursos operacionais para identificar e registrar falhas.
Usabilidade / Viabilidade	Facilidade de aprendizado e uso da aplicação.
A Arquitetura “menos pior”

Projetar um software envolve equilibrar qualidades conflitantes (ex.: segurança e desempenho). Não existe arquitetura perfeita — existe a que atende melhor ao contexto e aos objetivos do negócio. O papel do arquiteto é encontrar o ponto ideal entre compromissos, e não maximizar tudo ao mesmo tempo.

CQRS (Command Query Responsibility Segregation)

O CQRS defende a separação entre modelos de escrita e leitura para melhorar desempenho, escalabilidade e clareza. A ideia é que as operações de atualização e consulta sigam caminhos diferentes, cada um otimizado para sua função.

Com o crescimento de uma aplicação, surgem problemas como:

Formatos divergentes entre estruturas de leitura e escrita;

Conflitos de concorrência (locks);

Quedas de performance por acesso simultâneo;

Dificuldade de controlar segurança em operações mistas.

A solução: separar o modelo de comandos (escrita) do modelo de consultas (leitura).

Modelo de Escrita

Processa comandos e atualiza dados.

Valida regras de negócio.

Garante consistência das transações.

Modelo de Leitura

Prioriza performance em consultas.

Gera objetos específicos para leitura (DTOs/projeções).

Evita regras complexas, tornando a operação mais rápida.

Mesmo compartilhando o mesmo banco, cada modelo trabalha de forma independente.

Retry Pattern

Esse padrão é usado quando uma operação falha temporariamente, permitindo novas tentativas controladas. É comum em sistemas distribuídos e ambientes em nuvem, onde interrupções momentâneas são frequentes.

Falhas transitórias incluem:

Oscilações de rede;

Serviços temporariamente offline;

Timeouts por sobrecarga.

Estratégias de repetição:

Cancelar: Quando a falha é permanente (ex.: senha inválida).

Repetir imediatamente: Adequado para erros raros.

Repetir com atraso: A estratégia mais utilizada.

Tipos de atraso:

Incremental: Crescimento linear.

Exponencial (Backoff): Intervalos cada vez maiores para evitar sobrecarga.

Fundamentos de Padrões Arquiteturais

Os estilos arquiteturais ajudam a organizar sistemas e orientar decisões de design.

Grande Bola de Lama

Quando o sistema evolui sem controle, vira um amontoado de código cheio de remendos e difícil de manter.

Arquitetura Monolítica

Uma estrutura única onde tudo roda em um único processo. Tradicional, simples, porém limitada para necessidades complexas.

Cliente/Servidor

Divide responsabilidades entre a interface (cliente) e o processamento (servidor).

Desktop + Servidor de Banco de Dados

O cliente trata da exibição e interação; o servidor cuida da manipulação e armazenamento dos dados.

Navegador + Servidor Web

Modelo clássico da web moderna. O navegador é leve e o servidor web centraliza a lógica.

Arquitetura em Camadas (N-Tier)

Modelo tradicional onde a aplicação é organizada em camadas horizontais, cada uma com sua responsabilidade:

Apresentação

Camada Comercial (Negócio)

Persistência

Banco de Dados

Mudanças por funcionalidade atravessam todas as camadas, já que a divisão é técnica, não orientada ao domínio.

Camada Fechada: Respeita a hierarquia.
Camada Aberta: Permite pular camadas (mais flexível, porém mais frágil).

Sinkhole: Quando as camadas passam requisições adiante sem acrescentar valor.

Arquitetura Pipeline

Modelo baseado em fluxo contínuo de dados. É composto por:

Filtros: etapas de processamento independentes;

Canais: caminhos unidirecionais entre os filtros.

Tipos de filtros:
Produtor, Transformador, Verificador e Consumidor.

Arquitetura Microkernel

Muito usada em produtos instaláveis e sistemas modulares. Divide-se em:

Sistema Central: núcleo mínimo e estável;

Plug-ins: módulos especializados que podem ser adicionados ou substituídos.

A comunicação normalmente ocorre via chamadas diretas, mas pode ser feita por serviços externos.

Microsserviços

Arquitetura baseada em pequenos serviços independentes, cada um responsável por um domínio específico. Fortemente influenciada pelo DDD, principalmente pelos Bounded Contexts.

Características principais:

Serviços autônomos e isolados;

Banco de dados próprio por serviço;

Comunicação síncrona ou assíncrona;

Foco em independência e escalabilidade;

Granularidade definida por finalidade, transações e comunicação mínima.

Microsserviços trazem flexibilidade e rapidez evolutiva, porém aumentam complexidade operacional.
