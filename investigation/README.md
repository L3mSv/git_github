# Git objects

Objetos são armazenados em `<repository>/.git/objects` uma subpasta juntando os dois primeiros caracteres do SHA-1 de 40 caracteres *(Identificador completo de um objeto GIT)*.
`fc1da6e8f` portanto é o arquivo: `.git/objects/fc/1da6e8f`.

`git cat-file` mostra o conteúdo de qualquer que seja o _ref_ que você passar.
 
Usando `-p` como parâmetro para `cat-file` imprime o conteúdo de um objeto.

Usando `-t` como parâmetro para `cat-file` mostra o autor de um objeto.

`git ls-tree master ` lista o conteúdo de uma pasta.

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

1. Usando `git ls-tree` e `git cat-file`, desenhe a estrutura pastas inteira do GIT.
	- O que tree e blob objects são e o que eles apontam?
	- Que commits apontam para dentro desse gráfico e aonde?	