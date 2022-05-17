# Objetivos:

1. Git/GitHub Introdução
2. Ferramentas GIT
3. Controle de versão
4. Git e repositório
5. Git vs Github
6. Git - Primeiros passos
7. Criando um repositório no GIT
8. Checando diferentes versões
9. Sistema Distribuído Seguro no GitHub
10. Criando repositório no GitHub
11. Clonando em modo seguro (SSH) do GITHub para seu PC
12. Promovendo atualização em um repositório remoto:
13. Resolvendo conflitos


# 1. Git/Github Introdução:

Git é um **sistema de controle de versão distribuído** projetado para lidar com tudo, desde projetos pequenos a muito grandes com rapidez e eficiência.

O Git é um projeto de código aberto maduro e com manutenção ativa desenvolvido em 2005 por Linus Torvalds, o famoso criador do kernel do sistema operacional Linux

## Ferramentas para desenvolvimento de Software
**GIT e GIT HUB**

### GIT – Software de controle de versões

* Software/Sistema de versionamento de Código distribuido
* Criador Linux Tovalds
* Software é colaborativo
* Necessidade versionar versões e complexo para várias pessoas
* Padrão de Mercado 

## GITHUB - Plataforma de hospedagem, controle de código e colaboração

PGitHub é uma **plataforma de hospedagem** de código para controle de versão e colaboração utilizando o GIT. 

Permite que programadores, utilitários ou qualquer usuário cadastrado na plataforma contribuam em projetos privados e/ou Open Source de qualquer lugar do mundo.

# 2. Ferramentas GIT

**Windows Git Clients:**
* Sourcetree 
* GitHub for Windows
* Tortoise Git 

**Mac Git Clients:**
* GitUp 
* GitBox 
* Git-Xdev 

# 3. Controle de versão

* Colaborativo;
* Versionamento;
* Compreensível;
* Permitir reversão.

## Sistemas de controle de versão

* CVS;
* Subversion;
* Mercurial;
* GIT.

# 4. Git e repositórios

Git tem muitas vantagens sobre sistemas anteriores, como CVS e Subversion

## Vantagens:

* Velocidade;
* Suporte para desenvolvimento não linear (milhares de ramificações paralelas);
* Totalmente distribuído;
* Capaz de lidar com grandes projetos, como Linux, de forma eficiente.

# 5. GIT vs. GITHUB

* Git é instalado e mantido e um sistema local (ao invés de numem);
* Modelo de ramificação;
* Sistema de controle de versão de alta qualidade.

* Github é projetado como um serviço de hospedagem de repositório git;
* Totalmente baseado e serviços na nuvem;
* Compartilhar o código com outros, fornecendo o poder de fazer revisões ou edições.

# 6. GIT - Primeiros passos

## Download e instalação do GIT

Versão Padrão: http://git-scm.com/downloads

## Git BASH
O Git para Windows fornece uma emulação BASH usada para executar o Git a partir da linha de comando. *Os usuários do UNIX devem se sentir em casa, pois a emulação BASH se comporta exatamente como o comando "git" em ambientes LINUX.

### Comandos para criar repositório:
Após instalado executar o Git Bash e realizar os seguintes comandos:
* $ cd /c (Mudar diretório corrente para diretório raiz C:/);
* $ mkdir demo (Criar diretório demo dentro de C:/);
* $ cd demo (Mover para diretório C:/demo);
* $ git init (Diretório /c/demo torna-se o diretório master (repositório criado));
* $ ls -a (Lista todos arquivos e diretórios dentro de C:/demo/ (inclusive ocultos));

**Criado o diretório .git (oculto) para armazenar todas as informações de versionamento do GIT.**

# 7. Criando um repositório no GIT

## Atribuindo identificação do colaborador
Deve ser similar aos dados do usuário do GITHUB para permitir versionamento entre sistema local git e repositório na nuvem.

