# Basic Branching

## Setup

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Você novamente vive somente na sua própria branch, nesse momento nós vamos fazer um pouco de malabarismo com branches, para te mostrar o quão simples é o manuseio de branches no git.
Dica: `git switch` auxilia na troca entre branches.

1. Use `git branch` para ver as duas branches que são relevantes para este exercício
2. Em que branch você está?
3. Use `git branch mybranch` para criar uma nova branch chamada _mybranch_
4. Use `git branch` novamente para ver a nova branch criada.
5. Use `git switch mybranch` para trocar para a sua nova branch.
6. Como fica a saída do `git status` alterado quando você troca entre a _master_ e a nova branch que você criou?
7. Como fica as mudanças no diretório de trabalho quando você muda entre as duas branches?
8. Tenha certeza que você está na sua _mybranch_ branch antes de continuar.
9. Crie um arquivo chamado `file1.txt` com seu nome.
10. `Add` o arquivo e `commit` com essa mudança.
11. Use `git log --oneline --graph` para ver sua branch apontando para o novo commit.
12. Troque de volta para a branch chamada _master_.
13. Use `git log --oneline --graph` e revise como o commit que você fez na  _mybranch_ branch está faltando na _master_ branch.
14. Crie um novo arquivo chamado `file2.txt` e commit esse arquivo.
15. Use `git log --oneline --graph --all` para ver sua branch apontando para o novo commit, e agora as duas branches possuem diferentes commits nelas.
16. Troque para a sua branch _mybranch_.
17. O que aconteceu no seu diretório de trabalho? Você consegue ver o seu `file2.txt`?
18. Use `git diff mybranch master` ou `git diff mybranch main` para ver as diferenças entre as duas branches.

## Comandos Úteis

- `git switch`
- `git switch -c`
- `git log --oneline --graph`
- `git branch`
- `git diff`
- `git checkout`
