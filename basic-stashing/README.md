# Basic stashing

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Você está trabalhando no seu projeto. Você adiciona alguns arquivos e tem outros arquivos que não estão adicionados também.
De repente, você descobre que um bug chegou à produção. Você guarda seu trabalho, corrige o bug e volta ao trabalho original. 

1. Explore o repositório
   1. Quais arquivos você possui no seu diretório de trabalho?
   2. Que arquivos você adicionou a área de preparação _(staging area)_?
   3. Como o log dos commits parece?
   >*Note que file.txt tem algumas mudanças adicionadas(i.e. mudanças no index ou staging area) e mudanças não adicionadas (mudanças no diretório de trabalho)*
2. Use `git stash` para esconder o seu trabalho atual.
   1. Agora, que arquivos você tem no seu diretório de trabalho?
   2. Quais arquivos você tem adicionados?
   3. Como o log dos commits se parece?
   4. Como a lista de arquivos ocultos se parece usando `git stash --list`?
3. Conserte os typos no bug.txt na master e commit suas mudanças.
4. Agora volte para o seu trabalho, aplique o stash na master.
   1. Quais arquivos você tem no diretório de trabalho?
   2. Que arquivos você tem adicionados?
   >*Oops. Todas as nossas mudanças não estão adicionadas agora. Isso pode ser indesejado e inesperado*
5. Desfaça nossas alterações com `git reset --hard HEAD`. Este é um comando inseguro, pois removerá arquivos do seu índice e diretório de trabalho permanentemente, mas nossas alterações estão armazenadas com segurança, então está tudo bem. Revise os exercícios de [reset](reset/README.md) se não tiver certeza do que acontece aqui.
6. Aplique o stash ao master com a opção `--index`.
   1. Quais arquivos você tem no diretório de trabalho?
   2. Quais arquivos você tem adicionados?
   >*Ok, de volta para onde estavamos!*
7. Nós não precisamos do stash mais. Remova isso.
   1. Como a lista de arquivos ocultos se parece?
   2. Como o log de commits se parece?



## Comandos Úteis 

- `git status`
- `git status -s`
- `git diff`
- `git diff master`
- `git stash`
- `git stash list`
- `git stash apply`
- `git stash apply --index`
- `git stash drop`
- `git log --oneline --all --graph`
- `git commit`
- `git add`