* $ git config --global user.name "davijaf" (Define o nome do colaborador para o repostiório)
* $ git config --global user.email "davijose@gmail.com" (Define o e-mail do colaborador para o repositório)
* $ git config --list (Apresenta a lista de parâmetros do repositório)
* Para sair digite tecla q (quit)

**Caso queira remover credenciais execute os comando abaixo:**
* $ git config --global --unset user.email (Para remover email)
* $ git config --global --unset user.name (Para remover nome)

## Funções de manipulação de repositórios no GIT

* $ git clone git@github.com:davijaf/desafio_de_projeto_repositorio_github.git (Copia um repositório GIT do servidor remoto)
* $ git add * (adiciona arquivos na stage area, local temporário)
* $ git commit (cria uma imagem da stage area)
* $ git status (compara os arquivos do diretorio com a stage area)
* $ git diff (mostra a diferença do stage com os arquivos modificados) - (Para sair tecle q)
* $ git help command (Verificar informações sobre o comando específico)
* $ git pull (Download de arquivos do repositório remoto para combinar ao repositório local)
* $ git push (Envio de novos arquivos do repositório local para combinar ao repositório remoto)

## Outras funções

* $ git init (transforma o diretório corrente em um novo repositório)
* $ git reset desfaz ação do comando **git add**, limpa a Stage Area)
* $ git branch (listar, criar e excluir ramificações do repositório)
* $ git checkout(subistituir ramificações ou restaurar diretório de arquivos)
* $ git merge (unir dois ou mais versões em desenvolvimento)
* $ git log (exigir registro do commit)
* $ git tag (etiquetar/catalogar a versão recente) 

## Adicionando um arquivo ao repositório GIT
              | Folder .git      | Folder .git
    | File       --> Stage Area     --> Repositório
    | Comando:| $ git add        | $ git commit 

### Ex.: Na pasta demo crie o arquivo teste.txt e siga os comandos abaixo:


* $ mkdir demo
* $ git init
* $ echo > teste.txt
* $ git status
* $ git add teste.txt
* $ git status
* $ git commit -m "Primeiro arquivo adicionado"
* $ git log
* $ git tag v.1.0
* $ git log

**Acrescente conteudo no arquivo teste.txt**

* $ echo "Vamos incluir um texto no arquivo texte.txt" > teste.txt
* $ git status
* $ git diff
* $ git add *
* $ git status
* $ git commit -m "Alterado conteudo do arquivo teste.txt"
* $ git tag v.2.0
* $ git log

**Adicione um novo diretório**
* $ mkdir subdemo
* $ ls -a


**Acrescente dois arquivos de texto ao diretorio subdemo**
* $ echo > /subdemo/teste2.txt
* $ echo > /subdemo/teste3.txt
* $ git status
* $ git add subdemo
* $ git status
* $ git commit -m "Adicionado o diretorio subdemo e dois arquivos"
* $ git status
* $ git log
* $ git tag v.3.0
* $ git log

# 8. Checando versões e recuperando alterações

* $ echo "Vamos incluir um texto no arquivo texte.txt e conferir diferenças" > teste.txt
* $ git status
* $ git diff HEAD~0 teste.txt
* $ git diff HEAD~1 teste.txt
* $ git diff HEAD~2 teste.txt
* $ git checkout HEAD~0 teste.txt (recupero alterações do aquivo para versão vigente)
* git status
**Consigo comparar o arquivo alterado com todas versões anteriores**

## Criar pasta de rascunhos para ser ignorada pelo GIT

o GIT pode ignorar um diretório do repositório local para utilizar como rascinho

* $ mkdir .gitignore
* $ ls -a
* $ git status
**GIT informará que não pode acessar o diretório .gitignore**

# 9. Sistem Distribuído Seguro no GitHub (SSH)

O SSH é um protocolo que garante que o repositório local e repositório remoto troquem informações de maneira segura e dinâmica. 

O processo é capaz de criptografar os arquivos enviados ao repositório do servidor, garantindo que alterações e o envio de dados sejam realizados da melhor forma.

*Devemos gerar a chave pública (repositório remoto) e a chave privada (repositório local)*

