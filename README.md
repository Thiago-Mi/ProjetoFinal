# Guia Prático de Git e GitHub

Projeto Integrador Final do curso de Git e GitHub (CEFET-MG). O repositório reúne, em um guia consultável, o que foi
praticado ao longo do curso: versionamento local, desfazer erros, branches, trabalho em equipe e publicação na web.

**Site publicado:** https://thiago-mi.github.io/ProjetoFinal/

## Conteúdo

| Arquivo | Descrição |
|:--|:--|
| `index.html` e `css/style.css` | Página web do guia, publicada com GitHub Pages |
| `docs/comandos.md` | Referência dos comandos essenciais, organizada por etapa do fluxo |
| `reflexao.md` | Análise crítica do aprendizado ao longo do curso |

## Como visualizar localmente

```bash
git clone https://github.com/Thiago-Mi/ProjetoFinal.git
cd ProjetoFinal
```

Depois, abra o arquivo `index.html` no navegador. O site é estático e não precisa de instalação de dependências.

## Como o projeto foi desenvolvido

O repositório segue o GitHub Flow, o mesmo fluxo praticado no curso:

1. Cada entrega nasceu de uma **Issue**, encerrada automaticamente pelo `Closes #N` no Pull Request.
2. Cada Issue virou uma **branch** própria, com prefixo que indica o tipo de mudança (`feature/`, `docs/`).
3. Os commits seguem o padrão **Conventional Commits**, em português (`feat:`, `docs:`, `style:`, `chore:`).
4. A integração com a `main` foi feita por **Pull Request**, preservando o histórico das branches.

| Issue | Branch | Entrega |
|:--|:--|:--|
| #1 | `feature/pagina-guia` | Página web do guia |
| #2 | `docs/comandos-essenciais` | Referência de comandos |
| #3 | `docs/reflexao` | Reflexão sobre o curso |

## Tecnologias

HTML5, CSS3, Markdown, Git e GitHub Pages.

## Autor

Thiago Miranda Aboboreira ([@Thiago-Mi](https://github.com/Thiago-Mi)), Engenharia de Computação no CEFET-MG.
Trabalho individual.
