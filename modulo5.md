# 📚 Módulo 5: Tópicos de Conclusão e Prática
Este módulo foca em tornar seu código robusto e em introduzir práticas essenciais do desenvolvimento de software.

## 5.1. Manipulação de Arquivos
Praticamente toda aplicação precisa ler ou salvar dados permanentemente. Em Python, a manipulação de arquivos é feita com a função nativa open().

### Abrindo e Fechando Arquivos
A função *open()* recebe o nome do arquivo e o modo de operação.

|Modo|Descrição|
|--|--|
|"r"|Leitura (read): Padrão. O arquivo deve existir.
|"w"|Escrita (write): Cria um novo arquivo. Se o arquivo já existir, o conteúdo é apagado.
|"a"|Anexar (append): Adiciona conteúdo ao final do arquivo. Se não existir, é criado.

```python
# Abrindo um arquivo no modo escrita e escrita
arquivo = open("dados.txt", "w")

# É fundamental fechar o arquivo após a operação para liberar recursos.
arquivo.close()
```

### Leitura e Escrita de Dados
**Escrita (write)**
```python
arquivo = open("log.txt", "w")
arquivo.write("Registro de início do programa.\n")
arquivo.write("O Python é poderoso!")
arquivo.close()
# Ao final, 'log.txt' terá as duas linhas.
```

**Leitura (read e readline)**
```python
arquivo = open("log.txt", "r")

# Lendo o conteúdo todo de uma vez como uma única string
conteudo_completo = arquivo.read()
print(conteudo_completo)

# Lendo o arquivo linha por linha em um laço for
for linha in arquivo:
    print(f"Linha lida: {linha.strip()}") # .strip() remove espaços/quebras de linha

arquivo.close()
```
### O Bloco with (Melhor Prática)
O método mais seguro e recomendado para trabalhar com arquivos é usando o bloco *with*. Ele garante que o arquivo será fechado automaticamente, mesmo que ocorra um erro.
```python
with open("config.txt", "r") as arquivo:
    # O arquivo é automaticamente fechado ao sair do bloco 'with'
    dados = arquivo.read()
    print("Dados lidos:", dados)
```
## 5.2. Tratamento de Erros e Exceções
Erros que ocorrem durante a execução do programa são chamados de Exceções. Tratar exceções significa prever e gerenciar esses erros para que o programa não pare abruptamente (crash).

### O Bloco try-except
Usamos o bloco try para colocar o código que pode gerar um erro e o bloco except para definir o que deve acontecer se o erro de fato ocorrer.
```python
try:
    # Código que PODE falhar (ex: conversão inválida)
    numero = int(input("Digite um número inteiro: "))
    resultado = 10 / numero

except ValueError:
    # Captura erros se o usuário digitar um texto em vez de um número
    print("Erro: Entrada inválida. Você deve digitar um número inteiro.")

except ZeroDivisionError:
    # Captura erros se o usuário digitar 0
    print("Erro: Não é possível dividir por zero.")
    
except Exception as e:
    # Captura qualquer outro erro inesperado e exibe a mensagem
    print(f"Ocorreu um erro desconhecido: {e}")

else:
    # Opcional: Bloco executado SOMENTE se o 'try' for bem-sucedido (sem erros)
    print(f"O cálculo foi bem-sucedido. Resultado: {resultado}")

finally:
    # Opcional: Bloco executado SEMPRE, ocorra erro ou não.
    print("Fim da operação de cálculo.")
```
## 5.3. Ferramentas de Versionamento: Introdução ao Git
O Git não é uma disciplina de programação, mas é a ferramenta profissional essencial para gerenciar o histórico do seu código.

### O que é Versionamento?
O controle de versão é um sistema que registra as mudanças em um arquivo ou conjunto de arquivos ao longo do tempo. Ele permite que você recupere versões específicas e, o mais importante, facilita o trabalho em equipe.

### Conceitos Chave do Git
- **Repositório:** Pasta do seu projeto que o Git está monitorando.
- **Commit:** Um "instantâneo" (foto) das mudanças do seu código em um determinado momento, acompanhado de uma mensagem descritiva.
- **Branch:** Um caminho paralelo para o desenvolvimento. Permite que você trabalhe em novas funcionalidades sem afetar a versão principal (o main ou master).

### Comandos Básicos (Terminal)

|Comando|Descrição|
|--|--|
|git init|Inicializa um novo repositório Git na pasta atual.|
|git status|Exibe o estado dos arquivos (quais foram modificados, quais estão prontos para o commit).|
|git add .|Prepara todos os arquivos modificados para o commit (movendo-os para a staging area).|
|git commit -m|"Mensagem"	Grava as mudanças preparadas no histórico. A mensagem deve ser concisa e descritiva.|
|git log|Exibe o histórico de commits.|
|git push|Envia os commits locais para um repositório remoto (como o GitHub).|

💡 **Prática Recomendada:** Utilize o GitHub ou GitLab para armazenar seus projetos remotamente, garantindo um backup seguro e facilitando a colaboração futura.

## 🧠 Projeto Final (Python Básico)
Desenvolva um Gerenciador de Tarefas em Linha de Comando.
- Use Listas para armazenar as tarefas.
- Implemente Funções para Adicionar, Listar e Marcar Tarefas como Concluídas.
- Use a Manipulação de Arquivos (Módulo 5.1) para salvar e carregar as tarefas em um arquivo de texto, para que elas persistam após o programa ser fechado.
- Utilize o bloco try-except (Módulo 5.2) para garantir que o programa lide com entradas inválidas do usuário.
- Registre todo o desenvolvimento com git commit.
