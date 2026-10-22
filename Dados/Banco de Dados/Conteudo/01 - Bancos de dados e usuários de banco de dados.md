
Atualmente, a maioria das nossas atividades acessa um banco de dados. Essas interações podem ser chamadas de **aplicações de banco de dados tradicionais**, em que a maior parte dos dados é armazenada como texto ou número.

Todavia, estão surgindo diversas outras formas de se armazenar dados, como: **banco de dados multimídia**, que armazenam imagens, vídeos, arquivos; **sistemas de informações geográficas**, que podem analizar e armazenar informaçẽos catográficas; e **data warehouses e sistemas OLAP**, que apoiam empresas na análise de dados e na tomada de decisões; entre outros.
# 1 Introdução

Genericamente, **banco de dados** é definido como uma **coleção de dados** relacionados. Porém, ele possui alguma propriedades implícitas:

- Um banco de dados representa algum aspecto do mundo real, às vezes chamado de mini-mundo ou de **universo de discurso**.
	- As mudanças no mundo real devem ser refletidas o mais rápido possível na representação do mini-mundo.
- Um banco de dados é uma coleção logicamente coerente de dados com algum significado inerente.
- Um banco de dados é projetado, construído e populado com dados para uma finalidade específica. 

> Em outras palavras, um banco de dados tem alguma fonte da qual o dado é derivado, algum grau deinteração com eventos no mundo real e um público que está ativamente interessado em seu conteúdo.

Um banco de dados pode ser gerido manualmente ou por computador através de um **SGBD** (*Sistema de Gerenciamente de Banco de Dados*) queé um sistema de software de uso geral que facilita o processo de:

- **Definição**: um banco de dados envolve especificar os tipos, estruturas e restrições dos dados a serem armazenados. As definições de um banco de dados também é armazenada em um catálogo chamado de **metadados**;
- **Construção**: é o processo de armazenar os dados;
- **Manipulação**:  é o processo de recuperação, atualização dos dados para refletir o mini-mundo e geração de relatório;
- **Compartilhamento de bancos de dados**: permite que diversos usuários e programas acessem-no simultaneamente;
- **Proteção**: inclui a proteção do sistema contra falha de hardware ou software e proteção contra acessos indevidos ou maliciosos;
- **Manutenção**: é o ato de permitir que o banco de dados evolua à medida que os requisitos mudam com o tempo.

Abaixo, um diagrama simplificado de um sistema de banco de dados.

<div align="center">
  <img src="Pasted image 20261020223825.png" width="45%">
  <br>
  <em>Figura 1: Diagrama simplificado de um ambiente de banco de dados.</em>
</div>

# 2 Características da abordagem de banco de dados

Na abordagem de banco de dados, um único repositório mantém os dados que são definidos apenas uma vez que podem ser reutilizados, diferentemente de sistemas de arquivos onde cada aplicação é livre para gerenciar seus dados independentemente.

## 2.1 Natureza de autodescrição de um sistema de banco de dados

Um banco de dados possui uma autodescrição de seus dados que é a definição completa de sua estrutura e restrições, chamada de **metadados**. Essas definições são especificadas pelo projetista antes da criação do banco de dados real e armazenadas no catálogo.

## 2.1 Isolamento entre programas e dados, e abstração de dados

No processamento de arquivos tradicional, a estrutura dos arquivos de dados está embutida nos pro gramas de aplicação, de modo que quaisquer mudanças em sua estrutura podem exigir alteração em todos os programas que acessam esse arquivo. Ao contrário, os programas que acessam o SGBD não exigem tais mudanças na maioria dos casos. A estrutura dos arquivos de dados é armazenada no catálogo do SGBD separadamente dos programas de acesso, isso é chamado de **independência entre dados e programa**.

Os programas que utilizam SGBDs podem operar sobre esses dados por meio do nome das operações que o SGBD suporta, independemente de sua implementação, a isso chamamos de **independência da operação do programa**.

A característica que permite essas duas independências é a **abstração de dados**. Um SGBD oferece aos usuários uma representação conceitual que não expoem muitos detalhes dados são armazenados ou como as operações são implementadas, usando conceitos lógicos, como objetos, suas propriedades e seus interrelacionamentos, que podem ser mais fáceis para os usuários entende- rem do que os conceitos de armazenamento de computador.

## 2.3 Suporte para múltiplas visões dos dados

