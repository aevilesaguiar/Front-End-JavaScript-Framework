# Front-End-JavaScript-Framework

## Arquitetura multicamada

Na engenharia de software , a arquitetura multicamadas (freqüentemente chamada de arquitetura de n camadas ) é uma arquitetura cliente-servidor na qual as funções de apresentação, processamento de aplicativos e gerenciamento de dados são fisicamente separadas. O uso mais difundido da arquitetura multicamada é a arquitetura de três camadas .

A arquitetura de aplicativos de N camadas fornece um modelo pelo qual os desenvolvedores podem criar aplicativos flexíveis e reutilizáveis. Ao segregar um aplicativo em camadas, os desenvolvedores adquirem a opção de modificar ou adicionar uma camada específica, em vez de retrabalhar o aplicativo inteiro. Uma arquitetura de três camadas normalmente é composta por uma camada de apresentação , uma camada lógica e uma camada de dados(composed of a presentation tier, a logic tier, and a data tier).


## Camadas comuns 

Em uma arquitetura lógica multicamada para um sistema de informação com design orientado a objetos , as quatro seguintes são as mais comuns:

Camada de apresentação (também conhecida como camada de interface do usuário, camada de visualização, camada de apresentação na arquitetura multicamada)
Camada de aplicação (também conhecida como camada de serviço [6] [7] ou camada de controlador GRASP [8] )
Camada de negócios (também conhecida como camada de lógica de negócios (BLL), camada de lógica de domínio)
Camada de acesso a dados (também conhecida como camada de persistência , registro, rede e outros serviços necessários para dar suporte a uma camada de negócios específica)

## Arquitetura de três camadas 

A arquitetura de três camadas é um padrão de arquitetura de software cliente-servidor no qual a interface do usuário (apresentação), lógica de processo funcional ("regras de negócios"), armazenamento de dados do computador e acesso a dados são desenvolvidos e mantidos como módulos independentes , na maioria das vezes em plataformas separadas . [11] Foi desenvolvido por John J. Donovan na Open Environment Corporation (OEC), uma empresa de ferramentas que ele fundou em Cambridge, Massachusetts .

Além das vantagens usuais do software modular com interfaces bem definidas, a arquitetura de três camadas destina-se a permitir que qualquer uma das três camadas seja atualizada ou substituída de forma independente em resposta a mudanças nos requisitos ou na tecnologia . Por exemplo, uma mudança de sistema operacional na camada de apresentação afetaria apenas o código da interface do usuário.

Normalmente, a interface do usuário é executada em um PC desktop ou estação de trabalho e usa uma interface gráfica de usuário padrão , lógica de processo funcional que pode consistir em um ou mais módulos separados executados em uma estação de trabalho ou servidor de aplicativos e um RDBMS em um servidor de banco de dados ou mainframe que contém a lógica de armazenamento de dados do computador. A camada intermediária pode ter várias camadas (nesse caso, a arquitetura geral é chamada de " arquitetura de n camadas").

Camada de aplicativo (lógica de negócios, camada lógica ou camada intermediária)

A camada lógica é extraída da camada de apresentação e, como sua camada, controla a funcionalidade de um aplicativo realizando processamento detalhado.

Camada de dados

A camada de dados inclui os mecanismos de persistência de dados (servidores de banco de dados, compartilhamentos de arquivos, etc.) e a camada de acesso a dados que encapsula os mecanismos de persistência e expõe os dados. A camada de acesso a dados deve fornecer uma API para a camada de aplicativo que expõe métodos de gerenciamento dos dados armazenados sem expor ou criar dependências nos mecanismos de armazenamento de dados. Evitar dependências nos mecanismos de armazenamento permite atualizações ou alterações sem que os clientes da camada de aplicativo sejam afetados ou mesmo cientes da alteração. Assim como na separação de qualquer camada, há custos de implementação e, muitas vezes, custos de desempenho em troca de escalabilidade e capacidade de manutenção aprimoradas.

Uso de desenvolvimento web 

No campo de desenvolvimento web , três camadas é frequentemente usado para se referir a sites , geralmente sites de comércio eletrônico , que são construídos usando três camadas:

Um servidor web de front-end servindo conteúdo estático e potencialmente algum conteúdo dinâmico em cache . Em aplicativos baseados na web, front-end é o conteúdo renderizado pelo navegador. O conteúdo pode ser estático ou gerado dinamicamente.
Um servidor de aplicativos de nível de geração e processamento de conteúdo dinâmico intermediário (por exemplo, Symfony , Spring , ASP.NET , Django , Rails , Node.js ).
Um banco de dados ou armazenamento de dados de back-end , que inclui conjuntos de dados e o software do sistema de gerenciamento de banco de dados que gerencia e fornece acesso aos dados.


