# Tipos em Python

### Os tipos built-in são:

* **Números:** `int`, `float`, `complex`
* **Sequências:** `list`, `tuple`, `range`
* **Texto:** `str`
* **Conjuntos:** `set`, `frozenset`
* **Mapeamentos:** `dict`
* **Booleanos:** `bool`
* **Binários:** `bytes`, `bytearray`, `memoryview`
* **NoneType:** `None`

### Classes dos tipos

* `int()`
* `float()`
* `complex()`
* `list()`
* `tuple()`
* `range()`
* `str()`
* `set()`
* `frozenset()`
* `dict()`
* `bool()`
* `bytes()`
* `bytearray()`
* `memoryview()`

# Modo interativo

Para entrar no modo interativo:
```bash
python -i <name>.py
```
### Comandos dir() e help()
```bash
dir(<obj>)  # Lista os nomes no escopo do objeto
help(<int>)  # Mostra a documentação da classe int
```

# Convenção sobre variável e constante

Por convenção, usa-se letras maíusculas para constantes
* **Variáveis**: letras minúsculas e underscores (ex: `minha_variavel`)
* **Constantes**: letras maiúsculas e underscores (ex: `MINHA_CONSTANTE`)

# Conversão de tipos

* `int()`: Converte para inteiro
* `float()`: Converte para ponto flutuante

**Exemplos:**
```python
int(10.5)  # Retorna 10
float(10)  # Retorna 10.0
print(10 / 2)  # Retorna 5.0
print(10 // 2)  # Retorna 5
```
> Importante: Ele trunca o valor para inteiro e não arredonda

# Concatenação de strings

### Usando o operador +
```python
nome = "Maria"
sobrenome = "Silva"
nome_completo = nome + " " + sobrenome
print(nome_completo) 	# Retorna "Maria Silva"
```

### Usando f-strings (Python 3.6+)
```python
nome = "Maria"
sobrenome = "Silva"
nome_completo = f"{nome} {sobrenome}"
print(nome_completo)  # Retorna "Maria Silva"
```

# Funções de entrada e saída

* `input()`: Lê uma entrada do usuário como string
* `print()`: Exibe uma saída no console

> A função built-in `print()` pode receber múltiplos argumentos separados por vírgulas.
> Ela recebe um argumento obrigatório e quatro opcionais: `sep`, `end`, `file` e `flush`.
>> * `sep`: define o separador entre os argumentos (padrão é espaço)
>> * `end`: define o que será impresso no final (padrão é nova linha `\n`)
>> * `file`: define o objeto onde a saída será escrita (padrão é `sys.stdout`)
>> * `flush`: define se o fluxo de saída será forçado a ser escrito (padrão é `False`)

**Exemplo:**

```python
nome = input("Digite seu nome: ")
print(f"Olá, {nome}!")

# Exemplo com múltiplos argumentos:
print("Olá", nome, "!", sep=", ", end="\n")

# Exemplo redirecionando a saída para um arquivo:
with open("saida.txt", "w") as f:
    print("Olá, mundo!", file=f)

# Exemplo forçando o flush da saída:
import sys
print("Processando...", end="", flush=True)
```

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
* `in`      : verifica se um valor está presente em uma sequência
* `not in`  : verifica se um valor não está presente em uma sequência

### Identidade
* `is`      : verifica se dois objetos são o mesmo objeto na memória
* `is not` d: verifica se dois objetos não são o mesmo objeto na memória

## Precedência de operadores

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

## Notas sobre operadores

* `%`: operador módulo retorna o resto da divisão inteira
* `**`: operador de exponenciação
* `//`: operador de divisão inteira (trunca o valor)