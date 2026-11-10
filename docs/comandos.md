# Comandos essenciais de Git

Referência rápida dos comandos praticados no curso, organizada por etapa do fluxo.

## 1. Ciclo de vida local

| Comando | O que faz |
|:--|:--|
| `git init` | Cria um repositório na pasta atual |
| `git status` | Mostra o estado dos arquivos (não rastreado, modificado, staged) |
| `git add <arquivo>` | Prepara a mudança para o próximo commit (`git add .` prepara tudo) |
| `git commit -m "feat: mensagem"` | Grava um snapshot com mensagem no padrão Conventional Commits |
| `git diff` | Mostra mudanças ainda não preparadas |
| `git diff --staged` | Mostra mudanças já preparadas para o commit |
| `git log --oneline --graph` | Mostra o histórico resumido, em formato de grafo |

Arquivos que não devem ser versionados (logs, pastas de editor) são listados no `.gitignore`.

## 2. Desfazendo erros

| Situação | Comando |
|:--|:--|
| Descartar alterações ainda não preparadas em um arquivo | `git restore <arquivo>` |
| Tirar um arquivo do stage, mantendo a alteração | `git restore --staged <arquivo>` |
| Corrigir a mensagem do último commit (ainda não publicado) | `git commit --amend -m "nova mensagem"` |
| Desfazer um commit já publicado, sem reescrever o histórico | `git revert <hash>` |

`git revert` cria um commit novo que neutraliza o anterior e por isso é seguro em branches compartilhadas.
`--amend` reescreve o histórico e só deve ser usado em commits locais.

## 3. Branches, merge e rebase

| Comando | O que faz |
|:--|:--|
| `git branch` | Lista as branches locais |
| `git switch -c feature/nome` | Cria uma branch e muda para ela |
| `git switch main` | Volta para a branch principal |
| `git merge feature/nome` | Integra a branch na branch atual |
| `git merge --abort` | Cancela um merge com conflito |
| `git rebase main` | Reaplica os commits da branch atual sobre a `main` atualizada |

Em um conflito, o Git marca o trecho com `<<<<<<<`, `=======` e `>>>>>>>`. Escolha o conteúdo correto,
remova os marcadores, rode `git add` e conclua com `git commit`.

Regra de ouro: use rebase para organizar o trabalho local e merge para integrar com a equipe.

## 4. Trabalho em equipe

| Comando | O que faz |
|:--|:--|
| `git clone <url>` | Copia um repositório remoto para a máquina |
| `git push -u origin feature/nome` | Publica a branch no GitHub |
| `git pull` | Traz e integra as mudanças do remoto |
| `git fetch upstream` | Busca atualizações do repositório original de um fork |
| `git remote add upstream <url>` | Registra o repositório original como `upstream` |

Fluxo do GitHub Flow: criar a Issue, criar a branch, commitar, publicar, abrir o Pull Request com
`Closes #N`, passar pelo Code Review, fazer o merge e apagar a branch.

Comentários de review são classificados como `[Sugestão]`, `[Bloqueador]` ou `[Opcional]`.
