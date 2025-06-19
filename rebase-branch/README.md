# rebase branch

## Setup

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Dessa vez nós vamos mostrar como rebase de branches no Git pode parecer mais fácil do que dizem.

1. Qual branches existem? 
2. Procure no log pela master branch
3. Troque para a uppercase branch
4. Como o log se compara ao log no branch master? 
5. Rebase sua uppercase branch with a master (`git rebase master`)
6. O que aconteceu? 
7. Agora troque para a branch master
8. Merge uppercase na master
9. Como se parece o log agora?


## Comandos Úteis

- `git switch <branch-name>`
- `git rebase <branch-name>`
- `git log --oneline --graph --all`
- `git merge <branch-name>`
