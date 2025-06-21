# Basic Commits
Este diretório vai introduzir você ao `git add` e ao `git commit` comandos.

Isto é um diretório muito introdutório. Se você tem usado `git status`, `git log --oneline --graph`, `git add` e `git commit` extensivamente, então provavelmente você deveria pular este diretório.

Você pode olhar no rodapé deste arquivo, se você ainda não configurou a configuração básica de git.

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

1. Use `git status` para ver em qual branch você está.
2. Ao executar `git log` o que aparece?
3. Crie um arquivo
4. O que aparece na saída de `git status` agora?
5. `add` o arquivo para a área de preparação 
6. Como parece `git status` agora?
7. `commit` o arquivo para o repositório
8. Como parece `git status` agora?
9. Mude o conteúdo do arquivo que você criou mais cedo
10. Como parece `git status` agora?
11. `add` as mudanças do arquivo
12. Como parece `git status` agora?
13. Altere o arquivo novamente
14. Faça um `commit`
15. Como parece `git status` agora? O `log`?
16. Adicione e commit a mais nova mudança

## Comandos Úteis
- `git add`
- `git commit`
- `git commit -m "My commit message"`
- `git log`
- `git log -n 5` --Mostra os últimos 5 commits a partir do mais novo
- `git log --oneline`
- `git log --oneline --graph`
- `touch filename` para criar um arquivo (ou `sc filename ''` no PowerShell)
- `echo content > file` para sobrescrever o conteúdo de um arquivo (ou `sc filename 'content'` no PowerShell)
- `echo content >> file` para anexar o conteúdo no arquivo (ou `ac filename 'content'` no PowerShell)


## Configuração inicial do Git
1. `git config --global user.name "John Doe"`
1. `git config --global user.email "johndoe@example.com`

Para os traumatizados com vim:
- `git config --global core.editor nano`

Para os usuários de windows:
- `git config --global core.editor notepad`

Outras opcões de editores:
- `git config --global core.editor "atom --wait"` --Atom
- `git config --global core.editor "code --wait"` --VScode
- `git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst"` --Notepad++