Como um banco de dados, geralmente, tem muitos usuários e cada pode exigir um ponto de vista (**visão**) diferente do banco de dados, é importante que um SGBD tenha suporte à múltiplas visões de dados. Uma visão (ou view) pode ser um subconjunto do banco de dados ou conter dado virtual que é derivado dos arquivos do banco de dados, mas não estão armazenados explicitamente. Alguns usuários não precisam saber se os dados a que se referem estão armazenados ou se são derivados.

## 2.4 Compartilhamento de dados eprocessamento de transação multiusuário

Um SGBD multiusuário deve permitir que vários usuários possam usar o banco de dados ao mesmo tempo. O SGBD precisa incluir um software de controle de concorrência para garantir que vários usuários tentando atualizar o mesmo dado faça isso de uma maneira controlada, de modo que o resultado dessas atualizações seja correto.

Esses tipos de aplicações geralmente são chamados de aplicações de processamento de transação on-line (**OLPT — On-Line Transaction Processing**). É importante definir **transação** que é um *programa em execução que inclui acessos a um banco de dados* para leitura ou atualização dos registros.

Um SGBD deve garantir, durante as transações, as propriedades de **atomicidade**, que garante que todas as operações em uma transação sejam executadas ou que nenhuma seja, e **isolamento** garante que cada transação pareça executar isoladamente das demais.

# 3 Atores

Para grandes bancos de dados é importante dividir as responsabilidades e funções de cada usuário.

## 3.1 Adminsitradores de Banco de Dados (DBA)

O administrador de banco de dados é o responsável por supervisionar e gerenciar a infraestrutura de dados em organizações onde múltiplos usuários compartilham os mesmos recursos. Nessa função, o banco de dados figura como o recurso principal sob sua gestão, enquanto o SGBD (Sistema Gerenciador de Banco de Dados) e os softwares associados constituem os recursos secundários. 

As atribuições do DBA envolvem autorizar permissões de acesso, monitorar, coordenar a utilização do sistema, e providenciar aquisição de recursos de hardware e software conforme as necessidades operacionais. Ele também responde diretamente pela solução de falhas de segurança e por problemas de desempenho, como a lentidão no tempo de resposta do sistema.

## 3.2 Projetistas de banco de dados

Os projetistas de banco de dados são responsáveis por identificar os dados a serem armazenados e escolher estruturas apropriadas para representar e armazenar esses dados, além de estabelecer **visões** para cada grupo de usuário. Essas tarefas são realizadas principalmente antes que o banco de dados esteja real­mente implementado e populado com dados. 

Para projetar, ele precisa se comunicar com todos os potenciais usuários a fim de entender suas necessidades e criar um projeto que as atenda.

## 3.3 Usuários Finais

Os **usuários finais** são aqueles usuários cujas funções exigem o acesso ao banco de dados para consultar, atualiazar e gerar relatórios. Podem ser separados em tipos, entre eles:

- **Usuários Finais Casuais:** ocasionalmente acessam o banco de dados, mas podem precisar de diferentes informações a cada vez. Utilizam uma linguagem sofisticada de consulta ao banco de dados para especificar suas necessidades e normalmente são gerentes de nível intermediário ou alto, ou outros usuários ocasionais.
- **Usuários Finais Iniciantes ou Paramétricos**: é a maior parte dos usuários finais. Sua principal função é consultar e atualizar os dados, geralmente, usando tipos padrão, as **transações programadas**.
- **Usuários Finais Sofisticados**: incluem profissionais que estão profundamente familiarizados com as facilidades do SGBD a ponto de implementar as próprias aplicações para que atendam a suas necessidades complexas.
- **Usuários Isolados**: mantêm bancos de dados pessoais usando pacotes de programas prontos, que oferecem interfaces de fácil utilização, baseadas em menus ou gráfico.

## 3.4 Analistas de sistemas e programadores de aplicações (engenheiros de software)

Os **analistas de sistemas** identificam as necessidades do usuários finais, definem as especificações das transações que as atendam.  Os **programadores** implementam essas especificações como programas, testam, depuram, documentam e mantém essas transações programadas.

# 4 Trabalhadores dos Bastidores

Além daqules que administram e projetam, há outros associados ao projeto, desenvolvimento e operação. Geralmente, elas não estão interessadas no conteúdo dos dados.

