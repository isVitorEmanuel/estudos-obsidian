A engenharia de software é essencial para o funcionamento do governo, da sociedade e das empresas e instituições nacionais e internacionais. O mundo moderno não funciona sem software. Os sistemas de software são abstratos e intangíveis, por isso não são regidos por leis absolutas, como a física. No entanto, devido à ausência de leis, os sistemas de software podem rapidamente se tornar bastante complexos, dificeis de entender e caros de modificar.

Exitem inúmeros tipos de softwares, por isso não há leis universais da engenharia. Além disso, existem muitos relatos de falhas de software, causadas por:

- **Complexidade crescente dos sistemas**: a medida que as novas técnicas de engenharia de software nos ajudam a construir sistemas maiores e mais complexos. as demandas mudam.
- **Não utilização de metodos de engenharia de software**;

## 1 Desenvolvimento de Software Profissional

Um software profissional é caracterizado pelo desenvolvimento por times e não por indivíduos; utilização por diversas pessoas e não somente pelo desenvolvedor; e é mantido e alterado ao longo de sua vida. A engenharia de software destina-se a apoirar o desenvovimento de software profissional.

|Pergunta|Resposta|
|---|---|
|O que é software?|Programas de computador e documentação associada. Os produtos de software podem ser desenvolvidos para um determinado cliente ou para um mercado genérico.|
|Quais são os atributos do bom software?|O bom software deve proporcionar a funcionalidade e o desempenho necessários e deve ser manutenível, usável e ter dependabilidade (_dependability_).|
|O que é engenharia de software?|A engenharia de software é uma disciplina de engenharia que se preocupa com os aspectos da produção de software, desde sua concepção inicial até sua operação e manutenção.|
|Quais são as atividades fundamentais da engenharia de software?|Especificação, desenvolvimento, validação e evolução do software.|
|Qual é a diferença entre engenharia de software e ciência da computação?|A ciência da computação se concentra na teoria e nos fundamentos. A engenharia de software se preocupa com as questões práticas de desenvolver e entregar software útil.|
|Qual é a diferença entre engenharia de software e engenharia de sistemas?|A engenharia de sistemas se preocupa com todos os aspectos do desenvolvimento de sistemas computacionais, incluindo hardware, software e engenharia de processos. A engenharia de software faz parte desse processo mais geral.|
|Quais são os principais desafios enfrentados pela engenharia de software?|Lidar com a crescente diversidade, com as demandas por menores prazos de entrega e desenvolver software confiável.|
|Quais são os custos da engenharia de software?|Aproximadamente 60% dos custos de software são relativos ao desenvolvimento e 40%, aos testes. Quanto ao software personalizado, os custos de evolução frequentemente ultrapassam os de desenvolvimento.|
|Quais são os melhores métodos e técnicas de engenharia de software?|Ainda que todos os projetos de software devam ser gerenciados e desenvolvidos profissionalmente, técnicas diferentes são adequadas para tipos diferentes de sistemas. Por exemplo, jogos devem ser sempre desenvolvidos usando uma série de protótipos, enquanto sistemas de controle críticos em segurança requerem o desenvolvimento de uma especificação completa e analisável. Não há métodos ou técnicas que sejam bons para todos os casos.|
|Quais diferenças a internet trouxe para a engenharia de software?|A internet não só levou ao desenvolvimento de sistemas massivos, largamente distribuídos, baseados em serviços, como também deu base para a criação de uma indústria de aplicativos (ou "_apps_") para dispositivos móveis que mudou a economia de software.|

Um bom software vai além de um programa de computador. É o programa de computador, a documentação, arquivos de configuração e todos os elementos necessários. Os engenheiros de software se preocupam em desenvolver produtos de software, ou seja, software que possa ser vendido para clientes. Existem dois tipos de produto de software:

- **Produtos genéricos:** produtos genéricos são sistemas **stand-alone** produzidos por uma organização de desenvolvimento de software e vendidos no mercado para qualquer cliente que queira comprá-los. Exemplos incluem aplicativos para dispositivos móveis e softwares para PCs, como bancos de dados, processadores de texto, pacotes de desenho e ferramentas de gerenciamento de projeto. Esse tipo de software também abrange aplicações “verticais”, projetadas para um mercado específico, como sistemas de informação de bibliotecas, sistemas contábeis ou sistemas para manter registros odontológicos.
- **Software personalizado (ou feito sob medida)**: são sistemas encomendados e desenvolvidos para um determinado cliente, sendo projetados e implementados por uma empresa de software especialmente para ele. Exemplos incluem sistemas de controle para dispositivos eletrônicos, sistemas escritos para apoiar processos de negócios específicos e sistemas de controle de tráfego aéreo

