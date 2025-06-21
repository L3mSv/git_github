# Basic Staging

Este diretório vai examinar a área de preparação do git _(staging area)_.

No git nós temos 3 diferentes áreas de trabalho:

* O diretório de trabalho, onde você faz as suas mudanças.
* A área de preparação _(staging area)_, onde todas as mudanças adicionadas por você através do `git add` vão ficar.
* O repositório, onde todo commit termina, construindo seu histórico. Para subir as suas mudanças da área de preparação _(staging area)_ você deve executar o comando `git commit`. 


O arquivo pode ter mudanças no diretório de trabalho e na área de preparação ao mesmo tempo.
Essas mudanças não precisam ser as mesmas.

Nós também vamos trabalhar com `git restore` para restaurar mudanças da área de preparação do arquivo, e `git checkout` para retornar um arquivo ao seu estado anterior.

## Setup

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

Você está no seu próprio repositório. Nele existe um arquivo chamado `file.txt`

1. Qual é o conteúdo de `file.txt`?
2. Sobrescreva o conteúdo de `file.txt`: `echo 2 > file.txt` para mudar o estado do seu arquivo no diretório de trabalho <br/>(ou `sc file.txt '2'` no PowerShell)
3. O que `git diff` diz a você?
4. O que `git diff --staged` diz a você? porque isto está em branco?
5. Execute `git add file.txt` para mover as suas mudanças do diretório de trabalho para a área de preparação
6. O que `git diff` diz a você?
7. O que `git diff --staged` diz a você?
8. Sobrescreva o conteúdo do `file.txt`: `echo 3 > file.txt` para mudar o estado do seu arquivo no diretório de trabalho <br/>(or `sc file.txt '3'` no PowerShell)
9. O que `git diff` diz a você?
10. O que `git diff --staged` diz a você?
11. Explique o que está acontecendo 
12. Execute `git status` e observe que `file.txt` está presente duas vezes na saída.
13. Execute `git restore --staged file.txt` para desfazer as mudanças 
14. O que `git status` diz a você agora? 
15. Execute `git add` e faça um commit
16. Como `git log` se parece? 
17. Sobrescreva o conteúdo no `file.txt`: `echo 4 > file.txt` (ou `sc file.txt '4'` no PowerShell)
18. Qual é o conteúdo de `file.txt`?
19. O que `git status` nos diz? 
20. Execute `git restore file.txt`
21. Qual é o conteúdo de `file.txt`?
22. O que `git status` nos diz?

## Comandos Úteis

- `git add`
- `git commit`
- `git commit -m "Minha preguiçosa e curta mensagem de commit"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `git restore --staged`

## Aliases (Apelidos)

Você pode configurar aliases tais como:
`git config --global alias.lol 'log --oneline --graph --all'`
Que podem ser úteis para você.

>[!NOTE]
>Um aliase é como configurar um apelido para um comando ser chamado, no exemplo acima
>ao invés de digitar `git log --oneline --graph --all` eu apenas escrevo `git lol` e 
>recebo a mesma saída em ambos os casos, a diferença é que `git lol` é mais simples.