- **Projetistas e Implementadores do Sistema de SGBD**: projetam e implementam os módulos e as interfaces do SGBD como um pacote de software. Um SGBD é um sistema muito complexo, que consiste em muitos componentes, ou módulos, incluindo módulos para implementação do catálogo, processamento de linguagem de consulta, processamento de interface, acesso e buffering de dados, controle de concorrência e tratamento de recuperação e segurança de dados.
- **Desenvolvedores de ferramentas**: projetam e implantam ferramentas — os pacotes de software que facilitam a modelagem e o projeto do banco de dados, o projeto do sistema de banco de dados e a melhoria no desempenho. Ferramentas são pacotes opcionais que, em geral, são adquiridos separadamente.
- **Operadores e pessoal de manutenção**: são responsáveis pela execução e manutenção do ambiente de hardware e software para o sistema de banco de dados.

# 5 Vantagens de usar a abordagem de SGBD

As vantagens de utilizar um SGBD são:

- **1. Controlando a redundância**: nos **sistemas de arquivos** antigos, cada grupo mantinha seus próprios arquivos que poderiam armazenar os mesmos dados de outros grupos, gerando uma **redundância**. 
	- Isso traz alguns problemas:
		- Problemas de atualização lógica, pois para cada arquivo pode ser necessário atualizar os dados, isso ocasiona uma **deduplicação de esforço**;
		- O espaço de armazenamento é **desperdiçado** quando o mesmo dado é armazenado em diversos arquivos;
		- Os arquivos que armazenam o mesmo dado podem se tornar **inconsistentes**;
	- Na abordagem de **banco de dados**, as visões dos diferentes grupos de usuários são integradas durante o projeto, e o ideal é que cada item de dados lógico seja armazenado em um único lugar. Isso é a **normalização**, que garante consistência e economia de espaço. Na prática, porém, às vezes é necessário recorrer à **redundância controlada** (**a desnormalização**) para melhorar o desempenho das consultas, já que reunir os dados em um só arquivo evita pesquisar vários arquivos para obtê-los. Nesses casos, o SGBD deve ser capaz de controlar essa redundância, impedindo inconsistências entre os arquivos. Isso é feito por verificações especificadas durante o projeto do banco e impostas automaticamente a cada atualização, que conferem se os valores redundantes coincidem com os registros originais. Sem esse controle, podem surgir registros incoerentes.
- **2. Restringindo o acesso não autorizado**: é comum que se tenha restrições de acesso aos usuários. Um SGBD deve oferecer um subsistema de segurança e autorização, que o DBA utiliza para criar contas e especificar suas restrições. Então, o SGBD deve impor essas restrições automaticamente
- **3. Oferecendo armazenamento persistente para objetos do programa**: os bancos de dados podem oferecer **armazenamento persistente** para objetos e estruturas de dados de programas, e esse é um dos principais motivos para a existência dos sistemas de banco de dados orientados a objeto.
- **4. Oferecendo estruturas de armazenamento e técnicas de pesquisa para o processamento eficiente de consulta**: os sistemas de banco de dados precisam executar consultas e atualizações de modo eficiente. Como o banco de dados costuma ficar armazenado em disco, o SGBD oferece estruturas de dados e técnicas de pesquisa especializadas para agilizar a busca dos registros desejados. Para isso, usam-se arquivos auxiliares chamados **índices**, normalmente baseados em **estruturas de árvore** ou de **hash**. Como os registros precisam ser copiados do disco para a memória principal para serem processados, o SGBD geralmente possui um módulo de **buffering** ou **caching**, que mantém partes do banco de dados em **buffers** na memória. Embora o **buffering** de disco para memória seja, em geral, responsabilidade do sistema operacional, ele é tão essencial ao desempenho que a maioria dos SGBDs realiza o próprio buffering. Além disso, o módulo de processamento e otimização de consultas escolhe um plano de execução eficiente para cada consulta, com base nas estruturas de armazenamento existentes. Já a escolha de quais índices criar e manter faz parte do projeto e ajuste do banco de dados físico, uma das responsabilidades da equipe de DBAs.
- **5. Oferecendo backup e recuperação**: um SGBD precisa se recuperar de falhas de hardware ou software, e quem cuida disso é o **subsistema de backup e recuperação**. Se o sistema falhar no meio de uma transação, esse subsistema deve restaurar o banco ao estado anterior à transação ou, alternativamente, retomá-la do ponto em que parou, de modo que seu efeito completo seja registrado. O backup de disco também é necessário para o caso de uma falha de disco catastrófica.
- **6. Oferecendo múltiplas interfaces do usuário**: como os usuários de um banco de dados têm perfis e níveis de conhecimento técnico muito diferentes, o SGBD deve oferecer uma variedade de interfaces. Entre elas estão as linguagens de consulta, voltadas a usuários casuais, as interfaces de linguagem de programação, para programadores de aplicação, os formulários e códigos de comando, para usuários paramétricos, e as interfaces controladas por menu e de linguagem natural, para usuários isolados. As interfaces de formulários e de menus costumam ser chamadas de interfaces gráficas do usuário (GUIs), para as quais existem diversas linguagens e ambientes especializados. Também é comum que o SGBD ofereça recursos para disponibilizar essas interfaces para um banco de dados na Web.
- **7. Representando relacionamentos complexos entre dados**: um banco de dados pode conter muitos tipos de dados inter-relacionados de diversas maneiras. Por isso, o SGBD precisa ser capaz de representar relacionamentos complexos entre os dados, definir novos relacionamentos à medida que eles surgem e recuperar e atualizar dados relacionados de modo fácil e eficaz.
- **8. Impondo restrições de integridade**: a maioria das aplicações de banco de dados possui restrições de **integridade** que precisam ser mantidas, e o SGBD deve oferecer meios de defini-las e impô-las. 
	- São os tipos de restrições:
		- A mais simples é a especificação do **tipo** de dado de cada item. 
		- Um tipo mais complexo é a restrição de **integridade referencial**, que exige que um registro esteja relacionado a registros de outros arquivos. 
		- Há também a **restrição de chave** (ou de singularidade), que exige valores exclusivos para determinado item de dado. 
	- Essas restrições derivam da semântica dos dados e do minimundo que eles representam, e cabe aos projetistas identificá-las durante o projeto do banco. Algumas podem ser especificadas ao SGBD e impostas automaticamente, enquanto outras precisam ser verificadas por programas de atualização ou na entrada de dados. Em grandes aplicações, costumam ser chamadas de regras de negócio. Mesmo com essas restrições, um dado pode ser inserido de forma errada e ainda assim ser válido, e o SGBD não consegue detectar esse tipo de erro, que só pode ser descoberto e corrigido manualmente. Já um valor fora do domínio permitido é rejeitado automaticamente. Além disso, cada modelo de dados possui regras inerentes, assumidas de modo automático para garantir a validade do modelo.
