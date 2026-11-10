# Reflexão sobre o curso de Git e GitHub

## O que aprendi

Antes do curso eu usava o Git como uma ferramenta de backup: `add`, `commit` e `push`, sem pensar no histórico.
Ao longo das atividades passei a tratar o histórico como parte do trabalho:

- **Ciclo de vida local.** Entendi os estados de um arquivo (não rastreado, modificado, staged e commitado) e a diferença
  entre `git diff` e `git diff --staged`. O `.gitignore` e o padrão Conventional Commits tornaram o histórico legível.
- **Desfazer erros.** Aprendi três ferramentas diferentes para três situações: `git restore` para descartar o que ainda
  não foi commitado, `git commit --amend` para corrigir a mensagem do último commit e `git revert` para neutralizar um
  commit sem apagar o passado.
- **Branches e merge.** Vi que uma branch é só um ponteiro leve, e que isso torna barato trabalhar em paralelo.
- **Trabalho em equipe.** Percorri o ciclo completo do GitHub Flow: Issue, branch, Pull Request, Code Review e merge,
  com `Closes #N` fechando a Issue automaticamente.
- **Publicação.** Com o GitHub Pages, o mesmo repositório que guarda o código passou a hospedar um site.
