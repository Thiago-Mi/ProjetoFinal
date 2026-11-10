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

## Dificuldades

- **Conflitos de merge.** Foi a parte que mais exigiu atenção. Quando duas branches alteraram a mesma linha do
  README, o Git não escolheu por mim: tive que ler os marcadores `<<<<<<<` e `>>>>>>>`, decidir o que manter e concluir o
  merge. No trabalho em dupla o conflito reapareceu, porque os dois Pull Requests editavam o início do mesmo arquivo.
  Aprendi que o segundo PR a ser integrado é o que sofre o conflito, e que PRs pequenos e em arquivos diferentes reduzem
  esse risco.
- **Reescrever histórico.** O `--amend` muda o hash do commit. Isso é inofensivo em um commit local, mas deixa de ser
  quando o commit já foi publicado ou está em uso por outra pessoa. A regra do curso (rebase só no que é local) passou a
  fazer sentido quando vi o hash mudar.
- **Code Review.** Escrever comentário técnico, classificado como Sugestão, Bloqueador ou Opcional, é diferente de
  apenas ler o código: é preciso justificar o motivo e criticar a solução, não a pessoa.

## Como vou aplicar

- Abrir uma Issue antes de começar qualquer mudança relevante e vincular o Pull Request com `Closes #N`.
- Trabalhar sempre em branch, nunca direto na `main`, e manter cada PR com uma mudança principal.
- Escrever mensagens de commit no padrão Conventional Commits, para que o histórico sirva de documentação.
- Revisar o próprio diff com `git diff --staged` antes de cada commit.
- Usar `git revert` em histórico compartilhado e reservar `--amend` e `rebase` para commits locais.

## Conclusão

O curso mudou a forma como enxergo o repositório: ele deixou de ser apenas o lugar onde o código fica guardado e passou
a ser o registro de como o trabalho foi feito, discutido e revisado. O portfólio publicado com GitHub Pages e este
projeto, desenvolvido com Issues, branches e Pull Requests, mostram esse fluxo de ponta a ponta.
