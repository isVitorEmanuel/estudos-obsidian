# 1 Introdução

Java é **orientada a objetos** e é uma das linguagens mais usadas para desenvolvimento de sotwares corporativos, bem como para aplicativos que se comunicam pela internet.

## 1.1 Versões do Java

- **Java Standard Edition (JSE)**: A JSE possui ferramentas para construir softwares desktop e servidores. Ela, bem como todas as outras versões do Java, suportam os paradigmas orientados a objetos, procedural, genérica e funcional (adicionado na versão 8).
- **Java Enterprise Edition (JEE)**: O Java Enterprise Edition (JEE) é adequado para desenvolver aplicativos em rede distribuída e em grande escala e também aplicativos baseados na web. Anteriomente, softwares de computadores rodavam isolados (não conectados à rede). Atualmente, os aplicativos de hoje podem ser escritos para que se comuniquem entre os computadores no mundo pela internet e web.
- **Java Micro Edition (JME)**: É um subconjunto da JSE voltados para o desenvolvimento de aplicações para dispositivos embarcados, ou seja, com recursos mais limitados.

# 2 Hardware

Um computador é composto por vários dispositivos chamados hardware (por exemplo, teclado, tela, mouse, unidades de disco,
memória, unidades de DVD e unidades de processamento). Os custos da computação estão caindo drasticamente, por conta dos rápidos avanços nas tecnologias de hardware e software.

Os computadores são capazes de realizar cálculos e tomar decisões muito mais rápido que seres humanos. Tal processamento e controle de dados é feito por intermédio de *programas de computador* que orientam o que o computador devo fazer.

## 2.1 Lei de Moore

Essa **lei**, identificada na década de $60$ por Gordon Moore, diz que o poder de processamento dos computador **dobra** a cada 2 anos. Isso pode ser observado principalmente em:

- Memória;
- Armazenamento;
- Veloocidade de processamento;

## 2.2 Organização do Computador

Na tabela abaixo, temos uma visão geral de como um computador é organizado.

| Unidade Lógica                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| -------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Unidade de Entrada                     | É o canal responsável pelo recebimento de dados/informações do mundo externo para o mundo interno do computador, o que permite o processamento, tratamento, armazenamento dos dados.                                                                                                                                                                                                                                                                                                               |
| Unidade de Saída                       | É o canal responsável por entregar os dados/informações do mundo interno do computador para o mundo externo.                                                                                                                                                                                                                                                                                                                                                                                       |
| Unidade de Memória                     | É a seção de armazenamento de acesso rápido e de baixa capacidade. É responsável por armazenar as informações que foram inseridas pela unidade de entrada, tornando-as passíveis de tratamento; e também é responsável por armazenar informações até que elas possam ser entregues pela unidade de saída.<br><br>As informações nela são voláteis, ou seja, se perdem com a falta de eletricidade.                                                                                                 |
| Unidade Lógica e Aritmética (ALU)      | Executa cálculos como adição, subtração, multiplicação e divisão. Também contém os mecanismos de decisão que permitem ao computador, por exemplo, comparar dois itens da unidade de memória para determinar se são iguais ou não.<br><br>> Atualmente, ela é implementada junto com a CPU.                                                                                                                                                                                                         |
| Unidade de processamento central (CPU) | Essa seção “administrativa” coordena e supervisiona a operação das outras seções. Muitos computadores de hoje têm múltiplas CPUs e, portanto, podem realizar muitas operações simultaneamente. Um processador de múltiplos núcleos (ou multi-core) implementa o multiprocessamento em um único chip de circuito integrado.                                                                                                                                                                         |
| Unidade de armazenamento secundária    | Essa é a seção de “armazenamento” de longo prazo e de alta capacidade. Programas ou dados que<br>não são utilizados ativamente pelas outras unidades, em geral, são colocados em dispositivos de<br>armazenamento secundário (por exemplo, discos rígidos) até que sejam necessários, talvez horas, dias, meses ou até mesmo anos mais tarde. As informações nos dispositivos de armazenamento secundário são persistentes — elas são preservadas mesmo quando a energia do computador é desligada |

# 3 Hierarquia de Dados

Orgniza-se os dados pela sua complexidade. Abaixo, temos uma lista que representa isso:

1. **Bits**: Menor item de dados de um computador. Pode armazenar os valores $0$ ou $1$.
2. **Caracteres**: É o conjunto de símbolos formados pelos **digitos**, **letras** e **símbolos especiais**. Como um computador entende apenas dados binários, os caracteres são representados, por baixo dos panos, por sequências de 0 e 1. **Java** usa caracteres **unicode** que são compostos por um, dois ou quatro *byes* (8 bits, 16 bits ou 32 bits).
3. **Campos**: Assim como caracteres são compostos de bits, campos são compostos de caracteres ou bytes. Um campo é um grupo de caracteres ou bytes que transmitem um significado, como o nome de uma pessoa.
4. **Registros**: Vrios campos relacionados podem ser usados para compor um registro.
5. **Arquivos**: Um arquivo é um grupo de registros relacionados ou, de maneira mais geral, um arquivo contém dados arbitrários em formatos arbitrários.
6. **Banco de Dados**: Um banco de dados é uma coleção de dados organizados para fácil acesso e manipulação. O modelo mais popular é o banco de dados relacional, em que os dados são armazenados em tabelas simples. Uma tabela inclui registros e campos. 
7. **Big data**: É a nova tendência dos dados. É a geração de dados caracterizadas por volume, velocidade e variedade.

## 4 Linguagens de máquina, assembly e de alto nível

**LINGUAGEM DE MÁQUINA**

É a única linguagem que um computador entende. Geralmente, consitem em conjuntos de números (em última instância, reduzido a 0s e 1s) que instruem os computadores a realizaram suas operações mais básicas. As linguagens de máquina são dependentes de máquina (uma determinada linguagem de máquina pode ser utilizada apenas em um tipo de computador).

**LINGUAGEM ASSEMBLY**

A programação na linguagem de máquina era muito complexa e lenta. Por esse motivo, programados começaram a utilizar abriviações em inglês para representar as operações que se tornaram base para a linguagem **assembly**.

**LINGUAGEM DE ALTO NÍVEL**

Com o crescimento do uso dos computadores e, consequentemente, do desenvolvimento de sotware,  programdores ainda gastavam muito tempo com codificações complexas para problemas simples. Por isso, foram desenvolvidas linguagens de alto nível que retiravam essa complexidade por meio de instruções mais parecidas com o inglês cotidiano e com notações matemáticas conhecidas.

**COMPILADORE E INTERPRETADORES**

Porém, linguagens de alto nível não são entendidas pelos computadores, por isso os **compiladores** e **interpretadores** foram desenvolvidos. 

- **Compiladores**: São responsáveis por traduzir/converter um código em alto nível para uma linguagem assembly ou de máquina para que o computador possa entender.
- **Interpretadores**: Interpretadores traduzem/convertem o código em alto nível enquanto o executam, diferentemente de compiladores que primeiro convertem o código para depois executá-lo.

# 5 Introdução à tecnologia de objetos

Orientação a objetos permite a reutilização de código o que permite uma maior velocidade de codificação, melhor manutenção de código, economia de recursos e diversas outras vantagens;

## 5.1 Tudo como objeto

Tudo que existe pode ser considerado um **objeto**, ou melhor, uma classe que fabrica **objetos**. Esses objetos têm atributos (características) e métodos (comportamentos). 

Suponha que quero criar um objeto carro. A nossa classe será chamado `Carro` e ela será uma fábrica de carros. Um carro terá os seguintes atributos:

- Cor;
- Ano;
- Placa;
- Número de portas;
- Dono;
- Velocidade;

E os seguintes métodos:

- Ligar;
- Desligar;
- Abrir porta;
- Acelerar;
- Freiar;

## 5.2 Métodos e Classes

Para realizar uma tarefa em um programa é necessário um **método**. Um método organiza e armazena as declarações de uma determinada ação que o programa deve executar, ocultando essas declarações do usuário, assim como um pedal acelarador esconde toda as engrenagens e mecânicas de fazer um carro acelerar.

No Java, criamos uma unidade de programa que guarda os métodos que executam as tarefas dela.

## 5.3 Instanciação

É o ato de **construir** um objeto a partir de sua classe. Pode-se dizer que um objeto é uma **instância** de uma classe.

## 5.4 Reutilização

Pode-se utilizar uma mesma classe para criar vários objetos dela. Além disso, é possível construir classes baseadas em outras classes. Isso dá mais consistência e confiança ao código, visto que classes já existentes, geralmente, passam por extensas baterias de testes e validações; além de permitir um desenvolvimento mais eficiente.

## 5.5 Mensagens e Chamada de Método

É por meio de **chamadas** que dizemos ao método como e quando ele deve executar.

## 5.6 Atributos e variáveis de instância

Atributos, como dito, são características de um objeto. Esses atributos são espacificados nas variáveis como parte da classe do objeto.

## 5.7 Encapsulamento e ocultamento de informações

Classes e, consequentemente, seus objetos **encapsulam**, isto é, guardam seus métodos e atributos. Métodos e atributos estão intimamente relacionados e, quando um objeto se comunica com outro, é ideal que a implementação dos métodos de um não esteja visível para o outro.

## 5.8 Herança

Uma nova classe de objetos pode ser criada convenientemente por meio de herança — ela (chamada **subclasse**) começa com as características de uma classe existente (chamada superclasse), possivelmente personalizando-as e adicionando aspectos próprios.
## 5.9 Interfaces