- **9. Permitindo dedução e ações usando regras**: alguns sistemas permitem definir regras de **dedução** (ou **inferência**) para obter novas informações a partir dos fatos armazenados no banco de dados, e por isso são chamados de **sistemas de banco de dados dedutivos**. Essas regras são especificadas de forma declarativa e mantidas pelo SGBD, enquanto em um SGBD tradicional seria necessário escrever código procedural explícito. Nos sistemas relacionais atuais, é possível associar gatilhos (**triggers**) às tabelas: regras ativadas por atualizações que executam operações adicionais em outras tabelas, enviam mensagens e assim por diante. Procedimentos mais elaborados para impor regras são chamados de procedimentos armazenados (**stored procedures**), que passam a fazer parte da definição do banco de dados e são chamados quando certas condições são atendidas. 
- **10. Implicações adicionais do uso da abordagem de banco de dados**: as implicações adicionais são:
	- Potencial para garantir padrões: ela permite que o DBA defina e imponha padrões (nomes e formatos de dados, formatos de exibição, estruturas de relatório, terminologia), o que facilita a comunicação e a cooperação entre departamentos e é mais simples em um ambiente centralizado do que quando cada grupo controla seus próprios arquivos e software.
	- Tempo reduzido para desenvolvimento de aplicação: também reduz o tempo de desenvolvimento de aplicações, embora projetar um grande banco de dados multiusuário do zero possa levar mais tempo do que escrever uma única aplicação de arquivo, depois que ele está pronto, criar novas aplicações com as facilidades do SGBD leva de um sexto a um quarto do tempo de um sistema de arquivos tradicional. 
	- Flexibilidade: há mais flexibilidade, pois os SGBDs modernos permitem mudanças evolutivas na estrutura do banco, como acrescentar arquivos ou estender elementos de dados, sem afetar os dados armazenados nem as aplicações existentes.
	- Disponibilidade de informações atualizadas: há ainda a disponibilidade de informações atualizadas, onde uma atualização feita por um usuário fica imediatamente visível aos demais, algo essencial em sistemas de reserva e bancos de dados bancários, e possibilitado pelos subsistemas de controle de concorrência e recuperação.
	- Economias de escala: a consolidação de dados e aplicações gera economias de escala, reduzindo sobreposições e redundâncias entre departamentos e permitindo à organização investir em equipamentos mais poderosos, em vez de cada setor comprar o seu, o que diminui os custos gerais de operação e gerenciamento.

