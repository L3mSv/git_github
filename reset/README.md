# Git reset

Nós podemos manipular o histórico da forma que quiesermos. Nós devemos sempre memxer com o nosso histórico local. Já que os commits devem ser imutáveis

Usamos reset para desfazer mudanças, mas também podemos fazer muitas outras coisas diferentes.

## Setup

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Task

1. Como seu diretório de trabalho parece? 
2. Como se parece o seu log? Como se parece sua área de preparação _(staging area)_? 
3. Tente executar `git reset --soft HEAD~1`
4. Como se parece seu diretório de trabalho, seu log e sua área de preparacação _(staging area)_? 
5. Execute `git reset --mixed HEAD~1`
6. Como se parece seu diretório de trabalho, seu log e sua área de preparacação _(staging area)_? 
7. Execute `git reset --hard HEAD~1`
8. Como se parece seu diretório de trabalho, seu log e sua área de preparacação _(staging area)_? 
9. Agora tente usar `git revert HEAD~1`
10. Como se parece seu diretório de trabalho, seu log e sua área de preparacação _(staging area)_? 

## Comandos Úteis

- `git log --oneline`
- `git commit --amend`
- `git status`
- `git reset --soft`
- `git reset --mixed`
- `git reset --hard`
- `git revert`

## Explicação Rápida

O seguinte foi retirado da seção Recapitulação de [https://git-scm.com/book/en/v2/Git-Tools-Reset-Demystified].
O comando reset substitui essas três árvores em uma ordem específica, parando quando você ordena:
1. Move para onde o branch HEAD aponta (parar aqui se --soft)
2. Faz a área de preparação _(staging area)_ se parecer com o HEAD (pare aqui, a menos que seja --hard)
3. Faz o diretório de trabalho se parecer com a área de preparação _(staging area)_