O Java suporta **interfaces** que são coleções de métodos relacionados que, normalmente, informam "o que" devem fazer, mas não "como" fazer. Uma classe pode implementar **nenhuma ou várias** interfaces.

## 5.10 Análise e projeto orientados a objetos (OOAD)

Para criar as melhores soluções, você deve seguir um processo de análise detalhado a fim de determinar os requisitos do projeto e desenvolver um design que os atenda. Idealmente, você passaria por esse processo e revisaria cuidadosamente o projeto antes de escrever qualquer linha de código. 

Se esse processo envolve analisar e projetar o sistema de um ponto de vista orientado a objetos, ele é chamado de processo de **análise e projeto orientados a objetos** (**object-oriented analysis and design — OOAD**). Linguagens como Java são orientadas a objetos. A programação nessa linguagem, chamada programação orientada a objetos, permite-lhe implementar um projeto orientado a objetos como um sistema funcional.

## 5.11 UML (unified modeling language)

A unified modeling language (UML) é agora o esquema gráfico mais utilizado para modelagem de sistemas orientados a objetos.

# 6 Java

Sua principal contribuição foi no desenvolvimento de computadores pessoais. Um objetivo claro do Java é ser capaz de escrever programas que podem ser executados em uma grande variedade de sistemas, "*escreva uma vez, execute em qualquer lugar*".

Também é muito utilizada em aplicações web e sistemas corporativos de grande porte, aprimorar funcionalidades de servidores web, fornecer aplicativos para dispositivos voltados ao consumo popular e diversos outros propósitos.

**BIBLIOTECAS JAVA**

A maioria dos programadores Java tira proveito das ricas coleções de classes existentes e métodos nas bibliotecas de classe Java, também conhecidas como Java **APIs (application programming interfaces)**.

> Utilizar as classes e os métodos da Java API em vez de escrever suas próprias versões pode melhorar o desempenho de programa, porque eles são cuidadosamente escritos para executar de modo eficiente. Isso também diminui o tempo de desenvolvimento de programa.


# 7 Ambiente Java

> É necessário ter a **SDK (software development kit)** instalada no seu computador. Trata-se de um conjunto completo de ferramentas, bibliotecas de código, documentação e compiladores que permite aos desenvolvedores criar aplicativos para uma plataforma, sistema operacional ou serviço específico.

**CRIANDO UM PROGRAMA**

Arquivo de código fonte em Java são salvos na memória de armzenamento secundário com a extensão `.java`.

<div align="center">
  <img src="Pasted image 20261020142514.png" width="75%">
  <br>
  <em>Figura 1: Fase de edição no ambiente Java.</em>
</div>

**COMPILANDO**

Para compilar um programa em Java, use o comando `javac <file_name.java>`. Se compilar, o compilador gerará um arquivo **bytecode** com a extensão `.class`.  

Após isso, o **bytecode** pode ser executado pela **JVM (Java Virtual Machine)** que é um aplicativo de software que simula um computador, mas oculta o sistema operacional e o hardware subjacentes dos programas que interagem com ela. Assim, ela é responsável por executar os **bytecodes** independentemente da plataforma.

A JVM é invocada pelo comando `java <file_name.class>`.

<div align="center">
  <img src="Pasted image 20261020143557.png" width="75%">
  <br>
  <em>Figura 2: Fase de compilação no ambiente Java.</em>
</div>

**CARREGANDO UM PROGRAMA NA MEMÓRIA**

É a fase que a JVM carrega os **bytecodes** necessários do disco para memória principal por meio do *classloader*.

**VERIFICAÇÃO DE BYTECODE**

Enquanto as classes são carregadas, o verificador de **bytecode** faz uma verificação para assegurar que eles são válidos e não violam restrições de segurança do Java.

<div align="center">
  <img src="Pasted image 20261020145427.png" width="75%">
  <br>
  <em>Figura 3: Fase de verificação no ambiente Java.</em>
</div>

**EXECUÇÃO**

Nesta fase, a **JVM** executa o byecode. Anteriormente, a execução era feita iterativamente, porém algumas arquiteturas permite a execução em paralelo.

Além disso, a **JVM** utiliza a interpretação com a **compilação just-in-time (JIT)**. Com isso, à medida que os bytecodes são interpretados, é feita uma análise buscando os **hotspots** (partes mais executadas do código). Para estas partes, um compilador JIT traduz o bytecode para a linguagem de máquina diretamente, permitindo uma execução mais rápida dessas partes.

<div align="center">
  <img src="Pasted image 20261020145427.png" width="75%">
  <br>
  <em>Figura 3: Fase de execução no ambiente Java.</em>
</div>












