As operações realizadas em um computador são baseadas no armazenamento e processamento de dados binários ($0$s ou/e $1$s) que é feito através de circuitos capazes de operar esses dados.

---
# 1. Álgebra Booleana

A **álgebra booleana** é a base dos circuitos digitais dos computadores, nome dado em homenagem ao matemático inglês *George Boole*. A álgebra mostra ser uma ótima ferramenta nas áreas:

- **Análise:** é um modo econômico de descrever a função do circuito digital;
- **Projeto:** dada uma função desejada, a álgebra booleana pode ser aplicada a desenvolver uma implementação simplificada dessa função;

Nela, utilizamos variáveis que podem receber os valores $0$ ou $1$ (FALSO e VERDADEIRO, respectivamente). As operações lógicas são:

| OPERAÇÃO    | ESCRITA            | MATEMÁTICA  | COMPORTAMENTO                                                               |
| ----------- | ------------------ | ----------- | --------------------------------------------------------------------------- |
| **AND**     | $A \text{ AND } B$ | $A \cdot B$ | Produz o valor verdadeiro ($1$), se os dois lados forem verdadeiro.         |
| **OR** <br> | $A \text{ OR } B$  | $A + B$     | Produz o valor verdadeiro ($1$), se pelo menos um dos lados for verdadeiro. |
| **NOT**     | $\text{NOT }A$     | $\bar{A}$   | Inverte o valor da variável.                                                |

> OBS: $A \cdot B = AB$.

Como exemplo, tome $D = A + (\bar{B} \cdot C)$. Se $D = 1$, $A = 1$ ou $B = 0$ e $C = 1$. Caso contrário, $D = 0$. Além disso, a ordem de precedência é:

1. Parênteses;
2. $NOT$;
3. $AND$;
4. $OR$;

Existem outras operações derivadas, são elas:

| OPERAÇÃO      | ESCRITA             | MATEMÁTICA             | COMPORTAMENTO                                                                |
| ------------- | ------------------- | ---------------------- | ---------------------------------------------------------------------------- |
| **XOR**       | $A \text{ XOR } B$  | $A \oplus B$           | Produz o valor verdadeiro ($1$), se um e apenas um dos lados for verdadeiro. |
| **NAND** <br> | $A \text{ NAND } B$ | $\overline{A \cdot B}$ | É o complemento do **AND**.                                                  |
| **NOR**       | $A \text{ NOR } B$  | $\overline{A + B}$     | É o complemento do **OR**.                                                   |

Abaixo, temos algumas tabelas resumo da tabela verdade, operações estendidas e identidades básica da álgebra booleana.

<div align="center">
  <img src="Pasted image 20261018224936.png" width="75%">
  <br>
  <em>Figura 1: Tabela verdade das operações lógicas.</em>
</div>

<div align="center">
  <img src="Pasted image 20261018225718.png" width="75%">
  <br>
  <em>Figura 2: Operações estendidas para mais de uma variável.</em>
</div>

<div align="center">
  <img src="Pasted image 20261018225903.png" width="75%">
  <br>
  <em>Figura 3: Identidades básicas.</em>
</div>
---

# 2. Portas Lógicas

São os blocos fundamentais da construção de um **circuitos lógicos**, pois implementam as funções lógicas através da combinação e interconexão de portas lógicas. *Por definição*, *uma **porta lógica** é um circuito que produz um sinal de saída aplicando uma operação da álgebra booleana em seus sinais de entrada*. Abaixo, vemos a simbologia dessas portas lógicas, notação matemática e a tabela verdade.

<div align="center">
  <img src="Pasted image 20261018230907.png" width="50%">
  <br>
  <em>Figura 4: Portas lógicas e suas notações.</em>
</div>

É importante notar que todas as portas, com exceção da **NOT** pode ser implementada com mais de $2$ portas também. Quando um sinal de entrada muda, o sinal correto da saída aparece que quase instantaneamente, atrasado apenas pelo tempo de *propagação das portas lógicas*. Além disso, definimos que **forçar** um sinal é mudar seu estado logicamente falso para um estado logicamente verdadeiro.

Em geral, nem todos os tipos de portas são usadas, pois o projeto e fabricação acaba se tornando mais simples com uma menor diversidade de portas. Assim, é importante identificar funcionalmente conjuntos completos de portas lógicas. São eles:

- **AND, OR, NOT**;
- **AND, NOT**;
- **OR, NOT**;
- **NAND**;
- **NOR**;

Para as portas **AND** e **NOT** formarem um conjunto funcionalmente completo, deve haver uma forma de sintetizar a operação **OR** a partir das operações **AND** e **NOT**. Isso pode ser feito ao aplicar o teorema de DeMorgan:

$$
A + B = \overline{\bar{A} \cdot \bar{B}} \\
A \text{ OR } B = \text{NOT }((\text{NOT A}) \text{ AND } (\text{NOT }B))
$$

Abaixo, temos as implementações das portas **AND, OR** e **NOT** através das portas **NAND** e **NOR**:

<div align="center">
  <img src="Pasted image 20261018232913.png" width="30%">
  <br>
  <em>Figura 5: Uso da porta NAND.</em>
</div>

<div align="center">
  <img src="Pasted image 20261018234333.png" width="30%">
  <br>
  <em>Figura 6: Uso da porta NOR.</em>
</div>
