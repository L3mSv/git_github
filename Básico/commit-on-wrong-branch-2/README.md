# Commit on wrong branch II

## Setup:

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## Tarefa

Você desenvolve uma nova funcionalidade na branch `new-feature`. Você já implementou a primeira parte de uma funcionalidade quando é notificado sobre um bug crítico que precisa ser corrigido imediatamente na branch `master`.

Após a correção do bug, você continua trabalhando na nova funcionalidade. Após fazer o commit da segunda parte da funcionalidade, você percebe que fez o commit na branch `master` em vez da branch da funcionalidade.

1. Mova o commit defeituoso da ramificação `master` para a ramificação `new-feature`.
2. Como você faria para trazer a correção de bug para sua feature branch?


## Comandos Úteis

* `git reset HEAD~1` para mover o branch atual um passo para trás. Isso tem como consequência _remover_ o commit mais recente de um branch
* `git stash` para temporariamente salvar suas mudanças para que você possa trocar entre suas branches
* `git cherry-pick` para adicionar o conjunto de mudanças do commit para sua branch atual
