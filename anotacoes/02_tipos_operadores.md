# Tipos de operadores

### Aritméticos
`+`, `-`, `*`, `/`, `//`, `%`, `**`

### Comparação
* `==` : igual a
* `!=` : diferente de
* `>`  : maior que
* `<`  : menor que
* `>=` : maior ou igual a
* `<=` : menor ou igual a

### Lógicos
* `and` : retorna `True` se ambos os operandos forem `True`
* `or`  : retorna `True` se pelo menos um dos operandos for `True`
* `not` : inverte o valor lógico do operando

### Atribuição
* `=`   : atribuição simples
* `+=`  : adição e atribuição
* `-=`  : subtração e atribuição
* `*=`  : multiplicação e atribuição
* `/=`  : divisão e atribuição
* `//=` : divisão inteira e atribuição
* `%=`  : módulo e atribuição
* `**=` : exponenciação e atribuição

### Bitwise
* `&`  : AND bit a bit
* `|`  : OR bit a bit
* `^`  : XOR bit a bit
* `~`  : NOT bit a bit
* `<<` : deslocamento à esquerda
* `>>` : deslocamento à direita

### Associação/Membros
* `in`: verifica se um valor está presente em uma sequência
* `not in`: verifica se um valor não está presente em uma sequência

### Identidade
* `is`      : verifica se dois objetos são o mesmo objeto na memória
* `is not` : verifica se dois objetos não são o mesmo objeto na memória

### Precedência de operadores

1.  Parênteses `()`
2.  Exponenciação `**`
3.  Multiplicação, Divisão, Divisão Inteira, Módulo `*`, `/`, `//`, `%`
4.  Adição, Subtração `+`, `-`
5.  Operadores de Comparação `==`, `!=`, `>`, `<`, `>=`, `<=`
6.  Operadores Lógicos `not`, `and`, `or`
7.  Operadores de Atribuição `=`, `+=`, `-=`, `*=`, `/=`, `//=`, `%=`, `**=`
8.  Operadores Bitwise `&`, `|`, `^`, `~`, `<<`, `>>`
9.  Operadores de Membros (Associação) `in`, `not in`
10. Operadores de Identidade `is`, `is not`

### Notas sobre operadores

* `%`: operador módulo retorna o resto da divisão inteira
* `**`: operador de exponenciação
* `//`: operador de divisão inteira (trunca o valor)
