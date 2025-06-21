# Git objects

Objetos são armazenados em `<repository>/.git/objects` uma subpasta juntando os dois primeiros caracteres do SHA-1 de 40 caracteres *(Identificador completo de um objeto GIT)*.
`fc1da6e8f` portanto é o arquivo: `.git/objects/fc/1da6e8f`.

Os objetos em Git podem ser um dos 3 tipos abaixo:
* `blob` : *conteúdo puro de um arquivo*, sem nome nem estrutura de caminho
* `commit` : aponta para um `tree` (raiz do projeto naquele ponto do tempo)
* `tree` : representa um *diretório*, contém entradas com nome, permissões e SHA do que está dentro (outros `tree`s ou `blob`s)

`git cat-file` mostra o conteúdo de qualquer que seja o _ref_ que você passar.
 
Usando `-p` como parâmetro para `git cat-file` imprime o conteúdo de um objeto.

Usando `-t` como parâmetro para `git cat-file` mostra o autor de um objeto.

`git ls-tree master ` lista o conteúdo de uma pasta.

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

1. Usando `git ls-tree` e `git cat-file`, desenhe a estrutura de pastas inteira do GIT.
	- O que tree e blob objects são e o que eles apontam?
	- Que commits apontam para dentro desse gráfico e aonde?	

## Comandos Úteis
* `git ls-tree <SHA_da_tree>`
* `git cat-file <SHA_do_commit>`
* `git rev-parse HEAD` _--Retorna o SHA do commit atual_
* `git ls-tree -r HEAD` _--Faz uma travessia recursiva da árvore e mostra todos os arquivos em todos os diretórios_