## Gerar a chava SSH
No Windows:
**GERAR A CHAVE NO GIT BASH (WINDOWS):**

-t : tipo de chave
-C : adicionar novo comentário
Obs.: Utilizado a chave **ED25519**, é assinatura de curva elíptica, cuidadosamente projetadas em vários níveis de design e implementação para atingir velocidades muito altas sem comprometer a segurança.

* $ ssh-keygen -t ed25519 -C email@example.com
Ex.:
* $ ssh-keygen -t ed25519 -C davijose@gmail.com
Enter file in which to save the key (/c/Users/User/.ssh/id_ed25519): *Comando irá sugerir o local que ficará salvo as chaves
Enter passphrase (empty for no passphrase): (Adicione uma senha)
Enter same passphrase again: (Repita a senha digitada anteriormente)
* $ cd /c/Users/User/.ssh/ (Acesse o diretório das chaves)
* $ cat id_ed25519.pub (O Git Bash irá mostrar a chave pública)

## Associar a chave pública no GitHub
* Copiei o print executado pelo comando acima, será sua chave pública. Ex.: ssh-ed25519 AAAAC3NasrfdsfsI1NTE5AAAAIIahqHpL03ZKUrZ7EV++4rUr6lN+EwlnjWEF8MtcqzhD email@example.com
* Acesse https://github.com/settings/ssh/new
* Identifique a máquina que está utilizando digitando no campo title.  Ex.: Notebook Dell Windows
* Cole o texto, chave pública, no campo Key
* Clique em Add SSH Key

## Associar a chave privado no Git

* Ainda no diretório das chaves digite:
*Ativar o SSH-AGENTE para rodar como plano de fundo*
* $ eval $(ssh-agent -s)
*Adicione a chave recentemente criada*
* $ ssh-add id_ed25519
* Enter passphrase for id_ed25519: XXXXXXXXXX
Print: Identity added: id_ed25519 (email@example.com)

# 10. Criando repositório no GITHUB

https://github.com/new
Repository name: teste (Nomeie o repositório)
Description (optional): teste
Public or Private: (Defina se todos poderão ver seu repositório ou não)
Add a README file: (Defina se adicionará um README setando o campo)
Create Repository (Clique no botão criar)

# 11. Clonando em modo seguro (SSH) do GITHub para seu PC

No repositório no GitHub clique em Code, selecione SSH e copie o endereço apresentado no campo.
Clonando o repositório remoto para o repositório local
* Dentro do diretorio de trabalho pelo Git Bash digite o comando abaixo:
* $ git clone "link ssh do repositório"
* $ git clone git@github.com:davijaf/teste.git

# 12. Promovendo atualização em um repositório remoto:

Usando o Git Bash e dentro do repositório teste digite:
* $ echo "Acrescentando texto ao README.md para enviar commit" > README.md
* $ git status
* $ git add *
* $ git commit -m "modificado conteudo do README.md"
* $ git status
* $ git push origin master

# 13. Resolvendo conflitos

Através da página do GITHUB altere o texto README.md e faça um commit online:
teste > READM.md > edit > Commit Changes
Ex.:
* 1 Acrescentando texto ao README.md para enviar commit
* 2 Acrescentando texto na segunda linha do README.md

Vá no diretório local e acrescente o texto no README.md e tente realizar o push:
* $ echo -e "Acrescentando segunda linha através do GIT no repositório local" >> README.md
* $ git status
* $ git add *
* git commit -m "acrescentado segunda linha ao README.md via repositorio local"
* $ git status
* $ git push origin master
Digite a senha do SSH e verifique se a atualização do repositorio remoto será realizada
* $ git pull origin main (baixe a versão mais atual do repositorio remoto para o repositorio local)
* $ git status (Informará qual arquivo está desatualizado para modificação)
* $ git diff README.md (Mostrará a diferença existente entre os arquivos)
* $ git add * (Caso não seja necessário uma alteração manual faça a adição do arquivo local)
* $ git commit -m "resolver conflitos"
* $ git push origin main