No entanto, a distinção entre esses tipos de produto está ficando cada vez mais confusa. Cada vez mais sistemas são criados com base em um produto genérico, que depois é adaptado para atender às necessidades de um determinado cliente. Os sistemas **ERP** (Enterprise Resource Planning, em português, planejamento de recursos empresariais), como os da SAP e da Oracle, são os melhores exemplos dessa abordagem: um sistema grande e complexo é adaptado para uma empresa, incorporando informações sobre as regras e os processos de negócio, os relatórios necessários e assim por diante.

A qualidade não tem a ver apenas com o que o software faz. Preferencialmente, ela deve incluir o comportamento do software enquanto ele está em execução, a estrutura e a organização dos programas do sistema e a documentação associada. Isso se reflete nos atributos da qualidade - também chamados de não funcionais - do software. Podemos generalizar as características da seguinte forma:

| Característica do produto                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Aceitabilidade                                         | O software deve ser aceitável para o tipo de usuário para o qual é projetado. Isso significa que ele deve ser inteligível, útil e compatível com os outros sistemas utilizados pelos usuários.                                                                                                                                                                           |
| Dependabilidade e segurança da informação (_security_) | A dependabilidade do software inclui uma gama de características, incluindo confiabilidade, segurança da informação (_security_) e segurança (_safety_). O software com dependabilidade não deve causar danos físicos ou econômicos em caso de falha do sistema. Ele também deve ser protegido para que usuários maliciosos não consigam acessar ou danificar o sistema. |
| Eficiência                                             | O software não deve desperdiçar recursos do sistema, como a memória e os ciclos de processador. Portanto, a eficiência inclui responsividade, tempo de processamento, utilização de recursos etc.                                                                                                                                                                        |
| Manutenibilidade                                       | O software deve ser escrito de tal modo que possa evoluir e satisfazer as necessidades mutáveis dos clientes. Este é um atributo crítico, pois a modificação do software é um requisito inevitável de um ambiente empresarial mutável.                                                                                                                                   |
## 1.1 Engenharia de Software

A engenharia de software está relacionada com **todos** os aspectos da **produção de um software**. Aqui, há dois conceitos importantíssimos:

- **Engenharia de Software:** engenharia de software é uma disciplina de engenharia, o que significa que seu foco é fazer as coisas funcionarem. Os engenheiros aplicam teorias, métodos e ferramentas de forma seletiva, onde forem apropriados, e sempre buscam soluções para os problemas dentro do **prazo** e do **custo**, mesmo quando não existem teorias ou métodos aplicáveis. Eles também reconhecem que precisam trabalhar dentro de limites organizacionais e financeiros, buscando soluções que caibam nesses limites.
- **Todos os aspectos da criação de software**: ela não se preocupa apenas com os aspectos técnicos, mas inclui as atividades de gerenciamento, desenvolvimento de ferramentas, métodos e teorias que apoiam a criação do software.

> Os engenheiros de software devem escolher a abordagem para o desenvolvimento observando as caracterísitcas e o contexto do software, buscando aquela mais adequada. Por exemplo: geralmente, os engenheiros de software adotam urna abordagem sistemática e organizada para o seu trabalho, já que muitas vezes essa é a maneira mais eficaz de produzir software de alta qualidade; porém, urna abordagem mais criativa e menos formal de desenvolvimento pode ser a mais adequada para alguns tipos de software.

A engenharia de software é importante por duas razões principais:

- Cada vez mais os individuas e a sociedade dependem de sistemas de softwares avançados.
- Geralmente é mais barato. no longo prazo. usar métodos e técnicas de engenharia de software para sistemas de software profissionais em vez de apenas escrever programas como urn projeto de programação pessoal.

De acordo com **Pressman**, a engenharia de software é construída em camadas:

<div align="center">
  <img src="Pasted image 20261022144115.png" width="55%">
  <br>
  <em>Figura 1: Camadas da Engenharia de Software, de acordo com Pressman.</em>
</div>

### 1.1.1 Processos de Software

A **abordagem sistemática** é muitas vezes chamadas de **processo de software** que é uma *sequência de atividades que levam à produção de um software*. São quatro as atividades comuns a todos os processos:

- **Especificação do Software**: etapa em que clientes e engenheiros definem o software que deve ser produzido e as restrições impostas à sua operação;
- **Desenvolvimento de software**: etapa em que o software é projetado e programado;
- **Validação de software**: etapa em que o programa é analisado para garantir que seja aquilo de que o cliente precisa; e
- **Evolução do software**: etapa de modificação para refletir a mudança de requisitos tanto do cliente quanto do mercado;

<div align="center">
  <img src="Pasted image 20261021182812.png" width="55%">
  <br>
  <em>Figura 2: Atividades principais de acordo com Sommerville.</em>
</div>

