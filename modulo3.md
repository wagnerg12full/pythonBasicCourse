# 📚Módulo 3: Estruturas de Dados Simples (Coleções Nativas)

Em Python, as coleções são estruturas que nos permitem armazenar múltiplos valores em uma única variável. As quatro coleções nativas mais importantes são Listas, Tuplas, Dicionários e Conjuntos.

## 3.1 Listas (list)

As listas são a coleção mais versátil e frequentemente usada em Python.

### Características Principais

- **Ordenadas:** Os elementos mantêm a ordem em que foram inseridos.
- **Mutáveis:** Você pode adicionar, remover ou modificar elementos após a criação.
- **Permitem Duplicatas:** Podem conter valores repetidos.

### Criação e Acesso
As listas são definidas por colchetes "[]", com itens separados por vírgulas.

```python
# Criação
frutas = ["Maçã", "Banana", "Morango", "Maçã"]
numeros = [10, 20, 30, 40]

## Acesso (Indexação)
# A contagem sempre começa no índice 0.
primeira_fruta = frutas[0]  # Resultado: "Maçã"
ultima_fruta = frutas[3]   # Resultado: "Maçã"

## Acesso Invertido (Indexação Negativa)
# O índice -1 se refere ao último item.
ultimo_item = numeros[-1]  # Resultado: 40
```


### Métodos Essenciais para Listas

|Método|Descrição|Exemplo|
|--|--|--|
|*.append()*|Adiciona um item ao final da lista.|frutas.append("Uva")|
|*.insert()*|Adiciona um item em uma posição específica.|frutas.insert(1, "Pêra")|
|*.remove()*|Remove a primeira ocorrência de um valor.|frutas.remove("Maçã")|
|*.pop()*|Remove o item de um índice específico (ou o último, se vazio) e o retorna.|	item_removido = frutas.pop(2)|
|*.sort()*|Ordena a lista in-place (modifica a lista original).|numeros.sort()|

### Fatiamento (Slicing)

Permite extrair uma porção (sublista) da lista original. A sintaxe é "lista[início:fim:passo]". O índice fim é exclusivo.

```python
# Fatiamento básico: do índice 1 até (mas não incluindo) o 3
sub_lista = numeros[1:3] # Resultado: [20, 30]

# Do início até o índice 2
inicio = numeros[:3]     # Resultado: [10, 20, 30]

# Do índice 2 até o fim
fim = numeros[2:]        # Resultado: [30, 40]
```

## 3.2. Tuplas (tuple)

Tuplas são muito semelhantes às listas, mas com uma diferença crucial.

### Características Principais

- **Ordenadas:** Mantêm a ordem de inserção.
- **Imutáveis:** Após a criação, você não pode alterar, adicionar ou remover elementos. São usadas para dados que não devem mudar (ex: coordenadas, configurações).
- **Permitem Duplicatas:** Podem conter valores repetidos.

### Criação e Acesso

Tuplas são definidas por parênteses ().

```python
# Criação
coordenada = (10, 5)
cores = ("Azul", "Verde", "Vermelho")

# Acesso (Indexação e Slicing) funciona exatamente como nas listas
primeira_cor = cores[0]  # Resultado: "Azul"

# TENTATIVA INVÁLIDA (dará erro)
# coordenada[0] = 20
```

## 3.3. Dicionários (dict)
Dicionários são coleções usadas para armazenar dados em pares de Chave-Valor.

### Características Principais

 - **Não Ordenados (em versões antigas):** Em Python 3.7+ são ordenados.
 - **Mutáveis:** Podem ser modificados.
 - **Chaves Únicas:** Cada chave deve ser única e imutável (geralmente strings ou integers).

### Criação e Acesso
Dicionários são definidos por chaves {}.

```python
# Criação: {chave: valor, chave: valor}
aluno = {
    "nome": "Carla Silva",
    "idade": 21,
    "curso": "Computação",
    "matriculado": True
}

# Acesso pelo Nome da Chave
nome_aluno = aluno["nome"]  # Resultado: "Carla Silva"

# Adição / Modificação de Elementos
aluno["cidade"] = "Fortaleza" # Adiciona nova chave-valor
aluno["idade"] = 22          # Modifica o valor da chave existente
```
### Iteração e Métodos de Dicionário

|Método|Descrição|
|--|--|
|*.keys()*|Retorna uma visão de todas as chaves do dicionário.|
|*.values()*|Retorna uma visão de todos os valores do dicionário.|
|*.items()*|Retorna uma visão de pares (chave, valor) do dicionário.|

```python
# Iterando sobre as chaves (padrão)
for chave in aluno:
    print(chave, aluno[chave])

# Iterando sobre pares chave-valor
for chave, valor in aluno.items():
    print(f"{chave}: {valor}")
```

## 3.4. Conjuntos (set)
Conjuntos são coleções matemáticas que se baseiam no conceito de não-repetição.

### Características Principais

- **Não Ordenados:** Não mantêm a ordem de inserção (o acesso por índice não existe).
- **Mutáveis:** Podem ter elementos adicionados ou removidos.
- **Elementos Únicos:** Não permitem valores duplicados.

### Criação e Operações
Conjuntos são definidos por chaves {}, ou pela função set().

```python

# Criação (elementos duplicados são ignorados automaticamente)
numeros = {1, 2, 3, 3, 4, 5}  # Resultado: {1, 2, 3, 4, 5}
linguagens = {"Python", "Java", "C++"}

# Adicionar e Remover
linguagens.add("JavaScript")
linguagens.remove("C++")

# Operações de Conjuntos (Teoria dos Conjuntos)
outras_linguagens = {"Java", "Ruby", "Python"}

# Intersecção: elementos em comum
comum = linguagens.intersection(outras_linguagens) # Resultado: {'Python', 'Java'}
```

## 🧠 Desafio de Programação (Módulo 3)

Crie um programa que faça o Registro de Notas de 3 alunos.
1. Crie um Dicionário onde a chave é o nome do aluno (string) e o valor é uma Lista de três notas (float).
2. Use um laço for para percorrer o dicionário. Para cada aluno:
    - Calcule a média aritmética das notas que estão na lista.
    - Imprima o nome do aluno e sua média final.
