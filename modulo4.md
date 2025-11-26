# 📚Módulo 4: Funções e Modularização
Aprender a usar funções é o passo mais importante para escrever códigos limpos, eficientes e de fácil manutenção. Funções permitem empacotar um bloco de código que pode ser executado várias vezes.

## 4.1. Definição e Chamada de Funções
### Palavra-Chave def
Em Python, definimos uma função usando a palavra-chave def seguida pelo nome da função e parênteses (). O corpo da função é definido pela identação.

```python
# 1. Função sem parâmetros e sem retorno
def saudacao():
    print("Olá! Seja bem-vindo ao módulo de funções.")

# Chamada da função
saudacao()
```

### Parâmetros e Argumentos
- **Parâmetros:** São as variáveis listadas dentro dos parênteses na definição da função.
- **Argumentos:** São os valores enviados à função quando ela é chamada.

```python
# 2. Função com parâmetros
def cumprimentar(nome): # 'nome' é o parâmetro
    print(f"Olá, {nome}. É um prazer te conhecer.")

# Chamada da função com argumento
cumprimentar("Maria") # "Maria" é o argumento
cumprimentar("João")

```
### Valor de Retorno (return)
A instrução return é usada para enviar um valor de volta ao ponto onde a função foi chamada. Se nenhuma instrução return for usada, a função retorna implicitamente o valor especial None.

```python
# 3. Função com retorno
def somar(a, b):
    resultado = a + b
    return resultado # Retorna o valor calculado

# A variável 'soma_total' armazena o valor retornado
soma_total = somar(15, 7)
print(f"A soma é: {soma_total}") # Saída: A soma é: 22
```


## 4.2. Escopo de Variáveis
O escopo define a região do programa onde uma variável é acessível. Entender o escopo é vital para evitar erros e garantir que o código funcione de forma previsível.

### Variáveis Locais
São variáveis definidas dentro do corpo de uma função. Elas só podem ser acessadas de dentro dessa função.

```python
def calcular_area(largura, altura):
    # 'area' é uma variável LOCAL
    area = largura * altura
    return area

area_calculada = calcular_area(10, 5)
# print(area) # Erro! A variável 'area' não existe fora da função.
```

### Variáveis Globais
São variáveis definidas fora de qualquer função (no nível superior do módulo). Elas podem ser lidas por qualquer função. Para modificar uma variável global dentro de uma função, você deve usar a palavra-chave global.

```python
# 'PI' e 'contador_global' são variáveis GLOBAIS
PI = 3.14159
contador_global = 0

def incrementar_contador():
    # Usamos 'global' para indicar que queremos MODIFICAR a variável global
    global contador_global
    contador_global += 1

incrementar_contador()
print(f"Contador: {contador_global}") # Saída: Contador: 1

```
## 4.3. Parâmetros Especiais e Padrão
### Argumentos Padrão (Default)
Você pode atribuir um valor padrão a um parâmetro. Se o chamador não fornecer um argumento para esse parâmetro, o valor padrão é usado.

```python
def log_mensagem(texto, nivel="INFO"):
    print(f"[{nivel}]: {texto}")

log_mensagem("Processo iniciado.")            # Usa o padrão "INFO"
log_mensagem("Erro crítico!", nivel="ERRO")   # Sobrescreve o padrão
```
### Argumentos Arbitrários (*args e **kwargs)
Essas sintaxes permitem que uma função receba um número variável de argumentos.
- ***args (Argumentos Posicionais):** Coleta todos os argumentos posicionais extras em uma tupla.
- ****kwargs (Argumentos Nomeados):** Coleta todos os argumentos nomeados extras em um dicionário.

```python
def exibir_perfil(nome, *cursos, **extras):
    print(f"Nome: {nome}")
    print(f"Cursos: {cursos}") # (Ciência, Eng. Software)
    print(f"Extras: {extras}") # {'Cidade': 'SP', 'ID': 123}

exibir_perfil("Pedro", "Ciência", "Eng. Software", Cidade="SP", ID=123)
```

## 4.4. Módulos e Pacotes
A modularização é a prática de dividir um programa grande em arquivos menores e independentes (módulos) para organização e reuso.

### O Conceito de Módulo
Um Módulo em Python é simplesmente um arquivo .py que contém código (funções, classes, variáveis).

### Importando Módulos

Usamos a palavra-chave import para usar o código de outro arquivo.
1. Criação do Módulo (Ex: matematica.py):
```python
# Arquivo: matematica.py
PI = 3.14159

def calcular_dobro(numero):
    return numero * 2

2.Uso em Outro Arquivo (Ex: main.py):
Python
# Arquivo: main.py
import matematica # Importa tudo do arquivo matematica.py

# Acessa usando o nome do módulo
raio = 5
area = matematica.PI * raio ** 2
print(area)

dobro = matematica.calcular_dobro(10)
print(dobro)
```


### Importação Seletiva (from ... import)
Permite importar apenas funções ou variáveis específicas, usando-as sem o prefixo do nome do módulo.

```python
from matematica import PI, calcular_dobro

# Uso direto, sem o prefixo 'matematica.'
print(f"O valor de PI é: {PI}")
```


## 🧠 Desafio de Programação (Módulo 4)

Crie um programa com um módulo de funções chamado utilidades.py e um arquivo principal app.py.
1. No arquivo utilidades.py, crie uma função chamada calcular_media(lista_de_notas) que recebe uma lista de números e retorna a média aritmética deles.
2. No arquivo app.py:
    - Importe apenas a função calcular_media.
    - Defina uma lista de notas.
    - Chame a função calcular_media e imprima o resultado com uma mensagem formatada.