Cabe citar também, de acordo com Pressman quais são as atividades gerais e de apoio:

- Práticas Gerais:
	- **Comunicação**; 
	- **Planejamento**;
	- **Modelagem**;
	- **Construção**;
	- **Entrega**;

<div align="center">
  <img src="Pasted image 20261021185731.png" width="55%">
  <br>
  <em>Figura 3: Atividades principais de acordo com Pressman.</em>
</div>

- Práticas de Apoio:
	- **Controle e Acompanhamento do Projeto**;
	- **Administração de Riscos**;
	- **Garantia de Qualidade**;
	- **Revisão Técnicas**;
	- **Medição**;
	- **Gerenciamento de Configuração de Software**;
	- **Gerenciamento da Configuração de Software**;
	- **Gerenciamento da Capacidade de Reutilização**;
	- **Preparo e Produção de Artefatos de Software**;

<div align="center">
  <img src="Pasted image 20261021190256.png" width="55%">
  <br>
  <em>Figura 4: Práticas de apoio, de acordo com Pressman.</em>
</div>

É importante notar que diferentes tipos de sistemas precisam de diferentes processos de desenvolvimento.

## 1.2 Engenharia de Software e seus Relacionamentos

A engenharia de software está relacionada tanto à ciência da computação quanto à engenharia de sistemas. Existem muitos tipos diferentes de software, porém não existem métodos ou técnicas universais de engenharia de software que possam ser utilizados. No entanto. existem quatro questões relacionadas que afetam muitos tipos de software diferentes:

- **Heterogeneidade**: Cada vez mais são necessários sistemas que atuem de forma distribuida em redes e que incluam diferentes tipos de computadores e dispositivos móveis.
- **Mudanças nos negócios e na sociedade**: As empresas e a sociedade precisam ser capazes de mudar seu software existente e de desenvolver rapidamente um novo, devido alterações no mundo. E necessário que as técnicas de desenvolvimento evoluam de modo que o tempo necessário para que o software entregue valor aos seus clientes seja reduzido.
- **Segurança da informação (security) e confiança (trust)**: Pelo fato de o software estar entranhado em todos os aspectos de nossas vidas, é essencial que possamos confiar nele. Precisamos ter certeza de que usuários maliciosos não consigam atacar com sucesso o nosso software e que a as informações estejam protegidas.
- **Escala**: O software tem de ser desenvolvido considerando diferentes escalas, desde pequenos sistemas embarcados em dispositivos móveis ou dispositivos vestíveis (também chamados de wearables) até sistemas baseados na nuvem e distribuídos pela internet que atendam a uma comunidade global.
## 1.3 Diversidade da Engenharia de Software

Já que existem diversos métodos para se implementar um software, a maneira mais eficiente de identificar qual usar é o tipo de aplicação que está sendo desenvolvida. Alguns tipos de aplicações são:

- **Aplicações stand-atone**: São sistemas de aplicação executados em um computador pessoal ou aplicativos que rodam em dispositivos móveis, podendo não necessitar de conexão com a rede.
- **Aplicações interativas baseadas em transações**: São aplicações executadas em um computador remoto e que são acessadas por usuários a partir de seus próprios computadores, smartphones ou tablets.
- **Sistemas de controle embarcados**: São sistemas de controle de software que controlam e gerenciam dispositivos de hardware.
- **Sistemas de processamento em lotes (batch)**: São sistemas de negócio concebidos para processar dados em grandes lotes.
- **Sistemas de entretenimento**: São destinados para uso pessoal, para entreter o usuário.
- **Sistemas para modelagem e simulação**: São desenvolvidos por cientistas e engenheiros para modelar processos fisicos ou situações que incluem muitos objetos diferentes e que interagem.
- **Sistemas de coleta de dados e análise**: São aqueles que fazem a sua coleta no ambiente e enviam esses dados para outros sistemas. para processamento.
- **Sistemas de sistemas**: São utilizados em empresas e outras grandes organizações e são compostos de uma série de outros sistemas de software.

> Obviamente, a fronteira entre esses tipos é tênue.

Mas, independentemente do tipo de software, os seguintes fundamentos da engenharia de software se aplicam:

- Eles devem ser desenvolvidos com o uso de um processo gerenciado e compreendido.
- Dependabilidade e desempenho são importantes para todos os tipos de sistema. O software deve se comportar conforme o esperado. sem falhas, e deve estar disponível para uso quando for necessário.
- É importante compreender e controlar a especificação e os requisitos do software (o que o software deve fazer).
- Os recursos existentes devem ser usados de modo eficaz.

## 1.4 Engenharia de Software para Internet

Com a evolução da web, uso de navegadores e evolução de recursos foi percebido que os sistemas web poderiam ser desenvolvidos e que. no lugar de uma interface com o usuário específica, eles passariam a ser acessados por meio de um navegador. Isso levou ao desenvolvimento de uma ampla gama de novos produtos de sistema que ofereciam serviços inovadores acessados pela internet.

