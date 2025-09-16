04/08

Artigo: Pensamento Arquitetônico - Fundamentos da Arquitetura de Software

1- Resuma a diferença entre: Arquitetura e Design

Arquitetura de Software: foca nas decisões de alto nível do sistema que são difíceis de mudar, define estruturas principais, componentes, 
comunicação entre eles e princípios que ajudarão a guiar o desenvolvimento. 

Design de Software: está mais próximo da implementação de baixo nível, detalhando como cada componente ou módulo será construído. 
Define classes, métodos, interfaces, padrões de design e outros aspectos internos que podem ser alterados com menor impacto.

Arquitetura = visão macro, estratégica, de longo prazo.
Design = visão micro, tática, de curto prazo.


2- Como é a formação do conhecimento de um arquiteto modelo T?

Ele combina amplitude e profundidade.
Barra horizontal do T: representa a amplitude de conhecimentos onde o arquiteto precisa entender um pouco de várias áreas 
como bancos de dados, redes, cloud, segurança, metodologias ágeis, conseguindo dialogar com diferentes especialistas.

Barra vertical do T:representa a profundidade em uma área específica onde o arquiteto deve ter especialização sólida em algum domínio técnico 
como por exemplo, integração de sistemas, microsserviços, IA...


05/08

1- O que é abstração?

Abstração significa não considerar ou ignorar algo propositalmente, o que é chamado de “abstrato” é tudo aquilo que não se refere ao mundo físico de forma direta.

2- O que é ocultamento de informações?

É uma técnica da que envolve a incorporação de mensagens secretas em informações públicas para ocultar sua existência, fornecendo uma camada extra de segurança ao tornar as mensagens secretas invisíveis para partes não autorizadas.

3- O que é um código com coesão?

Coesão se refere ao grau em que os elementos dentro de um módulo pertencem um ao outro, é uma medida da força do relacionamento entre os métodos e dados de uma classe e algum propósito ou conceito unificador servido por essa classe.

4- O que é acoplamento?

É o grau de interdependência entre dois componentes de um software, quando há baixo acoplamento o componente consegue operar de forma mais independente do outro, já o alto acoplamento implica em uma conexão forte entre os dois, o que pode torná-los até indistinguíveis.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Robert Martin - referência código limpo

SOLID: Usar a orientação a objetos do jeito mais correto possível.

-----------------------------------------------------------------------------------
S - Single responsability principle (Princípio da responsabilidade única) 

Relação direta com a coesão
Separar as coisas
MVC (dados, html, controla a tela)
Responsabilidade única na hora de construir uma interface gráfica

É um conceito na programação orientada a objetos que estabelece que uma classe deve ter apenas uma única razão para mudar, que deve ser responsável por uma única funcionalidade ou tarefa específica, ou seja,
uma classe não deve ser sobrecarregada com múltiplas responsabilidades que não estão relacionadas entre si.

------------------------------------------------------------------------------------
O - Open-Closed Principle (Princípio Aberto-Fechado) 

As entidades de software (classes, módulos, funções, etc.) devem ser abertas para extensão, mas fechadas para modificação. 
O comportamento de um módulo pode ser estendido sem alterar seu código-fonte. 

------------------------------------------------------------------------------------
L - Liskov Substitution Principle (Princípio da substituição de Liskov) 

Os objetos de uma classe base devem poder ser substituídos por objetos de suas subclasses sem que o comportamento do programa seja alterado. 
Se uma classe A é subtipo de uma classe B, então objetos de tipo A devem poder ser usados em qualquer lugar onde objetos de tipo B são esperados, sem causar erros ou comportamentos inesperados. 

------------------------------------------------------------------------------------
I - Interface Segregation Principle (Princípio da Segregação da Interface) 

Interface que seja bem escrita e que defina como vai ser a comunicação entre essas duas classes
Cada interface tem sua responsabilidade


------------------------------------------------------------------------------------
D - Dependency Inversion Principle (Princípio da inversão da dependência) 

Uma classe deve depender diretamente de uma abstração e não de uma impleentação concreta
É um princípio que afirma que módulos de alto nível não devem depender de módulos de baixo nível, e que ambos devem depender de abstrações. 
