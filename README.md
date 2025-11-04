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

`int()` | `float()` | `complex()` | `list()` | `tuple()` | `range()` | `str()` | `set()` | `frozenset()` | `dict()` | `bool()` | `bytes()` | `bytearray()` | `memoryview()`

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
>* **Variáveis**: letras minúsculas e underscores (ex: `minha_variavel`)
>* **Constantes**: letras maiúsculas e underscores (ex: `MINHA_CONSTANTE`)

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

# Estruturas de dados

### 📝 Listas (Vetores/Arrays Dinâmicos)
A estrutura de dados mais comum para sequências. Flexível e poderosa.

```python
# Declaração e Acesso
my_list = [10, 20, 30, 40]
first = my_list[0]
last = my_list[-1]

# Modificação
my_list.append(50)      # Adiciona ao final -> O(1)
my_list.pop()           # Remove do final -> O(1)
my_list.pop(0)          # Remove do início (lento!) -> O(n)

# Informações e Fatiamento (Slicing)
length = len(my_list)
sub_list = my_list[1:3] # [30, 40]
```


### 📚 Dicionários (Hash Maps)

Essenciais para buscas, contagens e mapeamentos com performance `O(1)` em média.
```python
# Declaração e Acesso
counts = {'apple': 3, 'banana': 5}
apple_count = counts['apple']

# Adicionar/Atualizar
counts['orange'] = 1 # Adiciona
counts['apple'] = 4  # Atualiza

# Acesso Seguro e Verificação
banana_count = counts.get('banana', 0) # Retorna 0 se 'banana' não existir
if 'cherry' in counts:
    print("Temos cerejas!")

# Iteração
for fruit, count in counts.items():
    print(f"{fruit}: {count}")
```

### 🔢 Matrizes (Listas de Listas)

Perfeitas para representar dados em 2D, como tabuleiros, imagens ou grafos.
```python
# Declaração (matriz 3x4 com zeros)
rows, cols = 3, 4
matrix = [[0 for _ in range(cols)] for _ in range(rows)]

# Acesso e Dimensões
element = matrix[1][2] # Linha 1, coluna 2
num_rows = len(matrix)
num_cols = len(matrix[0])

# Iteração
for r in range(num_rows):
    for c in range(num_cols):
        print(matrix[r][c], end=' ')
    print()
```


## If ternário

É uma estrutura simplificada da condicional
```python
status = "Sucesso" if saldo >= saque else "Falha"
print(f"{status} ao realizar o saque!")
```

## Estruturas de repetição

### ➿ for
> Usado para percorrer um objeto iterável ou repetir `n` vezes. 
```python
for <temp_var> in <obj_iteravel>:
    # ...
else:
    # Apenas quando o laço termina naturalmente
    # Pode ser omitido
```

Variações comuns:
```python
# range(fim) - de 0 até fim-1
for i in range(5):
    print(i)  # Imprime 0, 1, 2, 3, 4

# range(inicio, fim)
for i in range(2, 5):
    print(i)  # Imprime 2, 3, 4

# range(inicio, fim, passo)
for i in range(10, 0, -2):
    print(i)  # Imprime 10, 8, 6, 4, 2

nomes = ["Ana", "Bruno", "Carla"]

for nome in nomes:
    print(nome)  # Imprime Ana, Bruno, Carla

for letra in "Python":
    print(letra) # Imprime P, y, t, h, o, n
    
for indice, nome in enumerate(nomes):
    print(f"{indice}: {nome}") # Imprime 0: Ana, 1: Bruno, 2: Carla

usuario = {"nome": "Lucas", "idade": 30}

# Iterar sobre chaves (padrão)
for chave in usuario:
    print(chave) # Imprime nome, idade

# Iterar sobre valores
for valor in usuario.values():
    print(valor) # Imprime Lucas, 30

# Iterar sobre ambos (chave e valor)
for chave, valor in usuario.items():
    print(f"{chave} = {valor}") # Imprime nome = Lucas, idade = 30

```

### ➿ while
```python
while <condicao_verdadeira>:
    # ...
else:
    # Apenas quando o laço termina naturalmente
    # Pode ser omitido
```

# Manipulação de objetos string



### <>
```python

```