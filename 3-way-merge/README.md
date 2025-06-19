# 3-Way Merge

## Setup

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Você está na sua própria branch, dessa vez nós vamos usar um tipo de mesclagem específico, conhecido como merge de 3 vias ou _(3-Way Merge)_, para mostrar que o uso de mesclagem de branches não é tão difícil quando parece

1. Crie uma branch chamada greeting e troque para ela
2. Altere o conteúdo de `greeting.txt` para conter o seu tipo de saudação favorito
3. Adicione `greeting.txt` a área de preparação _(staging area)_
4. Commit
5. Volte para a branch master
6. Crie um arquivo README.md com informações sobre este repositório
7. Adicione o arquivo README.md para a área de preparação e faça o seu commit 
8. Qual é a saída de `git log --oneline --graph --all`?
9. Diff as branches
10. Merge a branch greeting na branch master

11. Qual é a saída de `git log --oneline --graph --all` agora? Observe o extra merge commit criado com a mensagem "Merge branch 'greeting'".
                                                        
## Comandos Úteis

- `git branch`
- `git branch <branch-name>`
- `git branch -d <branch-name>`
- `git switch <branch-name>`
- `git switch -c <branch-name>`
- `git branch -v`
- `git add`
- `git commit`
- `git commit -m`
- `git merge <branch-name>`
- `git diff <branchA> <branchB>`
- `git log --oneline --graph --all`
