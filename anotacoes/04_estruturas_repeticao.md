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