# 6 Uma breve história das aplicações de banco de dados

Agora, vamos apresentar uma breve visão histórica das aplicações que usam SGBDs e como elas motivaram o desenvolvimento de novos tipos de sistemas de banco de dados.

## 6.1 Antigas aplicações de banco de dados usando sistemas hierárquicos e de rede

Os sistemas de banco de dados antigos mantinham registros em grandes organizações, como corporações, universidades, hospitais e bancos, com muitos registros de estrutura semelhante e diversos inter-relacionamentos entre eles. Um dos principais problemas era a mistura dos relacionamentos conceituais com o armazenamento e o posicionamento físico dos registros no disco, o que limitava a abstração de dados e a independência entre dados e programas. Essa organização favorecia o acesso eficiente às consultas e transações originais, mas dava pouca flexibilidade para novas consultas que exigissem outra organização de armazenamento, e reorganizar o banco diante de mudanças nos requisitos era muito trabalhoso.

Outra deficiência é que esses sistemas ofereciam apenas interfaces de linguagem de programação, o que tornava demorada e cara a implementação de novas consultas e transações, já que exigiam novos programas escritos, testados e depurados. Eram implantados em grandes mainframes, de meados da década de 1960 até os anos 1980, e baseavam-se em três paradigmas principais: sistemas hierárquicos, sistemas de modelo de rede e sistemas de arquivo invertido.
## 6.2 Oferecendo abstração de dados e flexibilidade de aplicação com bancos de dados relacionais

Os bancos de dados relacionais foram propostos para separar o armazenamento físico dos dados de sua representação conceitual e para oferecer uma base matemática para representar e consultar os dados. O modelo também introduziu linguagens de consulta de alto nível, alternativa às interfaces de linguagem de programação, o que tornou muito mais rápida a escrita de novas consultas. Voltados inicialmente às mesmas aplicações dos sistemas antigos, davam flexibilidade para criar consultas rapidamente e reorganizar o banco conforme os requisitos mudavam, com abstração de dados e independência entre dados e programas mais desenvolvidas do que nos sistemas anteriores.

Os primeiros sistemas relacionais experimentais, do final da década de 1970, e os SGBDRs da década de 1980 eram muito lentos, pois não usavam ponteiros de armazenamento físico nem o posicionamento de registros para acessar dados relacionados. Com novas técnicas de armazenamento, o desempenho do processamento e da otimização de consultas melhorou, e os bancos relacionais se tornaram o tipo dominante para aplicações tradicionais, existindo hoje em quase todos os tipos de computadores, dos pessoais aos grandes servidores.
## 6.3 Aplicações orientadas a objeto e a necessidade de bancos de dados mais complexos

O surgimento das linguagens de programação orientadas a objeto no final da década de 1980, somado à necessidade de armazenar e compartilhar objetos complexos e estruturados, levou ao desenvolvimento dos Bancos de Dados Orientados a Objeto (BDOOs). Inicialmente vistos como concorrentes dos bancos relacionais, eles ofereciam estruturas de dados mais gerais e incorporavam paradigmas úteis da orientação a objeto, como tipos de dados abstratos, encapsulamento de operações, herança e identidade de objeto. Porém, a complexidade do modelo e a falta de um padrão inicial limitaram seu uso, e hoje eles são empregados principalmente em aplicações especializadas, como projeto de engenharia, publicação de multimídia e sistemas de manufatura, com penetração de mercado abaixo de cinco por cento. Além disso, muitos conceitos orientados a objeto foram incorporados às versões mais recentes dos SGBDs relacionais, dando origem aos sistemas de gerenciamento de banco de dados objeto-relacional (SGBDORs).
## 6.4 Intercâmbio de dados na Web para comércio eletrônico usando XML

