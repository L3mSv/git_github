# Fast-forward Merge

## Setup

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Novamente você se encontra na sua própria branch, dessa vez nós vamos mesclar um pouco diferentes branches, para te mostrar como trabalhar com diferentes branches não é tão difícil quanto parece.

1. Crie uma (feature)branch chamada `feature/uppercase` (sim, `feature/uppercase` é um nome de branch perfeitamente legal, e uma conveção comum).
2. Troque para esta branch
3. O que é a saída de `git status`? 
4. Altere o `greeting.txt` para armazenar uma saudação em letras maiúsculas
5. Adicione `greeting.txt` arquivos para a área de preparação e commit
6. Qual é a saída de `git branch`? 
7. O que é a saída de `git log --oneline --graph --all`

   *Remember: You want to update the master branch so it also has all the changes currently on the feature branch. The command 'git merge [branch name]' takes one branch as argument from which it takes changes. The branch pointed to by HEAD (currently checked out branch) is then updated to also include these changes.*

   *Lembre-se: Você quer atualizar a _master branch_ para que ele também tenha todas as alterações atuais da feature branch. O comando `git merge <branch-name>` recebe uma branch como argumento da qual irá extrair as alterações. A branch apontada pelo _HEAD_ (branch sendo trabalhada atualmente) é então atualizada para também incluir essas mudanças.*

8. Troque para a `master` branch
9. Use `cat` para ver o conteúdo de `greetings.txt`
10. Execute `git diff` entre as branches
11. Mescle as brances com `git merge`
12. Use `cat` para ver o novo conteúdo de `greetings.txt`
13. Delete a uppercase branch

## Comandos Úteis

- `git branch`
- `git branch <branch-name>`
- `git branch -d <branch-name>`
- `git switch`
- `git branch -v`
- `git add`
- `git commit`
- `git commit -m`
- `git merge <branch>`
- `git diff <branchA> <branchB>`
- `git log --oneline --graph --all`
