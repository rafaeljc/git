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
git add <arquivo.ext>
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
exibir as linhas de desenvolvimento (*branchs*)
```console
git log --graph
```
exibir os n últimos
```console
git log -n <número>
```
### Trabalhar com repositórios remotos
```console
git remote add <nome-do-repositorio> caminho/para/o/repositorio
```
listar os repositórios remotos
```console
git remote -v
```
```console
git remote rename <antigo> <novo>
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
### Exibir os *branchs* do repositório
```console
git branch
```
### Criar um novo *branch*
```console
git branch <nome-do-branch>
```
### Mudar de *branch*
```console
git checkout <nome-do-branch>
```
criar um novo *branch* e mudar para ele em seguida
```console
git checkout -b <nome-do-branch>
```
### Juntar um *branch* **ao atual** (gerando um *commit* de *merge*)
```console
git merge <nome-do-branch>
```
### Juntar um *branch* **ao atual** (**sem** gerar um *commit* de *merge*)
```console
git rebase <nome-do-branch>
```
### Desfazer alterações
reverter alterações que **ainda não foram adicionadas ao *stage***
```console
git checkout -- <arquivo.ext>
```
remover alterações do ***stage***
```console
git reset HEAD <arquivo.ext>
```
reverter alterações que **já foram *commitadas***
```console
git revert <hash>
```
### Salvar alterações (sem *commitar*) para serem trabalhadas depois
```console
git stash
```
### Retornar ao trabalho de onde parou
listar as alterações que estão salvas na *stash*
```console
git stash list
```
aplicar uma alteração em específico que está salva na *stash*
```console
git stash apply <índice>
```
remover da *stash* determinada alteração
```console
git stash drop <índice>
```
recuperar a **última** alteração salva na *stash* e removê-la da lista
```console
git stash pop
```
### Exibir mudanças efetuadas
mudanças que ainda não estão no *stage*
```console
git diff
```
mudanças realizadas entre dois *commits*
```console
git diff <hash-commit-inicial>..<hash-commit-final>
```
### Criar uma tag/release
```console
git tag -a <versão> -m "Mensagem descritiva"
```
```console
git push [repositório] <versão>
```
