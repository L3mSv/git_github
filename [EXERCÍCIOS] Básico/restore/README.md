# Restoring files

Todos cometemos erros. Às vezes, fazemos alterações que preferiríamos não ter feito ou, acidentalmente, preparamos alterações que não pretendíamos.
É aqui que o `git restore` entra em ação.

## Setup

1. Execute `source setup.sh` (ou `.\setup.ps1` no PowerShell)

## Tarefa

1. Execute `git status`\
 Que mudanças foram feitas no repositório?
2. Restaure o arquivo `foo.txt` usando  `git restore foo.txt`
3. Execute `git status` novamente\
 O que aconteceu com `foo.txt`?
4. Desfaça as mudanças do `bar.txt` usando `git restore --staged bar.txt`
5. Execute `git status` mais uma vez\
 O que aconteceu com `bar.txt`?
6. Restaure o arquivo `bar.txt` usando `git restore bar.txt`
7. Execute `git status` mais uma vez\
 O que aconteceu com `bar.txt`?
8. Execute `git log --oneline`\
Você viu a tag?
9. Restaure o conteúdo de `foo.txt` para sua última versão usando `git restore -s v1.0.0 foo.txt`
10. Execute `git status` mais uma última vez\
 O que aconteceu com `foo.txt`?

## Comandos Úteis

- `git status`
- `git log --oneline`
- `git restore`
- `git restore --staged`
