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