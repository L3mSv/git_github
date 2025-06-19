# Basic cleaning

## Setup:

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa
Você está trabalhando no seu projeto que involve geração de arquivos. Digamos que você compila alguns arquivos em C em arquivos executáveis. Antes de trocar para uma nova branch você quer começar deletar esses arquivos.

1. Explore o diretório com `ls -R`. Há muita coisa acontecendo. Arquivos de código, arquivos temporários, arquivos de objeto... Vamos limpar!
2. Só por segurança, faça um teste e execute o comando `git clean` com a opção `-n`.
3. Ah, não! Há um arquivo `.c` que teria sido excluído!
4. Adicione `src/mylib.c` à área de preparação. Não o commit.
5. Execute o comando clean com a opção ` -n`. Note que mylib.c não vai ser deletada. Além disso, os arquivos no diretório obj não vão ser listados.
6. Execute o comando clean com as opções ` -n -d `.
7. Ótimo! agora limpe o repositório com ` -f -d `.

## Comandos Úteis
- `git clean -n`
- `git add`
- `git clean -n -d`
- `git clean -f -d`
