---
title: Git
subtitle: Do noob até o Wizard lv12
author: Mateus Koppe
---

# Um pouco de história

![Linus Torval criador do Git](./images/torval.jpg)

Foi criado em 2005 por Linus Torval para o versionalmento do kernel Linux e foi rapidamente adotado por outros projetos.

# Sobre a apresentação

O repositório está na URL
https://github.com/mateusKoppe/git-basic-guide

# Como instalar

## Debians based
```
sudo apt install git
```

## Red-Hat based
```
sudo dnf install git
```

## Arch based
```
sudo pacman -S git
```

## Windows
Não sei, procura lá

# Setup
```bash
git config --global user.name <name>
git config --global user.email <email>
```

# Sobre `--global`
Utilize apenas no seu computador pessoal, caso você queria definir a configuração apenas para um repositório específico use `--local` (já é o padrão)

# Criando um repositório
```bash
# Inicia um repositório vazio
git init
```

# Comandos e conceitos básicos
* git-add
* git-status
* git-commit
* git-log
* git-diff

# git-add
```bash
# Adiciona arquivos para serem trackeados
git add <files>
```

# git-status
```bash
# Recebe status do repositório, dos arquivos
git status

```

# git-diff
```bash
# Exibe as diferenças que não foram adicionadas
git diff

# Exibe as que foram adicionadas:
git diff --cached
```

# git-commit
```bash
# Cria um commit
git commit

# De forma rápida:
git commit -m "<message>"
```

# git-log
```bash
# Exibe os logs
git log

# Uma linha por log
git log --oneline
```

# Branchs
* git-branch
* git-checkout
* git-stash
* git-merge

# git-branch
```bash
# Lista as branchs criadas e exibe a brach atual
git branch

# Cria uma nova branch baseada na branch atual
git branch <name>

# Deleta uma branch
git branch -d <name>
```

# git-checkout
```bash
# Troca de branch
git checkout <name>

# Cria e troca de branch
git checkout -b <name>
```

# git-stash
```bash
# Salva as mudanças de uma branch e reseta-a
git stash

# Retorna as mudanças que foram salvas para a branch
git stash apply
```

# git-merge
```bash
# Junta os commits da branch atual com a branch alvo
git merge <name>
```

# Remote
Git não faria sentido se não ouvesse uma forma de armazenar os repositório em algum lugar onde possa ser compartilhado para outras pessoas.

Crie um repositório online

##
* git-remote
* git-push
* git-pull
* git-clone

# Criando um repositório no Github
![](./images/create-online-repo.png)

# Criando um repositório no Github
![](./images/online-repo.png)

# git-remote
```bash
# Lista os repositórios adicionados
git remote

# Adiciona um repositório remoto
git remote add <name> <url>

# Por convenção o repositório principal geralmente
# é nomeado como origin
git remote add origin <url>
```

# git-push
```bash
# Push = Empurra
# Envia os commits da branch selecionada
# para o remote selecionado
git push <remote> <branch>

# O mais comum é
git push origin master
```

# git-pull
```bash
# Pull = Puxa
# Atualiza a branch selecionada de acordo com o
# remote selecionado
git pull <remote> <branch>
```

# git-clone
```bash
# Clona um repositório online
git clone <url> [<folder>]
```

# Gitignore
Caso seja necessário que o repositório ignore algum arquivo ou algumas pasta é possível criar um `.gitignore`, nele você insere quais arquivos deverão ser ignoradas no repositório.

# Variável HEAD
Reflete o branch e commit atual.
Você também pode utilizar `~<n>` para referenciar commits anteriores.

```
# Macetes
git push origin HEAD

git reset --head HEAD~1
```
