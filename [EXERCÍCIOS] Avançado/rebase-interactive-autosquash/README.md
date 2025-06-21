# Interactive rebase with --autosquash option

Você tem trabalhado em uma nova ferramenta chamada *Hello World*.
Essa ferramenta é finalizada com uma documentação e uma unidade teste, mas há um typo na documentação.

Você precisa consertar isso e então fazer um rebase para ter um histórico melhor.

Felizmente nós criamos uma tag `v0.0` antes mesmo de começarmos a trabalhar nessa ferramenta.

Há uma maneira simples de consertar isso com o uso de opções avançadas para `git commit` e `git rebase`.

## Setup:

1. Execute `. setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

1. Explore o repositório e o histórico para saber quando o arquivo de documentação foi adicionado.
2. Conserte o arquivo `README.md` e o adicione a área de preparação _(staging area)_.
3. Adicione seu commit usando  `git commit --fixup=<commit id a ser consertado>`.
4. Use `git rebase --autosquash --interactive v0.0` para ver a receita do rebase automaticamente gerado.

5. Use `git log` para ver o seu novo histórico.


### Comandos Úteis

- `ls -l`                           # lista de arquivos
- `tail -n +1 *`                    # mostra o conteúdo de todos os arquivos
- `git log --oneline`               # mostra o histórico
- `git log --stat`                  # log dos arquivos que foram modificados
- `git log --patch`                 # log com diff
- `git show <commit id>`            # mostra as mudanças em um commit
- `git add`                         # adiciona um arquivo
- `git commit --fixup=<commit id>`  # commit usando uma mensagem genérica
- `git rebase -i <ref>`             # Executa um rebase interativo de volta para <ref> e automaticamente reordena os commits.