Lógica de apresentação - a interface do usuário (UI) que exibe dados para o usuário e aceita a entrada do usuário. Em uma aplicação web esta é a parte que recebe a requisição HTTP e retorna a resposta HTML.
Lógica de negócios - lida com validação de dados, regras de negócios e comportamento específico da tarefa.
Lógica de acesso a dados - comunica-se com o banco de dados construindo consultas SQL e executando-as por meio da API relevante.
## Referencias



As regras da arquitetura de 3 camadas


Simplesmente não é bom o suficiente dividir o código de um aplicativo em 3 partes e chamá-lo de "3 Camadas" se o código dentro de cada camada não se comportar de uma determinada maneira. Existem regras a serem seguidas, mas essas regras são bastante simples.

O código para cada camada deve estar contido em arquivos separados que podem ser mantidos separadamente, possivelmente por equipes separadas.
Cada camada pode conter apenas o código que pertence a essa camada. Assim, a lógica de negócios só pode residir na camada de negócios, a lógica de apresentação na camada de apresentação e a lógica de acesso a dados na camada de acesso a dados.
A camada de Apresentação só pode receber solicitações e retornar respostas para um agente externo. Geralmente é uma pessoa, mas pode ser outro software.
A camada de Apresentação só pode enviar solicitações e receber respostas da camada de Negócios. Ele não pode ter acesso direto ao banco de dados ou à camada de acesso a dados.
A camada de Negócios só pode receber solicitações e retornar respostas para a camada de Apresentação.
A camada de negócios só pode enviar solicitações e receber respostas da camada de acesso a dados. Ele não pode acessar o banco de dados diretamente.
A camada de acesso a dados só pode receber solicitações e retornar respostas para a camada de negócios. Ele não pode emitir solicitações para nada além do DBMS que ele suporta.
Cada camada deve ser totalmente inconsciente do funcionamento interno das outras camadas. A camada Business, por exemplo, deve ser independente de banco de dados e não conhecer ou se preocupar com o funcionamento interno do objeto Data Access. Também deve ser agnóstico de apresentação e não saber ou se importar como seus dados serão tratados. Ele não deve processar seus dados de maneira diferente com base no que o componente receptor fará com esses dados. A camada de apresentação pode pegar os dados e construir um documento HTML, um documento PDF, um arquivo CSV ou processá-lo de alguma outra forma, mas isso deve ser totalmente irrelevante para a camada de Negócios.

