# Commit on wrong branch

## Setup

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## Tarefa

Você está trabalhando muito duro no branch master.
Parte do seu trabalho já está comprometida. É quando seu chefe entra com uma solicitação urgente.

Como seu HEAD atual não está pronto para o horário nobre, você faz backup de um commit e inicia uma nova branch chamada "quickfix". Você faz o que seu chefe quiser e envia as alterações para essa nova branch.

É aí que você percebe que fez uma pequena bagunça com suas branches.

Atualmente, seus commits estão assim:

```text
         master
           |
           v
   A <---- B
   ^ \
   |  \--- C
remote     ^
           |
        quickfix
```

Mas você quer que fique assim:

```text
         remote
           |
           v
   A <---- C <---- B
                   ^
                   |
                  HEAD
```

Vá em frente!

Observação: como o `B` na estrutura atual e na estrutura de destino não têm o mesmo pai, eles não podem ser literalmente o mesmo commit.

1. Use `git log --oneline --graph --all` para ver todas as branches e seus commits.
2. Copie `C` para `master` antes `B` por rebase `quickfix` no `master`.
3. Faça uma nova branch (`changes-including-B`) fora da sua `master` então nós podemos voltar a trabalhar na `B`.
4. Reset `master` de volta para `C`.
5. Delete a branch `quickfix`.
6. Push `master`. Você não pode fazer isso no exercício de treinamento.
7. Você pode mesclar a branch `changes-including-B` para `master` e delete `changes-including-B` ou apenas troque para `changes-including-B` e trabalhe lá.

## Comandos Úteis

- `git log --oneline --graph --all`
- `git switch <branch-name>`
- `git rebase <branch-name>`
- `git branch <branch-name>`
- `git reset --soft HEAD~`
- `git branch -d <branch-name>`
- `git merge <branch-name>`
