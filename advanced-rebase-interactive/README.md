# Advanced interactive rebase

Você tem trabalhado em uma ferramenta chamada *Hello World*.
No fim, a ferramenta foi finalizada, com documentação e testes de unidades, mas restaram alguns problemas.
O histórico ficou bastante bagunçado, com várias etapas deixadas pela metade e coisas inclusas que nem deveriam estar ali.

Você deve consertar isso, de forma que o seu `git log` parece incrível!

Para fazer isso vamos usar nosso velho amigo `git rebase --interactive`

Felizmente nós usamos uma tag `v0.0` antes mesmo de começarmos a construir a ferramenta.

Nesse exercício de nível avançado, não há passos específicos para seguir e não existe uma única solução.

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

1. Explore o repositório e o histórico para saber o que aconteceu
2. Use `git rebase --interactive v0.0` para deixar você editar a "receita" para o desenvolvimento inteiro da ferramenta
3. Limpe o histórico de forma que faça sentido. Tente usar quantos rebases "ferramentas" (e.g. reword, squash, fixup, drop) for possível. Você decide se você quer rescrever por inteiro de uma só vez, ou aplicar algumas mudanças primeiro, e então executar um novo `git rebase --interactive v0.0` para manter limpo. 

### Comandos Úteis

- `ls -l`                 # lista de arquivos
- `tail -n +1 *`          # mostra o conteúdo de todos os arquivos
- `git log --oneline`     # mostra o histórico
- `git log --stat`        # mostra o log de quais arquivos foram alterados
- `git log --patch`       # log com diff
- `git rebase -i <ref>`  # executa um rebase interativo de volta pra <ref>
