



# Manipulação de objetos string

> **STRINGS SÃO IMUTÁVEIS**
>
> Métodos de string sempre retornam uma `nova` string.

### Transformação (Aparência)


```python
# --- Maiúsculas/Minúsculas ---
texto = "   O lá Mundo    "
print(texto.upper())  #>>> "   O LÁ MUNDO"
print(texto.lower())  #>>> "   o lá mundo"
print(texto.title())  #>>> "   O Lá Mundo"

# --- Espaços em Branco ---
print(texto.strip(), end="|\n")  # Remove de ambos os lados -> "O lá Mundo|"
print(texto.lstrip(), end="|\n") # Remove da esquerda      -> "O lá Mundo    |"
print(texto.rstrip(), end="|\n") # Remove da direita       -> "   O lá Mundo|"

# --- Alinhamento ---
print(texto.center(21, "#")) #>>> "##   O lá Mundo    ##"
```
### Quebra e Junção (Estrutura)

```python
# --- Quebrar (String -> Lista) ---
palavras = "Python é muito legal".split()  #>>> ['Python', 'é', 'muito', 'legal']
data = "05/11/2025".split('/') #>>> ['05', '11', '2025']

# --- Juntar (Lista -> String) ---
curso = ["P", "y", "t", "h", "o", "n"]

print(".".join(curso)) #>>> "P.y.t.h.o.n"
print(" ".join(palavras)) #>>> "Python é muito legal"
```
### Busca e substituição
```python
texto = "Eu amo Python! Python é minha linguagem favorita."

# --- Encontrar ---
print(texto.find("Python"))    # Retorna o índice da *primeira* ocorrência (7)
print(texto.find("Java"))      # Retorna -1 se não encontrar

# --- Substituir ---
print(texto.replace("Python", "Java"))
#>>> "Eu amo Java! Java é minha linguagem favorita."
```

### Fatiamento (Slicing)
>Sintaxe: `[start: stop: step]`
```python
nome = "Ariel Gideon Ramos"
print(nome[0])        #>>> "A"
print(nome[:5])       #>>> "Ariel"
print(nome[6:])       #>>> "Gideon Ramos"
print(nome[6:12])     #>>> "Gideon"
print(nome[5:18:2])   #>>> " ienRms" (passo 2)
print(nome[::-1])     #>>> "somaR noediG leirA" (inverte)
```


### Interpolação (Formatação)
>O método `f-string (Python 3.6+)` é mais usado, rápido e legível.
```python
# --- f-strings (O Padrão Moderno) ---
nome, idade, PI = "Ariel", 29, 3.14159

print(f"Olá, me chamo {nome} e tenho {idade} anos.")
print(f"Valor de PI: |{PI:9.2f}|") # >>> "Valor de PI: |     3.14|"
```

**Legado**:
* `.format()`: *print( "Olá,* **`{}`**. *Você tem* **`{}`** *anos.*"**.format(nome, idade)** *)*
* `Old Style (%)`: *print( "Olá,* `%s`. Você tem `%d` anos." **% (nome, idade)** *)*

> * `%s`: **String** (converte o objeto para string usando `str()`)
> * `%d`: **Decimal** (converte para um número inteiro)
> * `%f`: **Float** (converte para um número de ponto flutuante/decimal)
> * `%r`: **Representação** (converte o objeto usando `repr()`, mostrando aspas para strings)