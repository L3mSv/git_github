# Merge Mergesort
Neste diretório você vai encarar seu primeiro conflito de merge!
Existem duas branches diferentes: 

* Mergesort-Impl
* master

A tarefa é análisar o conflito de merge, e editar o arquivo para resolver.

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

1. Execute `git branch` para ver as duas branches da tarefa
2. Merge `Mergesort-Impl` em `master`
3. Em seguida edite o arquivo de uma forma ou de outra:
   1. Resolva o conflito de merge com seu editor favorito e termine a mesclagem (`git status` vai dizer o que tem que fazer), **ou** 
   2. Use `git mergetool --tool=emerge` (para emacs fans) ou `git mergetool --tool=vimdiff` (para vim fans) e termine o merge (`git status` vai dizer o que tem que fazer)

## Comandos Úteis
- `git branch`
- `git merge`
- `git status`
- `git mergetool --tool=emerge`
- `git mergetool --tool=vimdiff`
- `git add`
- `git commit`

