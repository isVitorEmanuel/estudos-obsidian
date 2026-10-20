# 1. Chamando o Interpretador Python

Com o Python instalado, basta abrir um terminar e executar o código `python`:

<div align="center">
  <img src="Pasted image 20261019194118.png" width="75%">
  <br>
  <em>Figura 1: Saída da chamada do interpretador.</em>
</div>

É possível sair do *shell* executando o comando `quint()`. O interpretador trabalha de forma semelhante a uma shell de Unix: quando chamado com a saída padrão conectada a um console de terminal, ele lê e executa comandos interativamente; quando chamado com um nome de arquivo como argumento, ou com redirecionamento da entrada padrão para ler um arquivo, o interpretador lê e executa o _script_ contido no arquivo.

# 2. O interpretador e seu ambiente

Por padrão, os arquivo de código fonte Python são codificados em UTF-8, o que permite o uso de caracteres de diversos idiomas. O editor deve reconhecer que o arquivo é UTF-8. Pode-se utilizar uma codificação diferente adicionando um comentário na primeira linha do arquivo.

```python
# -*- coding: enconding -*-
```

Como exemplo:

```python
# -*- coding: cp1252 -*-
```

Uma exceção é quando o código fonte inicia com uma linha [UNIX “shebang”](https://docs.python.org/pt-br/3.15/tutorial/appendix.html#tut-scripts). Como no exemplo abaixo:

```python
#!/usr/bin/env python3
# -*- coding: cp1252 -*-
```
