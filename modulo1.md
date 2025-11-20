# Módulo 1: Introdução ao Python e Ambiente de Desenvolvimento

## 1.1. Por que Python?

Bem-vindo ao Python! Se você já domina a lógica de programação, está pronto para dar o salto para uma das linguagens mais poderosas e versáteis do planeta.

### O que torna o Python especial?

* Sintaxe Clara e Legível: A filosofia do Python valoriza a legibilidade do código, utilizando identação para definir blocos (o que substitui chaves {} ou ponto e vírgula ;). Essa característica facilita o aprendizado e a manutenção do código.
* Versatilidade e Adoção: Python não é limitado a uma área. É a linguagem de escolha em:
  - Data Science e Inteligência Artificial (IA): Bibliotecas como Pandas, NumPy e TensorFlow.
  - Desenvolvimento Web: Frameworks robustos como Django e Flask.
  - Automação e DevOps: Criação de scripts para tarefas repetitivas e gerenciamento de infraestrutura.
* Comunidade Vasta: O Python possui uma comunidade global enorme e ativa, o que significa que há sempre documentação, frameworks e suporte disponíveis.
  
💡 O "Zen of Python": A filosofia da linguagem é guiada por 19 "princípios" incluídos no Python, acessíveis pelo comando import this. O mais famoso é: "Bonito é melhor do que feio."

## 1.2. Configuração do Ambiente de Desenvolvimento

Para começar a programar, precisamos de duas coisas essenciais: o interpretador Python e um editor de código (IDE).

### A. Instalando o Python (O Interpretador)

Python é uma linguagem interpretada. Isso significa que você precisa de um programa (o interpretador) para ler seu código e executá-lo.
  * Download: Acesse o site oficial (python.org) e baixe a versão estável mais recente do Python 3.
  * Instalação: Crucial! Certifique-se de marcar a caixa "Add Python to PATH" durante a instalação. Isso permite que você execute o Python a partir de qualquer diretório do seu sistema operacional.
  * Verificação: Abra o Terminal (ou Prompt de Comando/PowerShell) e digite:

```
python --version
```

Se a versão for exibida (ex: Python 3.11.x), a instalação foi bem-sucedida.

### B. Escolhendo o Editor de Código (IDE)

Embora você possa escrever código Python em qualquer editor de texto, um IDE (Ambiente de Desenvolvimento Integrado) oferece ferramentas que facilitam muito a vida do programador (sugestões de código, debugging, realce de sintaxe).

  * VS Code (Visual Studio Code): Altamente recomendado pela leveza, vasto suporte a extensões e versatilidade.
  * PyCharm Community Edition: Um IDE específico para Python, mais robusto e com excelentes ferramentas de refatoração e debugging.

### C. Gerenciamento de Pacotes com PIP

O PIP (Pip Installs Packages) é o gerenciador de pacotes padrão do Python. Ele é usado para instalar bibliotecas de terceiros que estendem as funcionalidades da linguagem (ex: instalar a biblioteca requests para fazer requisições HTTP). O PIP é geralmente instalado automaticamente junto com o Python.

Instalar um Pacote:

```
pip install nome-do-pacote
```

Listar Pacotes Instalados:

```
pip list
```


## 1.3. Primeiro Programa e Interação


### A. O Clássico "Hello World"

O primeiro passo é escrever e executar um código simples. No seu editor, crie um arquivo chamado ola.py e digite:

Python

```
print("Olá, Mundo! Meu primeiro código Python.")
```

Para executar, abra o Terminal no mesmo diretório do arquivo e digite:

```
python ola.py
```

Saída esperada: Olá, Mundo! Meu primeiro código Python.

### B. A Função print() (Saída de Dados)

A função print() é utilizada para exibir informações na tela (console).

**Exibindo texto (string)**

```
print("A sintaxe do Python é simples.")
```
**Exibindo números**
```
print(10 + 5)
```


### C. A Função input() (Entrada de Dados)

A função input() é usada para solicitar dados ao usuário através do console. O dado inserido é sempre capturado como uma String.

**O texto dentro de input() é o prompt que o usuário verá**
```
nome = input("Qual é o seu nome? ")
print("Seja bem-vindo,", nome)
```



🧠 Exercício de Fixação (Prática Imediata)

Crie um script chamado apresentacao.py.
Use a função input() para perguntar ao usuário em qual ano ele nasceu.
Use a função print() para exibir uma mensagem de boas-vindas e o ano digitado.
