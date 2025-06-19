# Reordenando o Histórico

## Setup

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Os commits aqui foram obviamente feitos por um cara de mal humor.
Infelizmente, eles estão contendo informações úteis - pórem o histórico está com um aspecto estranho.
Você deve consertar isso de tal forma que nosso `git log` pareça bom!

Reordene o histórico de uma maneira que faça sentido - adicione os arquivos na ordem que combine com seus nomes

1. Use `git log --oneline --graph` para ver os commits 
2. Também tente `git reflog` para ver os commits. `git reflog` padrão  para `git reflog show` and isso é um alias para `git log -g --abbrev-commit --pretty=oneline`
3. Use `git rebase -i <after-this-commit>` para reordenar os commits. 
Há comentários nos arquivos que você pode editar para explicarem os comandos disponíveis
4. Use `git log --oneline --graph` para ver os resultados

### Comandos Úteis

- `git rebase -i <after-this-commit>`
- `git log --oneline --graph`
- `git reflog`