A World Wide Web é uma grande rede de computadores interconectados, na qual os usuários criam documentos com linguagens de publicação, como o HTML, e os armazenam em servidores Web, de onde outros usuários (clientes) podem acessá-los, sendo os documentos ligados entre si por hyperlinks. Na década de 1990, o comércio eletrônico surgiu como uma aplicação importante da Web, e logo ficou claro que parte das informações das páginas de e-commerce era extraída dinamicamente de SGBDs. Por isso, foram desenvolvidas diversas técnicas para o intercâmbio de dados na Web. Hoje, a XML (linguagem de marcadores extensível) é o principal padrão para o intercâmbio de dados entre diversos tipos de bancos de dados e páginas Web, combinando conceitos dos modelos usados em sistemas de documentos com conceitos de modelagem de banco de dados.
## 6.5 Estendendo as capacidades do banco de dados para novas aplicações

O sucesso dos sistemas de banco de dados nas aplicações tradicionais encorajou desenvolvedores de outros tipos de aplicações, que antes usavam suas próprias estruturas especializadas de arquivo e dados, a tentarem utilizá-los. Entre elas estão as aplicações científicas, o armazenamento e a recuperação de imagens e de vídeos, a mineração de dados, as aplicações espaciais e as de séries temporais. Logo ficou claro que os sistemas relacionais básicos não eram muito adequados a muitas delas, porque exigiam estruturas de dados mais complexas do que a representação relacional simples, novos tipos de dados além dos numéricos e alfanuméricos, novas operações e construtores de linguagem de consulta, e novas estruturas de armazenamento e indexação para pesquisa eficiente.

Isso levou os desenvolvedores de SGBD a acrescentarem funcionalidades aos sistemas, algumas de uso geral, como a incorporação de conceitos dos bancos orientados a objeto aos relacionais, e outras de uso especial, na forma de módulos opcionais para aplicações específicas, como um módulo de séries temporais.

Além disso, muitas organizações de grande porte utilizam pacotes de aplicação que trabalham intimamente com bancos de dados de back-end, que podem ser de diferentes fornecedores e usar diferentes modelos de dados, e que mantêm os dados usados para dar suporte a transações, gerar relatórios e responder a consultas ocasionais. Entre os sistemas mais usados estão o ERP, que consolida diversas áreas funcionais da organização, e o CRM, que compreende o processamento de pedidos, o marketing e o suporte ao cliente. Essas aplicações são habilitadas para a Web, pois usuários internos e externos interagem com os bancos de back-end por meio de interfaces de portal Web.
## 6.6 Bancos de dados versus recuperação de informações

A tecnologia de banco de dados se aplica tradicionalmente a dados estruturados e formatados, comuns em aplicações de rotina do governo, do comércio e da indústria, em setores como manufatura, varejo, bancos, seguros, finanças e saúde, nos quais os dados são coletados por meio de formulários. Uma área relacionada é a Recuperação de Informação (RI), que lida com livros, manuscritos e artigos de biblioteca, cujos dados são indexados, catalogados e anotados com palavras-chave. A RI se ocupa da busca por conteúdo com base nessas palavras-chave e de problemas de processamento de documentos e de texto em forma livre, como a localização de documentos, sua classificação por relevância, a categorização automática de texto e a classificação por tópicos.

Com o advento da Web e a proliferação de bilhões de páginas HTML, muitas técnicas de RI passaram a ser aplicadas ao processamento dos dados da Web, que costumam conter imagens, texto e objetos ativos que mudam dinamicamente. A recuperação de informações na Web é, portanto, um problema novo, que exige combinar técnicas de bancos de dados e de RI de maneiras inéditas.
# 7 Quando não usar um SGBD

Apesar de suas vantagens, um SGBD pode envolver custos adicionais desnecessários em comparação ao processamento de arquivos tradicional. Esses custos vêm do alto investimento inicial em hardware, software e treinamento, da generalidade que o SGBD oferece para a definição e o processamento de dados, e do esforço extra para prover segurança, controle de concorrência, recuperação e integridade.

Por isso, pode ser mais desejável usar arquivos comuns em aplicações simples e bem definidas, para as quais não se esperam muitas mudanças, em programas com requisitos rigorosos de tempo real que as operações extras do SGBD poderiam comprometer, em sistemas embarcados com armazenamento limitado e quando não há acesso de múltiplos usuários aos dados.

Alguns setores e aplicações também optaram por não usar SGBDs de uso geral, preferindo soluções próprias e especializadas, como ocorre nas ferramentas de CAD, com software proprietário para gerenciar desenhos e objetos 3D, nos sistemas de comunicação e comutação, voltados ao acesso rápido a dados hierárquicos para o roteamento de chamadas, e nos sistemas de informações geográficas (SIG), que usam esquemas próprios de organização de dados para processar mapas, contornos, linhas e polígonos de forma eficiente.