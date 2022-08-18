# Git cheatsheet
### Configurar as informações do usuário
```console
git config --global user.name "nome do usuário"
```
```console
git config --global user.email usuario@email.com
```
### Criar um repositório no diretório atual
```console
git init
```
iniciar um servidor git
```console
git init --bare
```
### Verificar o estado do repositório
```console
git status
```
### Adicionar arquivos para serem *commitados*
```console
git add <file.ext>
```
adicionar todos os arquivos
```console
git add .
```
### *Commitar* arquivos
```console
git commit -m "Mensagem de commit"
```
### Verificar o histórico de *commits*
```console
git log
```
```console
git log --oneline
```
exibir as alterações efetuadas nos *commits*
```console
git log -p
```
### Trabalhar com repositórios remotos
```console
git remote add <nome-do-repositorio> caminho/para/o/repositorio
```
```console
git remote rename antigo novo
```
### Baixar um repositório
```console
git clone caminho/para/o/repositorio <diretorio>
```
### Enviar alterações para um repositório remoto
```console
git push [<nome-do-repositorio>] [branch]
```
### Atualizar arquivos locais com os dados do repositório remoto
```console
git pull [<nome-do-repositorio>] [branch]
```
