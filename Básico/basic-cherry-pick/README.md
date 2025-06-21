# Basic Cherry Pick

Nessa tarefa nós queremos ter duas branches, master e feature. Nós temos trabalhado e progredido em ambas as branches separadamente. No entanto, há algumas mudanças na feature branch que nós queremos tirar e adicionar na master branch. Sem pegar o conjunto de mudanças por inteiro da feature branch.

Git tem uma funcionalidade para isso "pegue-apenas-essas-mudanças" e isso é chamado de `cherry-pick`.

Você diz ao Git com quais commits você gostaria realizar o `cherry pick` e o Git vai adicionar esses commits no histório de commits da sua branch.

O Git pode realizar o `cherry pick` ou em um único commit ou em um conjunto de commits da branch.

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Nós atualmente temos esse histórico do git no nosso repositório de exercício: 

    A - B - C - D         master
          \
            E - F - G - H feature

Como você pode ver a `feature` branch e a `master`branch tem progredido com diferentes commits. Nós queremos realizar o *cherry pick* nos commits F e G e adicionar eles na master branch, isso fará com que o nosso histórico do Git se pareça assim: 

    A - B - C - D - F - G master
          \
            E - F - G - H feature

1. Use `git log --oneline --graph --all` para dar uma olhada no histórico.
2. Use `cat` para ver o conteúdo de `names.txt`. Esse arquivo foi alterado no commit F.
3. Use `cat` para ver o conteúdo de `sentence.txt`. Esse arquivo foi alterado no commit G.
4. Use `git cherry-pick <commit_hash_F>` para realizar o *cherry pick* apenas no commit F na sua branch
5. Use `git log --oneline` para ver as mudanças no histórico e aquele commit commit F deveria ser agora o mais novo commit na master branch
6. Use `cat` para ver o conteúdo de `names.txt` olhe agro que está modificado!
7. Use `git reset --hard HEAD^` para excluir aquele *cherry picking* a partir do histórico para que possamos tentar novamente e selecionar uma série de commits
8. Use `git log --oneline --graph` para verificar se o commit selecionado foi removido do branch
9. Agora estamos essencialmente de volta ao ponto de partida. Agora, use `git cherry-pick <commit_hash_F>^..<commit_hash_G>` para selecionar o intervalo de commits de F a G (os dois commits). Preste bastante atenção e não se esqueça do símbolo `^` após o hash do primeiro commit (consulte a seção *Nota Útil* abaixo para entender por que isso é necessário).
10. Use `git log --oneline --graph` para ver o histórico
11. Use `cat` para ver o conteúdo de `names.txt` e `sentence.txt` olhe agora que eles foram modificados!
12. Quantos commits foram adicionados devido ao *cherry pick*?


## Nota Útil

Ao usar um intervalo de commits com o comando `cherry pick`, o primeiro hash de commit especificado para o mais antigo (lado esquerdo do intervalo) não é incluído no `cherry pick`, ou seja, esse commit é excluído, mas todos os outros entre e incluindo o commit mais recente são.

Portanto, para contornar esse problema, é útil usar o simbolo `^` após o primeiro hash de commit para informar ao Git que você deseja o commit ANTES deste commit, incluindo-o no processo de cherry pick.

Por exemplo

    git cherry-pick ABCD..EFGH

não incluiria o commit ABCD, em vez disso você deve adicionar um símbolo de circunflexo `^` ao final do ABCD para dizer ao git para incluí-lo, assim:

    git cherry-pick ABCD^..EFGH

Referência: https://www.tollmanz.com/git-cherry-pick-range/
Referência: https://git-scm.com/docs/git-cherry-pick

## Comandos Úteis
- `git cherry-pick <ref>`
- `git reset --hard <ref>`
- `git log --oneline --graph --all`