Assim, ao invés de instalar os softwares diretamente nos computadores dos clientes, os softwares começaram a ser implantados no em servidores web, barateando o desenvolvimento e manutenção de softwares. Isso, permitiu o surgimento de **software as a sevice - SaaS**, onde softwares são acessados pela nuvem e não em servidores locais.

Essa mudança na organização de software teve um efeito importante na engenharia de software para os sistemas web:

- O reúso de software se tornou a abordagem dominante para construir sistemas web.
- De maneira geral. hoje reconhece-se que é impraticável especificar todos os requisitos desses sistemas antecipadamente.
- O software pode ser implementado usando engenharia de software orientada a serviços. na qual os componentes do software são serviços da web stand-alone.
- As tecnologias de desenvolvimento de interfaces. como AJAX e HTMLS, surgiram para dar suporte á criação de interfaces dinâmicas dentro de um navegador web.

## 1.5 Ética da Engenharia de Software

Assim como outras disciplinas de engenharia. a engenharia de software é conduzida dentro de um arcabouço social e legal que limita a liberdade das pessoas que trabalham nesse setor. Um engenheiro de software deve aceitar que o seu trabalho envolve responsabilidades mais amplas do que a simples aplicação de habilidades técnicas.

Além das responsabilidades dadas por lei, existem outras responsabilidades:

- **Confidencialidade**: A confidencialidade dos seus empregadores ou clientes deve ser respeitada . independentemente de um acordo ter sido assinado ou não.
- **Competência**: Não se deve apresentar um nível de competência que não seja verdadeiro. Trabalhos que estejam fora da sua competência não devem ser aceitos.
- **Direitos de propriedade intefectual**: Deve-se estar a par das leis locais que regem o uso da propriedade intelectual, como patentes e direitos autorais.
- **Mau uso do computador** Não se deve aproveitar habilidades técnicas para usar indevidamente os computadores de outras pessoas.

As sociedades e instituições profissionais têm um papel importante no estabelecimento dos padrões éticos. Organizações como a **ACM** (Association for Computing Machinery), o **IEEE** (institute of Efectricaf and Efectronic Engineers) e a **British Computer Society** publicam um código de conduta profissional ou código de ética, e seus membros se compromentem a seguir.

## 1.6 A prática da Engenharia de Software

### 1.6.1 A essência da prática

A essência da prática é caracterizada por:

1. **Compreender o problema**;
2. **Planeje a solução**;
3. **Execute/leve adiante o plano**;
4. **Examine o resultado**;

### 1.6.2 Princípios Gerais

Um princípio nada mais é que uma importante afirmação, uma lei ou um pressuposto.

Independentemente do seu nível de enfoque, os princípios ajudam a estabelecer um modo de pensar para a prática segura da engenharia de software. São eles:

1. **A razão de existir**: Um software exite para gerar valor aos seus usuários.
2. **KISS (Keep It Simple, Stupid!, ou seja: Faça de forma simples, tapado!)**: Todo projeto deve ser o mais simples possível, mas não tão simples assim. Esse princípio contribui para um sistema mais fácil de compreender e manter. Issonão significa que características, até mesmo as internas, devam ser descartadas em nome da simplicidade.
3. **Mantenha a Visão:** Uma visão clara é essencial para o sucesso. Sem ela, um projeto se torna ambíguo. Sem uma integridade conceitual, corre-se o risco de transformar o projeto numa colcha de retalhos de projetos incompatíveis, unidos por parafusos inadequados.
4. **O que um produz, os outros consomem**: De uma maneira ou de outra, alguém dependerá da capacidade de entender seu sistema. Portanto, sempre especifique, projete e implemente ciente de que alguém mais terá de entender o que você está fazendo. Especifique tendo em vista os usuários; projete, tendo em mente os implementadores; e codifique considerando aqueles que terão de manter e estender o sistema. 
5. **Esteja aberto para o futuro**: Um sistema com tempo de vida mais longo tem mais valor. Sempre projete um softtware para que ele dure o máximo possível. Logo, jamais faça projetos limitados, sempre pergunte “e se” e prepare-se para todas as possíveis respostas, criando sistemas que resolvam o problema geral, não apenas aquele específico. Isso muito provavelmente conduziria à reutilização de um sistema inteiro.
6. **Planeje com antecedência, visando a reutilização**: A reutilização economiza tempo e esforço; alcançar um alto grau de reúso é indiscutivelmente a meta mais difícil de ser atingida ao se desenvolver um sistema de software.
7. **Pense**: Pensar bem e de forma clara antes de agir quase sempre produz melhores resultados.


  