![image](https://user-images.githubusercontent.com/52088444/186148370-2d979125-1773-44f5-9825-3faf24589f14.png)

Se você observar cuidadosamente essas camadas, verá que cada uma requer diferentes conjuntos de habilidades:

A camada de apresentação requer habilidades como HTML, CSS e possivelmente JavaScript, além de design de interface do usuário.
A camada de negócios requer habilidades em uma linguagem de programação para que as regras de negócios possam ser processadas por um computador.
A camada de acesso a dados requer habilidades de SQL na forma de linguagem de definição de dados (DDL) e linguagem de manipulação de dados (DML), além de design de banco de dados.
Embora seja possível que uma única pessoa tenha todas as habilidades acima, essas pessoas são bastante raras. Em grandes organizações com grandes aplicativos de software, essa divisão de um aplicativo em camadas separadas possibilita que cada camada seja desenvolvida e mantida por equipes diferentes com as habilidades especializadas relevantes.
![image](https://user-images.githubusercontent.com/52088444/186149029-82445bf6-e9fa-4760-bc77-48a713ab8f4d.png)

Arquitetura de 3 camadas em operação

Quando um aplicativo é desenvolvido, ele não é (ou não deve ser) construído a partir de um único componente grande. Geralmente, há muitos componentes pequenos (às vezes chamados de 'módulos' ou 'classes' em OOP), cada um executando uma função específica, e o aplicativo é a soma dessas partes. Isso permite que novas funcionalidades sejam adicionadas sem necessariamente afetar qualquer componente existente. A vantagem de uma abordagem em camadas é que um componente em uma camada inferior pode ser compartilhado por vários componentes em uma camada superior, conforme mostrado na figura 7 :


![image](https://user-images.githubusercontent.com/52088444/186149291-e690a3c8-9463-488e-883d-9a6557fec85a.png)

Aqui você vê que um componente na camada de Apresentação pode se comunicar com um ou mais componentes na camada de Negócios. Um componente na camada de negócios se comunica com o componente na camada de acesso a dados, mas também pode se comunicar com outros componentes da camada de negócios. Geralmente, há apenas um componente na camada de acesso a dados, pois os bancos de dados do aplicativo geralmente são manipulados por um único mecanismo de DBMS. É possível alternar para um mecanismo DBMS diferente simplesmente alterando esse único componente. Também é tecnicamente possível que diferentes partes do aplicativo lidem com diferentes mecanismos de DBMS ao mesmo tempo, conforme mostrado na figura 9 .

Na minha maior aplicação, tenho 2.000 componentes (transações do usuário) na camada de apresentação, 250 na camada de negócios e 1 na camada de acesso a dados. Ouvi falar de algumas implementações que têm um Data Access Object (DAO) separado para cada tabela individual no banco de dados, mas desenvolvedores mais experientes podem obter a mesma funcionalidade com apenas um. Em minha própria implementação, por exemplo, um único DAO pode lidar com todas as tabelas do banco de dados. No entanto, tenho um arquivo de classe separado para cada um dos principais mecanismos de DBMS - MySQL, PostgreSQL, Oracle e SQL Server - para poder alternar facilmente de um para outro alterando uma única entrada no meu arquivo de configuração.

Observe também que a conexão com o banco de dados não é aberta por nenhum componente da camada de Apresentação. Isso só deve ser feito dentro da camada de acesso a dados quando instruído a fazê-lo pela camada de negócios, e apenas um momento antes de uma operação no banco de dados ser realmente necessária. Isso é chamado de método "Just In Time" (JIT) em comparação com o método "Just In Case" (JIC). Quando a camada de Negócios decide que precisa falar com o banco de dados ela segue os seguintes passos:

Identifique qual DBMS é relevante para a tabela do banco de dados.
Instancie um objeto do arquivo de classe relevante, que geralmente é um singleton compartilhado.
Passe uma coleção de variáveis ​​para o objeto DBMS que será usado para construir a consulta relevante. Isso permite que a consulta seja construída de acordo com as necessidades desse mecanismo de DBMS específico. Os bancos de dados Oracle e SQL Server, por exemplo, não utilizam OFFSET e LIMIT para paginação.
Execute a consulta e aguarde a resposta.
Lide com a resposta antes de devolvê-la como uma matriz. Diferentes mecanismos de DBMS, por exemplo, têm métodos diferentes para lidar com colunas ou sequências de incremento automático, de modo que o código para lidar com essas diferenças está contido no objeto DBMS e totalmente invisível para o objeto de chamada.
Essa abordagem permite que uma instância do meu aplicativo acesse tabelas de banco de dados em mais de um servidor e até mais de um mecanismo DBMS.

## As arquiteturas MVC e 3-Tier não são a mesma coisa?

Existem alguns programadores que, ao ouvirem que uma aplicação foi dividida em 3 áreas de responsabilidade, automaticamente assumem que têm as mesmas responsabilidades que o padrão de projeto Model-View-Controller (MVC) . Este não é o caso. Embora existam semelhanças, também existem algumas diferenças importantes:

A Visualização e o Controlador se encaixam na camada de Apresentação.

Embora as camadas Modelo e Negócios pareçam idênticas, o padrão MVC não possui um componente separado dedicado ao acesso aos dados.
As sobreposições e diferenças são mostradas na Figura 8 e na Figura 8a :
![image](https://user-images.githubusercontent.com/52088444/186150508-fe2a6d5f-0d54-4677-b58f-b1ebd61321cb.png)

Aqui está um diagrama alternativo que mostra a mesma informação de uma maneira diferente:

![image](https://user-images.githubusercontent.com/52088444/186150677-38532f67-4cbb-4340-beef-689021cc46f1.png)

Você pode pensar que qualquer implementação do MVC pode ser considerada automaticamente como uma implementação do 3-Tier, mas esse não é o caso. Em cada implementação do MVC que vi até agora, houve um erro simples, mas fundamental, que torna isso impossível, e é aí que a conexão com o banco de dados é feita. Na Arquitetura de 3 Camadas, toda a comunicação com o banco de dados, incluindo a abertura de uma conexão, é feita na camada de Acesso a Dados mediante o recebimento de uma solicitação da camada de Negócios. A camada de Apresentação não possui comunicação com o banco de dados, apenascomunicar com ele através da camada de negócios. Com todos os frameworks MVC que vi até agora, a conexão com o banco de dados é feita dentro do controlador e o objeto de conexão é então passado para o modelo que o usa quando necessário. Este é um erro muitas vezes cometido por iniciantes e por aqueles que foram mal educados.

O pior exemplo desse erro que eu já vi foi quando um Controller abriu 3 conexões diferentes para a mesma instância do servidor de banco de dados para se comunicar com 3 bancos de dados diferentes nesse servidor. Cada uma dessas conexões foi então passada para um componente de modelo diferente que pode não usar essa conexão. Um programador experiente identificará imediatamente as falhas nessa abordagem, falhas que podem ter um impacto significativo no desempenho:

Abrir várias conexões com o mesmo servidor apenas para acessar bancos de dados diferentes nesse servidor é um desperdício de recursos. Um programador competente saberá que, uma vez estabelecida uma conexão, é possível alternar a identidade do banco de dados padrão ou até mesmo prefixar cada nome de tabela na consulta SQL com o nome do banco de dados relevante. É possível acessar várias tabelas de vários bancos de dados em uma única consulta, portanto, não é necessário ter uma conexão separada para cada banco de dados. Tudo o que é necessário é que o aplicativo esteja ciente dos nomes das tabelas eseus nomes de banco de dados associados e que o DAO seja inteligente o suficiente para lembrar o nome do banco de dados atual para que possa alternar para outro quando necessário. Infelizmente, a maioria dos frameworks MVC assume que todas as tabelas estão contidas em um único banco de dados, o que torna o uso de vários bancos de dados um pouco problemático.
Abrir uma conexão antes que ela seja realmente necessária é um desperdício de recursos. Este é o método "Just In Case" (JIC) onde o que deve ser utilizado é o método "Just In Time" (JIT).

Outro erro que encontrei com algumas implementações é que elas pensam que a validação de dados (às vezes chamada de 'filtragem de dados') deve ser realizada dentro do controlador antes de ser passada para o modelo. Isso não se encaixa na definição da Arquitetura de 3 Camadas, que afirma que essa lógica de validação de dados, juntamente com a lógica de negócios e o comportamento específico da tarefa, deve existir apenasdentro da camada de negócios ou componente do modelo. Ao retirar a validação de dados do modelo e colocá-la no controlador, você está efetivamente criando um acoplamento rígido entre o controlador e o modelo, pois esse controlador não pode ser reutilizado com um modelo diferente, e o acoplamento rígido é algo que deve ser evitado para para produzir software 'melhor'. O acoplamento fraco permitiria que um controlador fosse compartilhado por várias classes de modelo em vez de ser fixado em apenas uma.

Quando implementada corretamente, uma aplicação desenvolvida utilizando a Arquitetura de 3 Camadas deve ter toda a sua lógica – validação de dados, regras de negócio e comportamento específico da tarefa – confinada à camada de Negócios. Não deve haver lógica de aplicativo nas camadas de Apresentação e Acesso a Dados, permitindo assim que qualquer uma dessas duas camadas seja alterada sem afetar nenhuma lógica de aplicativo.

## Quais são os benefícios da arquitetura de 3 camadas?

Está tudo muito bem descrevendo algo como a Arquitetura de 3 Camadas, mas ninguém vai se esforçar para mudar de seu arranjo atual a menos que haja benefícios a serem feitos, então quais são exatamente os benefícios dessa arquitetura? De acordo com alguns, há muitas despesas, mas nenhum benefício, conforme expresso no seguinte blog do Sitepoint :

Sua função principal (independência da interface do usuário, regras de negócios e armazenamento/recuperação de dados) só ajuda na migração ou extensão para outra linguagem de script/motor de dados/plataforma. Mas isso só acontece muito poucas vezes em uma vida útil do aplicativo.


Esta é uma visão muito limitada de uma pessoa de experiência limitada. O objetivo de usar a Arquitetura de 3 Camadas não é apenas facilitar apenas quando você altera seu mecanismo de banco de dados ou linguagem de programação. Também é útil quando você deseja substituir sua camada de apresentação ou criar uma camada de apresentação adicional . Se você já trabalhou em uma variedade de aplicativos de 3 camadas e não de 3 camadas, poderá ver as diferenças e, portanto, as vantagens por si mesmo.

As principais vantagens da Arquitetura de 3 Camadas são frequentemente citadas como:

Flexibilidade - Ao separar a lógica de negócios de um aplicativo de sua lógica de apresentação, uma arquitetura de 3 camadas torna o aplicativo muito mais flexível a alterações.
Manutenibilidade - As alterações nos componentes em uma camada não devem ter efeito em nenhuma outra camada. Além disso, se camadas diferentes exigirem habilidades diferentes (como HTML/CSS é a camada de apresentação, PHP/Java na camada de negócios, SQL na camada de acesso a dados), elas podem ser gerenciadas por equipes independentes com habilidades nessas áreas específicas.
Reutilização - Separar o aplicativo em várias camadas facilita a implementação de componentes reutilizáveis. Um único componente na camada de negócios, por exemplo, pode ser acessado por vários componentes na camada de apresentação, ou mesmo por várias camadas de apresentação diferentes (como desktop e web) ao mesmo tempo.
Escalabilidade - Uma arquitetura de 3 camadas permite a distribuição de componentes de aplicativos em vários servidores, tornando o sistema muito mais escalável.
Confiabilidade - Uma arquitetura de 3 camadas, se implantada em vários servidores, torna mais fácil aumentar a confiabilidade de um sistema implementando vários níveis de redundância.

Outro benefício não tão óbvio que só pode vir da exposição real ao desenvolvimento de vários aplicativos usando a Arquitetura de 3 Camadas é que se torna possível criar uma estrutura para construir novos aplicativos em torno dessa arquitetura. Como cada uma das camadas é especializada em apenas uma área da aplicação, é possível ter mais componentes reutilizáveis ​​que tratam de cada uma dessas áreas. Esses componentes podem ser pré-construídos e entregues como parte da estrutura ou gerados pela própria estrutura. Isso reduz o esforço necessário para criar um novo aplicativo e também reduz o esforço necessário para manter esse aplicativo.

Se você acha que essa estrutura ainda não foi escrita, então você não ouviu falar da Radicore .

Por que o Front-End e o Back-End requerem camadas de Apresentação diferentes?
Esta é uma pergunta que muitas vezes me fazem pessoas inexperientes, e as razões, que são detalhadas em Web Site vs Web Application , podem ser resumidas como:

Eles são usados ​​por pessoas diferentes
Eles servem a um propósito diferente
Eles têm um "look and feel" diferente

As telas no front-end precisam atrair visitantes, assim como um showroom ou uma loja de rua. Eles são de formato livre e geralmente construídos usando HTML complexo, CSS, JavaScript e muitos gráficos sensuais. Eles também podem conter código para lidar com Search Engine Optimization (SEO), análises, marketing de afiliados, banners de publicidade e outras coisas de marketing.

As telas no back-end são muito mais simples, pois tudo o que eles precisam fazer é permitir que os membros da equipe façam seus trabalhos da maneira mais rápida e eficiente possível e, portanto, precisam ser funcionais e não sexy. Eles não precisam de HTML, CSS ou JavaScript complexo e certamente não precisam de gráficos sensuais, SEO ou outras coisas de marketing. 

Como eles lidam com os dados do banco de dados que são organizados em linhas e colunas, eles podem ser resumidos em duas estruturas de tela comuns - a visualização LIST que mostra várias linhas em um arranjo horizontal e o DETAILvista que mostra uma única linha em uma disposição vertical. Isso significa que as telas no back-end podem ser construídas mais facilmente a partir de modelos padrão, enquanto as telas no front-end geralmente são feitas à mão uma a uma. Geralmente, existem algumas telas adicionais no back-end que podem precisar de consultas SQL complexas para que os dados possam ser extraídos e apresentados em uma variedade de relatórios de gerenciamento.

Há também mais telas no back-end do que no front-end (a proporção pode chegar a 100:1), e nem todas as funções disponíveis no back-end estarão disponíveis no front-end enquanto qualquer coisa que possa ser feito no front-end também deve ser possível no back-end. Por exemplo, em aplicativos de comércio eletrônico, o site front-end é usado pelos clientes para inserir seus pedidos, mas sempre deve haver uma função de entrada de pedidos disponível no back office.

Devido a essas diferenças significativas entre o front-end e o back-end, deve ser fácil ver que:

Eles exigem habilidades de desenvolvimento diferentes.
Eles podem ser construídos em diferentes idiomas.
Se construídos na mesma linguagem, eles podem usar estruturas diferentes.

O objetivo principal de um site front-end é apresentar a organização ao mundo exterior para atrair clientes. O objetivo principal do aplicativo de back-end é a administração dos dados da organização e a aplicação das regras de negócios. Ambos compartilham o mesmo conjunto de dados, ambos compartilham o mesmo conjunto de regras de negócios, e é apenas na maneira como os dados são apresentados aos seus respectivos conjuntos de usuários e nas funções que eles são capazes de executar, o que é diferente. Você deve ver que os termos "apresentação", "regras de negócios" e "dados" são uma combinação perfeita para as diferentes camadas da arquitetura de 3 camadas,



## Referencias

- https://en.wikipedia.org/wiki/Multitier_architecture
- http://www.tonymarston.net/php-mysql/3-tier-architecture.html
