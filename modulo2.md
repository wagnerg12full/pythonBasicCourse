# 📚Módulo 2: Fundamentos da Linguagem


## 2.1. Variáveis e Tipos de Dados

Em Python, você não precisa declarar o tipo de uma variável explicitamente antes de usá-la. A linguagem é de tipagem dinâmica, o que significa que o tipo é determinado automaticamente pelo valor que você atribui.

### Variáveis em Python
Atribuição: Use o sinal de igual (=).
```python
nome = "Alice"
idade = 25
preco = 49.90
```
**Boas Práticas:**
 Use nomes de variáveis claros, descritivos e em *snake_case* (tudo minúsculo, separado por sublinhado).

### Tipos de Dados Primitivos

| Tipo Python | Descrição | Exemplo |
|--|--|--|
|*int*|Números inteiros (sem parte decimal).|100, -5|
|*float*|Números de ponto flutuante (com parte decimal).|	3.14, 0.5|
|*str*|Sequência de caracteres (texto), delimitada por aspas simples ou duplas.|'Olá', "Python"|
|*bool*|Valores lógicos, podendo ser apenas True ou False.|True, False|

### Conversão de Tipos (Type Casting)

Como a função input() sempre retorna uma string, muitas vezes é necessário converter o tipo para realizar operações matemáticas.

|Função|Uso|Exemplo|
|--|--|--|
|*int()*|Converte para inteiro.|int("10") resulta em 10
|*float()*|Converte para ponto flutuante.|float(5) resulta em 5.0
|*str()*|Converte para string.|str(100) resulta em "100"

#### Exemplo de Conversão
```python
numero_str = input("Digite um número: ") # Recebe '10' (tipo str)
numero_int = int(numero_str) # Converte para 10 (tipo int)
resultado = numero_int + 5
print("O resultado é:", resultado)
```

## 2.2. Operadores

### Operadores Aritméticos

Usados para realizar cálculos matemáticos.

|Operador|Operação|Exemplo|Resultado|
|--|--|--|--|
|+|Adição|5 + 2|7
|-|Subtração|5 - 2|3
|*|Multiplicação|5 * 2|10
|/|Divisão (sempre retorna float)|5 / 2|2.5
|//|Divisão Inteira (descarta a parte decimal)|5 // 2|2
|%|Módulo (resto da divisão)|5 % 2|1
|**|Exponenciação|5 ** 2|25

### Operadores Relacionais (Comparação)
Retornam um valor booleano (True ou False).

|Operador|Significado|Exemplo|
|--|--|--|
|==|Igual a|idade == 18|
|!=|Diferente de|nome != 'Maria'|
|>|Maior que|saldo > 1000|
|<|Menor que|valor < 50|
|>=|Maior ou igual a|nota >= 7.0|
|<=|Menor ou igual a|dias <= 30|

### Operadores Lógicos
Usados para combinar expressões booleanas (relacionais).

|Operador|Função|Exemplo|
|--|--|--|
|and|Retorna True se ambas as condições forem True.|x > 5 and y < 10|
|or|Retorna True se pelo menos uma das condições for True.|dia == 'Sabado' or dia == 'Domingo'|
|not|Inverte o valor lógico.|not tem_permissao|

## 2.3. Estruturas Condicionais (Decisão)

As estruturas condicionais controlam quais blocos de código devem ser executados, baseadas na avaliação de uma expressão booleana. A **identação** (espaçamento à esquerda) define o bloco de código em Python.

### O "if" Simples
```python
idade = 19
if idade >= 18:
    print("Você é maior de idade.")
```


### O "if/else" (Bifurcação Simples)
```python
saldo = 500.00
if saldo > 0:

 print("Sua conta está positiva.")
else:
    print("Sua conta está negativa. Atenção!")
```


### O "if/elif/else" (Múltiplas Condições)
O *elif* (*else if*) é usado para testar múltiplas condições em sequência.

```python
nota = float(input("Digite a nota: "))

if nota >= 7.0:
    print("Aprovado!")
elif nota >= 5.0: # Testa apenas se a primeira condição (nota >= 7.0) for False
    print("Recuperação.")
else:
    print("Reprovado.")
```


## 2.4. Estruturas de Repetição (Laços)
Os laços permitem executar um bloco de código repetidamente.

### O laço "while" (Repetição Condicional)
Executa um bloco de código enquanto uma condição for verdadeira.

```python
contador = 1
while contador <= 5:
    print(contador)
    contador = contador + 1 # Atualiza a variável de controle
print("Fim do loop while.")
```


### O laço "for" (Iteração)

O for em Python é tipicamente usado para iterar sobre elementos de uma sequência (como uma lista ou uma faixa de números).
Usamos a função range() para gerar uma sequência de números:
|Funçãorange()|Gera
|--|--|
|*range(5)*|Números de 0 até 4 (5 - 1)|
|*range(2, 6)*|Números de 2 até 5|
|*range(1, 10, 2)*|Números de 1 até 9 (com passo de 2)|


```python
# Exemplo de for: Imprimindo os 5 primeiros números
for i in range(5):
    print("Número:", i)
```


### Comandos break e continue

***break***: Interrompe imediatamente a execução do laço (sai do for ou while).
***continue***: Pula para a próxima iteração do laço (o código restante no bloco é ignorado).

## 🧠 Desafio de Programação (Módulo 2)

Crie um programa que simule a tabuada de um número.
1. Peça ao usuário que digite um número inteiro. (Lembre-se da conversão de tipos!)
2. Use um laço for para calcular e exibir a tabuada desse número (de 1 a 10).

Exemplo de Saída (se o usuário digitar 7):

```python
7 x 1 = 7
7 x 2 = 14
...
7 x 10 = 70
```
