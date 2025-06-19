# Basic revert
## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Nesta tarefa, algumas alterações foram introduzidas e gostaríamos de removê-las. Nosso histórico é público, então não podemos simplesmente alterá-lo. Em vez disso, precisamos usar a função "reverter" para remover as alterações indesejadas de forma segura.

1.  Use `git log --oneline` para dar uma olhada no histórico
2.  Use `cat` para ver o conteúdo de `greeting.txt`
3.  Use `git revert` no mais novo commit, para reverter as mudanças adicionadas pelo último commit
4.  Use `git log --oneline` para ver o histórico
5.  O `git revert` adicionou ou removeu o commit? 
6.  Use `cat` para ver o conteúdo de `greeting.txt`
7.  Use `ls` para ver o conteúdo do diretório de trabalho
8.  Use `git log --oneline` para encontrar o SHA do commit adicionando credenciais para o repositório
9.  Use `git revert` para reverter o commit que adicionou credenciais ao repositório
10. Use `git log --oneline` para ver o histórico
11. Use `ls` para ver o conteúdo do diretório de trabalho
12. Quantos commits foram adicionados ou alterados pelo último revert? 
13. Use `git show` com o SHA do commit que você reverteu para ver  que aquele  arquivo das credenciais ainda está no histórico
14. Você reverteu o arquivo das credenciais, então ele foi removido do seu diretório de trabalho, mas isso também removeu ele do seu git? 

## Comandos Úteis
- `git revert <ref>`
- `git log --oneline`
- `git show <ref>`
