# Tutorial do git

## Git

Sistema de controle de versões, facilita o trabalho em em equipe e o controle de mudanças entre arquivos e diretórios.

## Clonar o repositório
- Acessar o link: https://github.com/OPE-IMPACTA/DOCS
- Executar o comando `git clone https://github.com/OPE-IMPACTA/DOCS` no terminal dentro do diretório que deseja clonar o projetos

## Branch

Uma das principais vantagens do git é a possibilidade de criarmos `ramificações`, assim podemos trabalhar em funcionalidades adicionais para um projeto, sem modificarmos o `ramificação principal`, o master.

Toda vez que formos adicionar uma nova funcionalidade, devemos iniciar criando um novo branch ao invés de fazermos alterações direto no master. O que for modificado no branch não afetara o master.

Comandos do git
- `git config --global user.name "seu nome"` configurar nome
- `git config --global user.email "email@email.com"` configurar email
- `git init` inicia um repositório
- `git remote add origin link-do-repositorio` Adicionar diretório remoto
- `git push -u origin master` push do primeiro commit
- `git branch` para verificar as branchs locais
- `git branch nome-branch` Cria um novo branch
- `git branch -a` para verificar os branchs locais e remotas
- `git branch -d nome-do-branch` deleta o branch local
- `git checkout nome-da-branch` para mudar de branch
- `git checkout -b nome-da-branch` atalho para criar um novo branch e mudar automáticamente
- `git checkout nome-do-arquivo` desfaz as alterações feitas no arquivo
- `git checkout .` defaz todas as alterações feitas nos arquivos
- `git status` para verificar os arquivos modificados
- `git add nome-do-arquivo` para adicionar um arquivo modificado
- `git add .` para adicionar todos os arquivos modificados
- `git commit -m "comentarios"` para descrever o commit
- `git push origin nome-da-branch` para subir o arquivo
- `git pull origin nome-da-branch` para atualizar o arquivo
- `.gitignore` lista de arquivos que não devem ser manipulados pelo git
