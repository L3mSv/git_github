# Bad Commit

Um dos commits na `master` introduziu um arquivo defeituoso.
Encontre o commit e reverta isso usando `git bisect`.

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Use `git bisect` para encontrar o commit "ruim" e então use `git revert` para reverter isso. Quando você estiver executando `git bisect`, você precisa indicar se o "estado" do arquivo é "bom" ou "ruim" até o comando encontrar o commit que introduziu a mudança.

Para esse exercício, a versão é ruim se `badfile` existe.

1. Inicie `git bisect`.
2. Normalmente o HEAD é "ruim", como está nesse exercício. Use `git bisect bad` para indicar isso.
3. Normalmente alguma versão antiga vai ser boa. Nesse exercício, a versão inicial é. Use `git bisect good <commit -ish>` para indicar isso.
4. `git bisect` vai então verificar vários commits para encontrar o commit ruim. Continue indicando o estado até isso dizer para você o primeiro commit ruim. Mantenha o rastro desse commit.
5. Execute `git bisect reset` para que possamos trabalhar no repositório.
6. Use `git diff` para ter certeza que o commit ruim apenas introduziu `badfile`.
7. Use `git revert` para isso.

Se você tiver um script que possa dizer se o código-fonte atual é bom ou ruim, você pode dividi-lo ao meio emitindo `git bisect run`.

## Comandos Úteis

- `git bisect start`
- `git bisect bad`
- `git bisect good <commit-ish>`
- `git bisect good`
- `git bisect reset`
- `git diff <commit-ish-1> <commit-ish-2>`
- `git revert <commit-ish>`
- `git bisect run <cmd>`
- `test ! -f badfile` (ou `gci . badfile` no PowerShell) para testar a existencia de um arquivo
- `test ! -f badfile;echo $?` para mostrar a saída do resultado no console
