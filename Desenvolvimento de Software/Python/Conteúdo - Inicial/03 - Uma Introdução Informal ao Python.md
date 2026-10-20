Um comentário em Python é indicado por `#` e se estende até o final da linha e pode aparecer em qualquer lugar da linha, mas não dentro de uma *string* literal. Alguns exemplos:

```python
# este é o primeiro comentário
spam = 1  # e este é o segundo comentário
          # ... e agora um terceiro!
texto = "# Este não é um comentário por estar entre aspas."
```

# 1. Usando Python como calculadora

## 1.1 Números

A sintaxe das operações é a comum das linguagens, bem como a precedência, mas existem alguma peculiaridades. Tome os exemplos abaixo:

```python
>>> 2 + 2   # Soma
4
>>> 2 - 2   # Subtração
0
>>> 2 * 2   # Multiplicação
4
>>> 5 / 2   # Divisão
2.5
>>> 5 // 2  # Parte inteira da divisão
2
>>> 5 % 2   # Resto da divisão
1
>>> 5 ** 2  # Potenciação
25
```

É importante notar: 

- Número inteiros são do tipo `int`, já os números com ponto flutuante são do tipo `float`. 
- A divisão `/` sempre retorna um `float`. 
- O sinal de igual `=` é utilizado como sinal de atribuição.
- Ao tentar usar uma variável não definida, um erro será gerado.

Além dos tipos `int` e `float`, o Python oferece suporte ao tipos `Decimal`, `Fraction` e a números complexos, representados por `j` ou `J`.

## 1.2 Textos

Python pode manipular textos, representados pelo tipo `str`. Podendo ser colocados entre aspas simples ou duplas.

```python
'spam eggs'  # aspas simples
"Coelho de Paris, eu te projeto :)! Viva!"  # aspas duplas
'1975'  # dígitos e numerais envoltos em aspas também são strings
```

Algumas observações interessantes:

- Para colocar aspas dentro de aspas iguais, deve-se utilizar um caractere de escape, no caso, `\`.
- No *shell*, a saída das strings diretamente imprimem as aspas e os caracteres de escape e especiais. Isso não ocorre usando o `print()`.
- Caso não queira que os caracteres especiais sejam interpretados, basta utilizar as strings brutas (*raw*, em inglês). Para isso, insira um `r` antes da primeira aspas, como no código abaixo:
	- É importante notar que não pode existir um número ímpar de caracteres `\`.

```python
>>> print('C:\this\name')  # aqui \t significa tabulação, \n significa nova linha
C:      his
ame
>>> print(r'C:\this\name')  # note o r antes da aspa
C:\this\name
```

- Strings literais são utilizadas para abranger várias linhas. Usa-se aspas triplas `"""..."""`.

```python
print("""\
Uso: coisinha [OPÇÕES]
     -h                        Exibe esta mensagem de uso
     -H hostname               Hostname para se conectar
""")
```

### 1.2.1 Operações com Strings

**CONCATENAÇÃO E REPETIÇÃO:**

Strings podem ser concatenadas com `+` ou repetidas com `*`. Como no exemplo abaixo:

```python
# 3 vezes 'un', seguido por 'ium'
>>> 3 * 'un' + 'ium'
unununium
```

> Duas strings literais podem ser concatenadas diretamente. 

**INDEXAÇÃO**

Strings podem ser indexadas para retornar o caractere de uma posição específica.

```python
palavra = 'Python'

# Começando pela esquerda
palavra[0]  # P - caractere na posição 0
palavra[5]  # n - caractere na posição 5

# Começando pela direita.
palavra[-1]  # n - último caractere
palavra[-2]  # o - penúltimo caractere
palavra[-6]  # P - primeiro caractere
```

> Como $+0 = -0$, índices negativos começam do `-1`.

A tentativa de acessar um índice fora do *range* da string resulta em erro.

**FATIAMENTO/SLICING**

O fatiamento permite a obtença de uma substring.

```python
palavra[0:2]  # Py - caracteres da posição 0 (incluída) até 2 (excluída)
palavra[2:5]  # tho - caracteres da posição 2 (incluída) até 5 (excluída)
palavra[:2]   # Py - caracteres do início até a posição 2 (excluída)
palavra[4:]   # on - caracteres da posição 4 (incluída) até o fim
palavra[-2:]  # on - caracteres da penúltima (incluída) até o fim
```

Note que `s[:i] + s[i:] = s`. Para uma melhor memorização uma maneira de lembrar como fatias funcionam é pensar que os índices indicam posições _entre_ caracteres:

```
+---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
 0   1   2   3   4   5   6
-6  -5  -4  -3  -2  -1
```

A primeira fileira de números indica a posição dos índices 0…6 na string; a segunda fileira indica a posição dos respectivos índices negativos.

Os índices de fatiamento fora do alcance são tratados graciosamente (N.d.T: o termo original “gracefully”) quando usados para fatiamento. Um índice maior que o comprimento é trocado pelo comprimento, um limite superior menor que o limite inferior produz uma string vazia. Isso garante uma maior **robustez**.

```python
palavra[4:42] # "on"
palavra[42:]  # ""
```

**OBSERVAÇÕES**

- Strings em Python não podem ser alteradas! Portanto, atribuir a uma posição indexada na sequência resulta em um erro. É necessário criar uma nova.
- A função `len()` retorna o comprimento da String.

## 1.3 Listas

`list` é uma estrutura de dados composta de Python muito versátil. Pode ser escrita como uma lista de valores separados por vírgulas envoltos em colchetes. Os valores **não precisam ser do mesmo tipo**.

```python
>>> quadrados = [1, 4, 9, 16, 25]
>>> quadrados
[1, 4, 9, 16, 25]
```

### 1.3.1 Operações

**INDEXAÇÃO**

A indexação retorna um item da lista.

```python
>>> quadrados[0]  # indexação retorna o item
1
>>> quadrados[-1]
25
```

**FATIAMENTO**

O fatiamento retorna uma sublista.

```python
>>> quadrados[-3:]  # fatiamento retorna uma nova lista
[9, 16, 25]
```

> OBS: As operações de fatiamento retornam uma nova lista.

**CONCATENAÇÃO**

É a ação de juntar duas listas ou mais. 

```python
>>> quadrados + [36, 49, 64, 81, 100]
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

**OBSERVAÇÕES**

- As listas são mutáveis, ou seja, é possível alterar elementos individualmente.
- Pode-se adicionar itens aos finais da lista com o método `list_name.append()`.
- A atribuição de lista é por referência ao objeto e não por cópia. Tome o exemplo abaixo:

```python
>>> rgb = ["Vermelho", "Verde", "Azul"]
>>> rgba = rgb
>>> id(rgb) == id(rgba)  # elas referenciam o mesmo objeto
True
>>> rgba.append("Alf")
>>> rgb
["Vermelho", "Verde", "Azul", "Alf"]
```

- Também é possível aplicar atribuições em fatiamentos.

```python
>>> rgba
['Red', 'Green', 'Blue', 'Alpha']
>>> rgba[1:3] = ["G", "B"]
>>> rgba
['Red', 'G', 'B', 'Alpha']
```

- O `len()` também pode ser usado para recuperar o tamanho da lista.
- É possível aninhar listas.