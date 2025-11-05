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