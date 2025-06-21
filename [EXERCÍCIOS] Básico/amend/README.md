# Amending commits

Quando nós estamos trabalhando, nós fazemos vários commits.
Algumas vezes apenas esquecemos de algo óbvio que nós queriamos consertar rapidamente.

`git commit --amend` nos permite fazer isso - mexer no último commit que fizemos.

Você pode usar `git log -p` ou `git show` para inspecionar o conteúdo dos commits e alterações em arquivos que foram feitas nos commits adicionados.

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

1. O que `git status` nos diz?
2. O que `git log -p` nos diz?
3. Adicione bar.txt a área de preparação _(staging area)_
4. Execute `git commit --amend`
5. O que aconteceu? O que `git log -p` nos diz?
6. E se você executa-se `git commit --amend` novamente?

## Comandos Úteis

- `git add`
- `git log --oneline --graph`
- `git log -p`
- `git show`
- `git commit --amend`
