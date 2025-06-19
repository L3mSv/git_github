# Página de Material de Git e Github

![README](https://github.com/user-attachments/assets/49331e55-72dc-4dfc-aa6e-13356b032866)

## Introdução 

> [!NOTE]
> Primeiramente, quero agradecer a **eficode-academy** que por meio do seu repositório [git-katas](https://github.com/eficode-academy/git-katas.git) e suas ferramentas me mostrou uma maneira simples de estruturar exercícios sobre git e github para o meu mini-curso. 

Este repositório é uma coleção de exercícios de Git e exercícios exemplo de aulas.

Os exercícios são designados para serem usados quando nós estamos ensinando cursos sobre Git. Você deveria ser capaz de usar eles como exercícios independentes que vão permiter que você mantenha suas habilidades de Git afiadas.

Exercícios começando com _básico_ são relativamente fáceis - outros exercícios são maiores em dificuldade.

Para ter uma visão geral dos exercícios deste repositório, veja [Overview.md](Overview.md).

Sinta-se livre para usar esses exercícios, essa é a razão deles serem públicos!

## Testando

Há um teste muito pequeno que você pode executar em um powershell ou bash.
Ele está contido nos scripts `test.sh` and `test.ps1`.

## Erros Comuns 

### Powershell bloqueando Scripts
>Caso você esteja usando o Powershell e ao executar `.\setup.ps1` receba este erro:
>
>``` powershell
>PS D:\git_github\git_github\basic-staging> .\setup.ps1    
>.\setup.ps1 : O arquivo D:\git_github\git_github\basic-staging\setup.ps1 não pode ser carregado porque a execução de scripts foi desabilitada neste sistema. Para obter       
>mais informações, consulte about_Execution_Policies em https://go.microsoft.com/fwlink/?LinkID=135170.
>No linha:1 caractere:1
>+ .\setup.ps1
>+ ~~~~~~~~~~~
>    + CategoryInfo          : ErrodeSegurança: (:) [], PSSecurityException
>    + FullyQualifiedErrorId : UnauthorizedAccess
>```
>Siga estes passos:
>1. Execute o seu PowerShell como Administrador
>2. Digite o comando `Set-ExecutionPolicy` RemoteSigned
>3. Digite *a* ou *s*, e logo em seguida *Enter* neste formato de pergunta:
>
>``` powershell
>A política de execução ajuda a proteger contra scripts não confiáveis. A alteração da política de execução pode
>implicar exposição aos riscos de segurança descritos no tópico da ajuda about_Execution_Policies em
>https://go.microsoft.com/fwlink/?LinkID=135170. Deseja alterar a política de execução?
>[S] Sim  [A] Sim para Todos  [N] Não  [T] Não para Todos  [U] Suspender  [?] Ajuda (o padrão é "N"): s
>PS C:\Windows\system32> cd D:\git_github\git_github\basic-staging
>```

## Caminho de Aprendizado Sugestionado

Se você está chegando de paraquedas nesse repositório, em busca de algum conhecimento básico de Git, é recomendável seguir através dessa ordem de exercícios.<br/><br/>
Esta ordem de exercícios é a mais seguida atualmente mas pode mudar com o tempo ou por opinião do programador, Podem parecer poucos exercícios mas eles devem ensinar tudo que você precisa para ser capaz de usar o Git eficientemente no seu dia a dia.<br/>

- [Basic Commits](./basic-commits/README.md)
- [Basic Staging](./basic-staging/README.md)
- [Investigation](./investigation/README.md)
- [Basic Branching](./basic-branching/README.md)
- [Fast Forward Merge](./ff-merge/README.md)
- [3 way Merge](./3-way-merge/README.md)
- [Merge Mergesort](./merge-mergesort/README.md)
- [Rebase Branch](./rebase-branch/README.md)
- [Basic Revert](./basic-revert/README.md)
- [Reset](./reset/README.md)
- [Basic Cleaning](./basic-cleaning/README.md)
- [Amend](./amend/README.md)
- [Reorder the History](./reorder-the-history/README.md)
- [Advanced Rebase Interactive](./advanced-rebase-interactive/README.md)
- [Rebase using autosquash](./rebase-interactive-autosquash/README.md)
- [Basic Stashing](./basic-stashing/README.md)

Visite [Overview.md](Overview.md) para uma lista mais completa e sugestões.

## Contribuição 

Se você encontrar erros ou sentir falta de um exercício específico, sinta-se livre para melhorar eles e fazer um **pull request**.

Você também pode fazer um **issue**, para expôr uma oportunidade de melhora!

Obrigado!

## Folha de colas

Uma coleção de comandos úteis para usar nos exercícios:

```shell
# Initializing an empty git repository.
git init            # Initialize an empty git repository under current directory.

# Cloning a repository
git clone https://github.com/praqma-training/git-katas.git      # Clone this repository to your current working directory

# Git (user and repo level) configurations
git config --local user.name "Repo-level Username"          # For setting a local git repo level user name.
git config --local user.email "Repo-level.Email@Example.com" # For setting a local git repo level user email.
                                                            # --global -> User level git config stored in <user-home>/.gitconfig for e.g. ~/.gitconfig
                                                            # --local -> repo level config stored in repo's main dir under .git/config


# See local changes
git status                  # Show the working tree status
git diff                    # Show changes current working directory (not yet staged)
git diff --cached           # Show changes currently staged for commit

# Add files to staging (before a commit)
git add myfile.txt          # Add myfile.txt to stage
git add .                   # Add entire working directory to stage

# Make a commit
git commit                              # Make a new commit with the changes in your staging area. This will open an editor for a commit message.
git commit -m "I love documentation"    # Make a new commit with a commit message from the command line
git commit -a                           # Make a new commit and automatically "add" changes from all known files
git commit -am "I still do!"            # A combination of the above
git commit --amend                      # Re-do the commit message of the previous commit (don't do this after pushing!)
                                        #   We _never_ change "public history"
git reset <file>                        # Unstage a staged file leaving in working directory without losing any changes.
git reset --soft [commit_hash]          # resets the current branch to <commit>. Does not touch the staging area or the working tree at all.
                                        # --hard mode would discard all changes.

# Configuring a different editor
## Avoid Vim but stay in terminal:
- `git config --global core.editor nano`

## For Windows:
- Use Notepad:
`git config --global core.editor notepad`

- or for instance Notepad++:
`git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin"`


# See history
git log             # Show commit logs
git log --oneline   # Formats commits to a single line (shorthand for --pretty=oneline  --abbrev-commit )
git log --graph     # Show a graph commits and branches
git log --pretty=fuller     # To see commit log details with author and committer details, if any different.
git log --follow <file>     # List the history of a file beyond renames
git log branch2..branch1    # Show commits reachable from branch1 but not from branch2

# Deferring
git stash                               # Stash (store temporarily) changes in working branch and enable checkingout a new branch
git stash list                          # List stored stashes.
git stash apply <stash>                 # Apply given <stash>, or if none given the latest from stash list.


# Working with Branches
git branch my-branch       # Create a new branch called my-branch
git switch my-branch     # Switch to a different branch to work on it
git switch -c my-branch  # Create a new branch called my-branch AND switch to it
git branch -d my-branch    # Delete branch my-branch that has been merged with master
git branch -D my-branch    # Forcefully delete a branch my-branch that hasn't been merged to master

# Merging
git merge master         # Merge the master branch into your currently checked out branch.
git rebase master        # Rebase current branch on top of master branch

# Working with Remotes
git remote              # Show your current remotes
git remote -v           # Show your current remotes and their URLs
git push                # Publish your commits to the upstream master of your currently checked out branch
git push -u origin my-branch  # Push newly created branch to remote repo setting up to track remote branch from origin.
                              # No need to specify remote branch name, for e.g., when doing a 'git pull' on that branch.
git pull                # Pull changes from the remote to your currently checked out branch

# Re/moving files under version control
git rm <path/to/the/file>                 # remove file and stage the change to be committed.
git mv <source/file> <destination/file>   # move/rename file and stage the change to be committed.

# Aliases - it's possible to make aliases of frequently used commands
#   This is often done to make a command shorter, or to add default flags

# Adding a shorthand "sw" for "switch"
git config --global alias.sw "switch"
# Usage:
git sw master     # Does a "git switch master"

## Logging
git log --graph --oneline --all # Show a nice graph of the previous commits
## Adding an alias called "lol" (log oneline..) that shows the above
git config --global alias.lol "log --graph --oneline --all"
## Using the alias
git lol     # Does a "git log --graph --oneline --all"
```

### Limpeza

Você pode remover arquivos de teste, `exercise` diretórios, com o git clean command: 

```sh
git clean -ffdX
```
